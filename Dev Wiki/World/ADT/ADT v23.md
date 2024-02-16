_Sync'd to version from 16 June 2019._

This is another temporary version on the way to Cataclysm after [[ADT v22]]. It now has more chunks. (well, there are now more chunks in the leaked files.)

Do not bother implementing until final version is there. This is not used in current clients.

There might be some changes in the chunks below. I have not yet checked them but only added new ones!

**This document may not list all chunks.**

# AHDR: HeaDeR

- size: 0x40

```
DWORD version // 23, mirrors MVER
DWORD vertices_x // 129
DWORD vertices_y // 129
DWORD chunks_x // 16
DWORD chunks_y // 16
DWORD[11]
```

# AVTX: VerTeX

- size: may be variable but client hardcodes size. Its based on the header. `header.vertices_x*header.vertices_y + (header.vertices_x-1)*(header.vertices_y-1) * 4 bytes (float)`.

A large collection of floats. Again with` inner[(header.vertices_x-1)*(header.vertices_y-1)] and outer[header.vertices_x*header.vertices_y]` vertices.

Important: These are NOT mixed as in the [[ADT v18]]s, but have the `129*129` field first, then the `128*128` one.

```
float outer[129][129];
float inner[128][128];
```

for example. Same should apply for the normals.

# ANRM: NoRMals

- size: may be variable. Its based on the header. `header.vertices_x*header.vertices_y + (header.vertices_x-1)*(header.vertices_y-1) * 3 bytes`.

Like [[ADT v18]], these are triples of chars being a vector. 127 is 1.0, -127 is -1.0.

# ATEX: TEXtures

- size: variable

Used for texture filenames. This is an array of chunks. There are as many chunks as there are textures used in this ADT tile.

# ADOO: DOOdad

- size: variable

Used for [M2](https://wowdev.wiki/M2 "M2") and [WMO](https://wowdev.wiki/WMO "WMO") filenames. Both are in here. Again, an array of chunks with a chunk for every filename.

# ACNK: ChuNK

- size: variable

This one is a bit like the MCNK one. There is an header for it, if the size is bigger than 0x40. If it has an header, its like this, otherwise header size is zero for non-root adts:

```
/*0x00*/ int indexX
/*0x04*/ int indexY
/*0x08*/ uint32_t flags
/*0x0C*/ int areaId
/*0x10*/ WORD holes_low_res
/*0x12*/ DWORD[4] lowdetailtextureingmap
/*0x22*/ WORD mcdd
/*0x2A*/ char[6]
/*0x30*/ uint16 mcnk's unknown_but_used at 0x03E
/*0x32*/ char[8] high_res_holes // if flags & 0x10000
/*0x3A*/ char[6]
/*0x40*/ 
```

Due to the nature of the parser in the client, any ADT MCNK subchunk can appear as well. This is probably not intended.

## ALYR: LaYeR

- size: 0x20 or more.

This will include the alpha map if `flags&0x100`.

```
/*0x00*/ int textureID // as in ATEX
/*0x04*/ int flags
/*0x08*/ DWORD[6]
/*0x20*/ 
```

Note: AMAP is a sub-chunk here!

### AMAP: alpha MAP

- optional. size: variable (?)

either uncompressed 8bit (depending on WDT) or 4bit RLE

Note: Due to laziness, contained chunks reuse the same parser again, so this could contain every other sub chunk again.

## ASHD: SHaDow map

- optional. size: 0x200 (?)

most likely like the old one.

## ACDO: Chunk - Definitions of Objects

- optional. size: 0x38

Doodads and WMOs are now both defined here.

```
int modelid // as in ADOO
float position[3]
float rotation[3]
float scale[3]
float
uint uniqueId
DWORD[] // name / doodadsets?
```

# AFBO: Flight BOx information

- size: 0x48

This again is just a list of two planes in shorts.

```
short[3][3] maximum;
short[3][3] minimum;
```

# ACVT: (Chunk?) VerTex shading

- size: may be variable. Its based on the header. `header.vertices_x*header.vertices_y + (header.vertices_x-1)*(header.vertices_y-1) * 4 bytes`. Like AVTX.

This now is over the whole ADT as the heightmap instead being a subchunk of the ACNK chunk. These are color values defined with 4 bytes: RGBA.