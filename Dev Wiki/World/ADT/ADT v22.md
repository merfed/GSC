_Sync'd to version from 3 March 2019._

_Most likely a temporary version. Do not bother implementing until final version is there. This is not used in current clients._

**This document may not list all chunks.**

# AHDR

- **H**ea**D**e**R**
- **Size**: 0x40

```cpp
DWORD version    // 22, mirrors MVER
DWORD vertices_x // 129
DWORD vertices_y // 129
DWORD chunks_x   // 16
DWORD chunks_y   // 16
DWORD[11]
```

# AVTX

- **V**er**T**e**X**
- **Size**: May be variable. It's based on the header. 
	- `header.vertices_x*header.vertices_y + (header.vertices_x-1)*(header.vertices_y-1) * 4 bytes (float)`

A large collection of floats. Again with `inner[(header.vertices_x-1)*(header.vertices_y-1)] and outer[header.vertices_x*header.vertices_y]` vertices.

**Important**: These are NOT mixed as in the ADT/v18s, but have the `129*129` field first, then the `128*128` one.

```cpp
float outer[129][129];
float inner[128][128];
```

Same should apply for the normals.

# ANRM

- **N**o**RM**als
- **Size**: May be variable. It's based on the header. 
	- `header.vertices_x*header.vertices_y + (header.vertices_x-1)*(header.vertices_y-1) * 3 bytes`

Like [[ADT v18]] these are triples of chars being a vector. 127 is 1.0, -127 is -1.0.

# ATEX

- **TEX**tures
- **Size**: Variable

Used for texture filenames. This is an array of chunks. There are as many chunks as there are textures used in this ADT tile, which is limited to 128 textures per ADT.

# ADOO

- **DOO**dad
- **Size**: Variable

Used for M2 and WMO filenames. Both are in here. Again, an array of chunks with a chunk for every filename.

# ACNK

- **C**hu**NK**
- **Size**: Variable

This one is a bit like the MCNK one. There is an header for it, if the size is bigger than 0x40. If it has an header, its like this:

```cpp
int indexX
int indexY
DWORD
int areaId
WORD
DWORD[4] lowdetailtextureingmap
WORD
DWORD[7]
```

## ALYR

- **L**a**Y**e**R**
- **Size**: 0x20 or more

This will include the alpha map if flags&0x100.

```cpp
int textureID // as in ATEX
int flags
DWORD[6]
```

### AMAP

- **alpha MAP**
- **Optional**
- **Size**: Variable (?)

Either uncompressed 8bit (depending on WDT) or 4bit RLE.

## ASHD

- **SH**a**D**ow map
- **Optional**
- **Size**: 0x200 (?)

Most likely like the old one.

## ACDO

- **Chunk - Definitions of Objects**
- **Optional**
- **Size**: 0x38

Doodads and WMOs are now both defined here.

```cpp
int modelid        // as in ADOO
float position[3]
float rotation[3]
float scale[3]
float
uint uniqueId
DWORD[]            // name / doodadsets?
```