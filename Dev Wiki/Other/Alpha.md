>[!Version]
>This only applies to versions < 0.6.0.3592

_Sync'd to version from 23 December 2018._

This page contains information about the map/terrain files used in the alpha. For information added on 2012-03-24 : files I looked at come from 0.5.3.3368 (Mjollnà).

# WDT

In the Alpha the ADTs and the WDT were just one big file with this structure :

## MVER

```
struct
{
  uint32_t version; // 18, just as all others
} mver;
```

## MPHD

```
struct SMMapHeader
{
  uint32_t nDoodadNames;
  uint32_t offsDoodadNames;   // [MDNM](https://wowdev.wiki/Alpha#MDNM "Alpha")
  uint32_t nMapObjNames;
  uint32_t offsMapObjNames;   // [MONM](https://wowdev.wiki/Alpha#MONM "Alpha")
  uint8_t pad[112];
};
```

## MAIN

- **Map tile table.** Needs to contain 64x64 = 4096 entries of sizeof(SMAreaInfo)

```
struct SMAreaInfo
{
  uint32_t offset;     // absolute offset [MHDR](https://wowdev.wiki/Alpha#MHDR "Alpha")
  uint32_t size;       // offset relative to MHDR start (so value can also be read as : all ADT chunks total size from MHDR to first MCNK) [MCNK](https://wowdev.wiki/Alpha#MCNK "Alpha")
  uint32_t flags;      // FLAG_LOADED = 0x1 is the only flag, set at runtime
  uint8_t pad[4];
};
```

## MDNM

Filenames Doodads. Zero-terminated strings with complete paths to models.

## MONM

Filenames WMOS. Zero-terminated strings with complete paths to models.

### MODF (optional)

Only one instance is possible. It is usually used by WMO based maps which contain no ADT parts with the exception of RazorfenDowns. If this chunk exists, the client marks the map as a dungeon and uses absolute positioning for lights.

[See the new files.](https://wowdev.wiki/WDT#MWMO.2C_MODF_chunks "WDT")

## MHDR

The start of what is now the ADT files.

```
struct SMAreaHeader
{
  uint32_t offsInfo;    // [MCIN](https://wowdev.wiki/Alpha#MCIN "Alpha")
  uint32_t offsTex;     // [MTEX](https://wowdev.wiki/Alpha#MTEX "Alpha")
  uint32_t sizeTex;
  uint32_t offsDoo;     // [MDDF](https://wowdev.wiki/Alpha#MDDF "Alpha")
  uint32_t sizeDoo;
  uint32_t offsMob;     // [MODF](https://wowdev.wiki/Alpha#MODF_.28in_ADT_part.29 "Alpha")
  uint32_t sizeMob;
  uint8_t pad[36];
};
```

### MCIN

256 Entries, so a 16*16 Chunkmap.

[See the new files.](https://wowdev.wiki/ADT/v18#MCIN_chunk_.28.3CCata.29 "ADT/v18")

### MTEX

[See the new files.](https://wowdev.wiki/ADT/v18#MTEX_chunk "ADT/v18")

### MDDF

[See the new files.](https://wowdev.wiki/ADT/v18#MDDF_chunk "ADT/v18")

### MODF (in ADT part)

[See the new files.](https://wowdev.wiki/ADT/v18#MODF_chunk "ADT/v18")

## MCNK

The header is 128 bytes like later versions, but information inside is placed slightly differently. Offsets are relative to the end of MCNK header.

```
struct SMChunk
{
  uint32_t flags;                     // See SMChunkFlags
  uint32_t indexX;
  uint32_t indexY;
  float radius;
  uint32_t nLayers;
  uint32_t nDoodadRefs;
  uint32_t offsHeight;                // [MCVT](https://wowdev.wiki/Alpha#.28MCVT.29_sub-chunk "Alpha")
  uint32_t offsNormal;                // [MCNR](https://wowdev.wiki/Alpha#.28MCNR.29_sub-chunk "Alpha")
  uint32_t offsLayer;                 // [MCLY](https://wowdev.wiki/Alpha#MCLY_sub-chunk "Alpha")
  uint32_t offsRefs;                  // [MCRF](https://wowdev.wiki/Alpha#MCRF_sub-chunk "Alpha")
  uint32_t offsAlpha;                 // [MCAL](https://wowdev.wiki/Alpha#.28MCAL.29_sub-chunk "Alpha")
  uint32_t sizeAlpha;
  uint32_t offsShadow;                // [MCSH](https://wowdev.wiki/Alpha#.28MCSH.29_sub-chunk "Alpha")
  uint32_t sizeShadow;
  uint32_t areaid;
  uint32_t nMapObjRefs;
  uint16_t holes;
  uint16_t pad0;
  uint16_t predTex[8];
  uint8_t noEffectDoodad[8];
  uint32_t offsSndEmitters;           // MCSE
  uint32_t nSndEmitters;
  uint32_t offsLiquid;                // MCLQ
  uint8_t pad1[24];
};

enum SMChunkFlags
{
  FLAG_SHADOW = 0x1,
  FLAG_IMPASS = 0x2,
  FLAG_LQ_RIVER = 0x4,
  FLAG_LQ_OCEAN = 0x8,
  FLAG_LQ_MAGMA = 0x10,
};
```

### (MCVT) sub-chunk

No chunk name and no size.

It's composed of the usual 145 floats, but their order is different : alpha vertices are not interleaved... Which means there are all outer vertices first (all 81), then all inner vertices (all 64) in MCVT (and not 9-8-9-8 etc.). Unlike 3.x format, MCVT have absolute height values (no height relative to MCNK header 0x70).

```
struct 
{
  float height[9*9 + 8*8];
} mcvt;
```

### (MCNR) sub-chunk

No chunk name and no size.

Same as 3.x format, except values order which is like alpha MCVT : all outer values first, then all inner ones.

```
struct SMNormal
{
  uint8_t n[145][3];
  uint8_t pad[13];
};
```

### MCLY sub-chunk

[See the new files](https://wowdev.wiki/ADT/v18#MCLY_sub-chunk "ADT/v18").

```
struct SMLayer
{
  uint32_t textureId;
  uint32_t props;       // only use_alpha_map is implemented
  uint32_t offsAlpha;
  uint16_t effectId;
  uint8_t pad[2];
};
```

### MCRF sub-chunk

Since there are no MMDX/MWMO MMID/MWID in alpha ADT, MCRF entries directly point to index in MDNM and MONM chunks.

### (MCSH) sub-chunk

No chunk name and no size.

[See the new files.](https://wowdev.wiki/ADT/v18#MCSH_sub-chunk "ADT/v18")

### (MCAL) sub-chunk

No chunk name and no size.

[See the new files.](https://wowdev.wiki/ADT/v18#MCAL_sub-chunk "ADT/v18")

### (MCLQ) sub-chunk

No chunk name and no size.

[See the new files.](https://wowdev.wiki/ADT/v18#MCLQ_sub-chunk "ADT/v18")

### (MCSE) sub-chunk

No chunk name and no size.

[See the new files.](https://wowdev.wiki/ADT/v18#MCSE_sub-chunk "ADT/v18")