- **Author**: Kanma
- **Syntax**:

A command-line tool to convert BLP image files to PNG or TGA format. The BLP images are used by Blizzard games.

Supports the following BLP formats:

* BLP1:
	* JPEG
	* Uncompressed without alpha channel
	* Uncompressed with alpha channel (8-bits)
* BLP2:
	* Uncompressed without alpha channel
	* Uncompressed with alpha channel (1- and 8-bits)
	* DXT1 without alpha channel
	* DXT1 with alpha channel (1-bit)
	* DXT3 with alpha channel (4- and 8-bits)
	* DXT5 with alpha channel (8-bit)

Works on MacOS X and Linux.

## Compilation

```
somewhere$ mkdir build
somewhere$ cd build
build$ cmake <path/to/the/source/of/BLPConverter>
build$ make
```

The executable will be put in build/bin/

To compile as a library add ``-DWITH_LIBRARY=YES`` as a flag to cmake.

## Usage

```
(Copied from ./BLPConverter --help)

Usage: ./BLPConverter [options] <blp_filename> [<blp_filename> ... <blp_filename>]

Options:
--help, -h:      Display this help
--infos, -i:     Display informations about the BLP file(s) (no conversion)
--dest, -o:      Folder where the converted image(s) must be written to (default: './')
--format, -f:    'png' or 'tga' (default: png)
--miplevel, -m:  The specific mip level to convert (default: 0, the bigger one)
```

## Extras

The Python script 'extra/convert_all.py' can be used to convert recursively in-place all the BLP files in a hierarchy of folders.

## Dependencies

The repository/package contain all the necessary files, no need to install any
other library.

The following libraries are used (and are part of the distribution):

* squish 1.10 (http://code.google.com/p/libsquish/), MIT License
* FreeImage 3.13.1 (http://freeimage.sourceforge.net/), FreeImage Public License - Version 1.0
* SimpleOpt 3.4 (http://code.jellycan.com/simpleopt/), MIT License

## License
BLPConverter is is made available under the MIT License. The text of the license is
in the file 'LICENSE'.

Under the MIT License you may use BLPConverter for any purpose you wish, without
warranty, and modify it if you require, subject to one condition:

   "The above copyright notice and this permission notice shall be included in
   all copies or substantial portions of the Software."

In practice this means that whenever you distribute your application, whether as
binary or as source code, you must include somewhere in your distribution the
text in the file 'LICENSE'. This might be in the printed documentation, as a
file on delivered media, or even on the credits / acknowledgements of the
runtime application itself; any of those would satisfy the requirement.

Even if the license doesn't require it, please consider to contribute your
modifications back to the community.

# Mangos BLP Format

*This is from the **/docs** folder in the source.*

The BLP file format!
Compiled by Magnus Ostberg (aka Magos)
MagosX@GMail.com

## Data Types

- **CHAR**   - 8bit character
- **BYTE**   - 8bit unsigned integer
- **WORD**   - 16bit unsigned integer
- **DWORD**  - 32bit unsigned integer
- **FLOAT**  - 32bit floating point number
- **COLOR**  - 32bit color value of type RGBA, one byte per channel
- **X[n]**   - An n-dimensional vector of type X

## Descriptions

- **[X | Y]** - Exactly one of the structures X and Y are present.
- **X** - A structure that must be present.
- **#X** - A flag value, more than one can be combined.

## Notes
A full mipmap chain must be present. The last mipmap must be 1x1 (no larger). If an image is 32x8 the mipmap chain must be 32x8, 16x4, 8x2, 4x1, 2x1, 1x1. Sizes not of powers of 2 seems to work fine too, the same rules for mipmaps still applies. Ex: 24x17, 12x8 (rounded down), 6x4, 3x2, 1x1 (rounded down).
  
## BLP Structure

```cpp
struct Blp
{
  DWORD 'BLP1';
  DWORD Compression;                   //0 - Uses JPEG compression
                                       //1 - Uses palettes (uncompressed)
  DWORD Flags;                         //#8 - Uses alpha channel (?)
  DWORD Width;
  DWORD Height;
  DWORD PictureType;                   //3 - Uncompressed index list + alpha list
                                       //4 - Uncompressed index list + alpha list
                                       //5 - Uncompressed index list
  DWORD PictureSubType;                //1 - ???
  DWORD MipMapOffset[16];
  DWORD MipMapSize[16];

  [BlpJpeg | BlpUncompressed1 | BlpUncompressed2]
};
```

## BLP JPEG Structure (Compression = 0)

```cpp
struct BlpJpeg
{
  DWORD JpegHeaderSize;

  BYTE[JpegHeaderSize] JpegHeader;

  struct MipMap[16]
  {
    BYTE[???] JpegData;
  };

  // Up to 16 mipmaps can be stored in a blp image. 2^16 = 65536, so there's
  // little risk it won't be enough. Each JPEG (JFIF to be more exact) image
  // is constructed by merging the header with the mipmap (all mipmaps uses
  // the same header. It seems like Warcraft 3 can handle JPEG header sizes
  // of 0 (in case you have trouble generating JPEG images using the same
  // header) however there are other fan tools that does not. Specifying a
  // low number like 4 will work too as the only shared data are the initial
  // JPEG markers.
  //
  // Each mipmap has a certain size and is located at  a certain offset as
  // specified in the main blp header. There can be (and sometimes are in
  // Blizzard's images) unused space between the JPEG header and the JPEG
  // data. Why this is I don't know!
  //
  // The JPEG header of Blizzard's images is usually 624 bytes long. This
  // may or may not be true for your own generated images depending on how
  // you generated them.
  //
  // The JPEG format is advanced so I won't go into detail here.
};
```

## BLP Uncompressed 1 Structure (Compression = 1, PictureType = 3 or 4)

```cpp
struct BlpUncompressed1
{
  COLOR[256] Palette;

  struct MipMap[16]
  {
    BYTE IndexList[CurrentWidth * CurrentHeight];
    BYTE AlphaList[CurrentWidth * CurrentHeight];
  };

  // CurrentWidth/CurrentHeight is the width/height for the current mipmap.
  // Mipmap size/offset works the same as explained for JPEGs above.
  //
  // Each cell in the index list refers to a location in the palette where
  // the corresponding RGB value is (the palette is still RGBA, but A is not
  // used). The alpha list contains the alpha value for the pixel.
};
```

## BLP Uncompressed 2 Structure (Compression = 1, PictureType = 5)

```cpp
struct BlpUncompressed2
{
  COLOR[256] Palette;

  struct MipMap[16]
  {
    BYTE IndexList[CurrentWidth * CurrentHeight];
  };

  // CurrentWidth/CurrentHeight is the width/height for the current mipmap.
  // Mipmap size/offset works the same as explained for JPEGs above.
  //
  // Each cell in the index list refers to a location in the palette where
  // the corresponding RGBA value is. The alpha value is inversed so the real
  // alpha is "255 - alpha".
};
```

# Versions

| Name         | Filesize         | Author | Source ? | Notes |
| ------------ | ---------------- | ------ | -------- | ----- |
| BLPConverter | 12.6 MB (Source) | Kanma  | ✔️       | `6-22-2015`      |

# Links
* [Github](https://github.com/Kanma/BLPConverter)