- **Author**: Relaxok
- **Syntax**:

# Original Readme

Hi all -

I had been previously been trying to rely on some combination of two versions of BLPConverter and BLPLab to convert every blp in the MPQ tree to a png for use in non blizz things. Unfortunately while they are pretty good there are still certain file types and methods that these tools fail on, making it pretty much impossible to have a toolchain where an engine doesn't complain that stuff is missing. I'm sure if you have been hardcore into anything with BLPs you'll know how most of the 4-bit alpha textures do not work with the converters available, for example.

Anyway, I got pretty fed up yesterday and wrote a BLP Converter.. it seems to handle all the texture types correctly with my testing so far.. I'd like to release a version of it to the community as a very simple CLI tool.. blah.exe infile outfile, maybe with some options. Currently I have it writing out to my own .TXR format with mipmaps included.

If you were to have a tool like this, what are the primary outputs you'd want, say besides PNG? Is that good enough? What about the other mipmaps beyond the base level? What about other features?

FYI I'm only testing it with WOTLK data, except for Interface data which is whatever's the latest on bnet. It seems to work with the newer uncompressed A8R8G8B8 types as well so it might work for all MoP stuff, not sure. If someone wants to try let me know. I"d like to find out what bugs might exist as currently I'm just going around the world seeing if anything looks off. One thing that might need testing is clothing type textures... 

Curious about going in the other direction as well (? to BLP).. what do you all use for that and is it okay for your purposes? The above tools seem to work okay for that but I don't do that much.

Would be glad to share the code as well if anyone is interested, PM me.. it's very very small/short/easy.

# Versions

| Name      | Filesize      | Author  | Source ? | Notes |
| --------- | ------------- | ------- | -------- | ----- |
| blp (old) | 2 KB (Source) | Relaxok | ✔️       |       |
| blp       | 5 KB (Source) | Relaxok | ✔️         |       |

There are two versions of this (possibly from earlier development periods). Orginally retrieved on 12/8/2015.

## Version 1

```cpp
#ifndef BLP_H
#define BLP_H

#include <string>

enum BLP_TYPE
{
	BLP_TYPE_JPEG						= 0, // unused it seems
	BLP_TYPE_UNCOMPRESSED_OR_DIRECTX	= 1,
};

enum BLP_ENCODING
{
	BLP_ENCODING_UNCOMPRESSED	= 1,
	BLP_ENCODING_DIRECTX		= 2,
	BLP_ENCODING_A8R8G8B8		= 3, // >= cataclysm?
};

enum BLP_ALPHAENCODING
{
	BLP_ALPHAENCODING_DXT1				= 0,
	BLP_ALPHAENCODING_DXT3				= 1,
	BLP_ALPHAENCODING_UNK_CATA_A8R8G8B8 = 2,
	BLP_ALPHAENCODING_UNK_3				= 3,
	BLP_ALPHAENCODING_UNK_TAXIMAPS		= 4, // didnt see anything else with this?
	BLP_ALPHAENCODING_UNK_5				= 5, // unused?
	BLP_ALPHAENCODING_UNK_6				= 6, // unused?
	BLP_ALPHAENCODING_DXT5				= 7,
	BLP_ALPHAENCODING_UNK_1BIT_PALETTE	= 8,
};

enum BLP_MIPTYPE
{
	BLP_MIPTYPE_NOMIPS	= 0,
	BLP_MIPTYPE_HASMIPS = 1,
};

struct BLP_HEADER // from wikipedia
{
	char fourcc[4]; // BLP2

	unsigned __int32 Type;
	unsigned __int8  Encoding;
	unsigned __int8  AlphaDepth;
	unsigned __int8  AlphaEncoding;
	unsigned __int8	 MipType;
	unsigned __int32 Width;
	unsigned __int32 Height;
	unsigned __int32 Offsets[16];
	unsigned __int32 Lengths[16];
	unsigned __int32 Palette[256];
};

class BLP
{
	public:
		BLP()
		{
			memset( &header, 0, sizeof(BLP_HEADER) );
			for( unsigned int i = 0; i < 16; ++i )
			{
				raw_mips[i] = 0;
				conv_mips[i] = 0;
			}
		}
		virtual ~BLP()
		{
			for( unsigned int i = 0; i < 16; ++i )
			{
				if( raw_mips[i] )
					delete [] raw_mips[i];
				if( conv_mips[i] )
					delete [] conv_mips[i];
			}
		}

	BLP_HEADER header;
	unsigned char* raw_mips[16];  // raw
	unsigned char* conv_mips[16]; // converted

	BLP_TYPE			Type;			// enum casting types are friendlier
	BLP_ENCODING		Encoding;		// ...
	BLP_ALPHAENCODING	AlphaEncoding;  // ...
	BLP_MIPTYPE			MipType;		// ...

	unsigned int NumMips;
};

BLP* BLP_LoadTexture( std::string infilename );

#endif // BLP_H
```

## Version 2

```cpp
// blp.cpp - by relaxok | 17 Aug 2013
// Converts all .BLP types to raw RGBA buffers
// This should correctly convert all textures from MPQ data in the 3.3.5 client

#include <assert.h>
#include "blp.h"
#include "common.h"
#include "squish.h"

static const int COLOR_SIZE = 4; // 4 bytes for A8R8G8B8

BLP* BLP_LoadTexture( std::string infilename )
{
   BLP* blp = new BLP();

   OPEN_NEW_FILE_FOR_READ( infilename );
   READ_WHOLE_FILE_BUF( infilename );
   unsigned char* fileStart = fileBuf;

   // Read header and enum-ify some values for ease of debugging
   READ_BUF_DATA( blp->header );

   blp->Type         = (BLP_TYPE)         blp->header.Type;
   blp->Encoding      = (BLP_ENCODING)      blp->header.Encoding;
   blp->AlphaEncoding   = (BLP_ALPHAENCODING)   blp->header.AlphaEncoding;
   blp->MipType      = (BLP_MIPTYPE)         blp->header.MipType;

   blp->NumMips = blp->header.Width > blp->header.Height   ? (unsigned int)( log10( blp->header.Width  ) / log10(2) + 1 ) 
                                             : (unsigned int)( log10( blp->header.Height ) / log10(2) + 1 );

   // Some sanity checking
   assert( blp->Type == BLP_TYPE_UNCOMPRESSED_OR_DIRECTX );
   assert( blp->Encoding >= BLP_ENCODING_UNCOMPRESSED && blp->Encoding <= BLP_ENCODING_A8R8G8B8 );
   assert( blp->AlphaEncoding >= BLP_ALPHAENCODING_DXT1 && blp->AlphaEncoding <= BLP_ALPHAENCODING_UNK_1BIT_PALETTE );
   
   // These temp vars change in the loop
   unsigned int mipWidth = blp->header.Width;
   unsigned int mipHeight = blp->header.Height;
      
   for( unsigned int i = 0; i < blp->NumMips; ++i )
   {
      unsigned int mipRez = mipWidth * mipHeight;

      // Read in raw mip
      blp->raw_mips[i] = new unsigned char[ blp->header.Lengths[i] ];
      memcpy( blp->raw_mips[i], fileStart + blp->header.Offsets[i], blp->header.Lengths[i] );

      // .. convert
      blp->conv_mips[i] = new unsigned char[ mipRez * COLOR_SIZE ];
      memset( blp->conv_mips[i], 0, sizeof( mipRez * COLOR_SIZE ) );
      
      if( blp->Encoding == BLP_ENCODING_UNCOMPRESSED ) // UNCOMPRESSED PALETTIZED MODES
      {
         bool nibbleflip = false; // alphaDepth 4 nibbles alternate
         for( unsigned int j = 0; j < mipRez; ++j )
         {
            unsigned __int32 bgra = blp->header.Palette[ *( blp->raw_mips[i] + j ) ];
	    unsigned __int32 pixelColor = ( bgra & 0xFF000000 ) | ( ( bgra & 0x00FF0000 ) >> 16 ) | ( bgra & 0x0000FF00 ) | ( ( bgra & 0x000000FF ) << 16 );
            unsigned char* baseOffset = fileStart + blp->header.Offsets[i] + mipRez;
      
            if     ( blp->header.AlphaDepth == 0 ) pixelColor |= 0xFF000000;
            else if( blp->header.AlphaDepth == 1 )
            {
               unsigned char pixelAlphaBit = ( ( *( baseOffset + (unsigned int)( j / 8 ) ) ) >> ( j % 8 ) ) & 1;
               pixelColor |= ( pixelAlphaBit ? 0xFF000000 : 0 );
            }
            else if( blp->header.AlphaDepth == 4 )
            {
               unsigned char pixelAlphaByte = *( baseOffset + (unsigned int)( j / 2 ) );
               unsigned char pixelAlphaNibble = !nibbleflip ? ( ( pixelAlphaByte & 0xf0 ) >> 4 ) : pixelAlphaByte & 0x0f;
               pixelColor |= ( ((unsigned __int32)pixelAlphaNibble) << 24 );
               nibbleflip = !nibbleflip;
            }
            else if( blp->header.AlphaDepth == 8 ) pixelColor |= (unsigned __int32)( ( *( baseOffset + j ) ) );
            else assert(false); // invalid

            memcpy( blp->conv_mips[i] + j * COLOR_SIZE, &pixelColor, COLOR_SIZE );
         }
      }
      else if( blp->Encoding == BLP_ENCODING_DIRECTX ) // DXT COMPRESSED MODES
      {
         int   DXTMode = -1;
         if     ( blp->AlphaEncoding == BLP_ALPHAENCODING_DXT1 ) DXTMode = squish::kDxt1; // DXGI_FORMAT_BC1_UNORM;
         else if( blp->AlphaEncoding == BLP_ALPHAENCODING_DXT3 ) DXTMode = squish::kDxt3; // DXGI_FORMAT_BC2_UNORM;
         else if( blp->AlphaEncoding == BLP_ALPHAENCODING_DXT5 ) DXTMode = squish::kDxt5; // DXGI_FORMAT_BC3_UNORM;
         else assert(false); // invalid
         
         squish::DecompressImage( blp->conv_mips[i], mipWidth, mipHeight, blp->raw_mips[i], DXTMode );
      }
      else memcpy( blp->conv_mips[i], blp->raw_mips[i], blp->header.Lengths[i] ); // direct copy

      mipWidth = max( mipWidth / 2, 1);
      mipHeight = max( mipHeight / 2, 1);
   }
      
   delete [] fileStart;
   return blp;
}
```
