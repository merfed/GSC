_Sync'd to version from 15 November 2022._

WDL files contain a low-resolution heightmap for a world. This is probably what the WoW client uses to draw the solid-colored mountain ranges in the background ('in front of' the sky, but 'behind' the fog and the rest of the scenery). It can also be conveniently used to construct a minimap - however, since no water level information is present, the best guess is 0 (sea level) - this results in some lower-than-sea-level areas being blue on the WoWmapview minimap. Oh well. :)

- [Chunked](https://wowdev.wiki/Chunk "Chunk") structure.

> [!Note] This section only applies to version <span class="wrath">Wrath</span> (3.3.5.12340)
> The WotLK parser is very picky about the files it reads. It assumes that if there is a [#MWMO](https://wowdev.wiki/WDL/v18#MWMO) chunk as the first chunk, the [#MWID](https://wowdev.wiki/WDL/v18#MWID) and [#MODF](https://wowdev.wiki/WDL/v18#MODF) chunks follow in that order. Otherwise, or after the three, it *will* be [#MAOF](https://wowdev.wiki/WDL/v18#MAOF), and after that it only uses the offsets in that chunk to parse [#MAREs](https://wowdev.wiki/WDL/v18#MARE).

# Object Related Chunks

> [!Note] This section only applies to verisons <= <span class="wod">WoD</span>

MWMO, MWID and MODF chunks seem to have been added to every WDL and contain information about low resolution [WMO](https://wowdev.wiki/WMO "WMO") used to create a silhouette.

## MWMO

**Filenames for [WMO](https://wowdev.wiki/WMO "WMO") that appear in the low resolution map.** Zero terminated strings.

## MWID

**List of indexes into the MWMO chunk.**

## MODF

**Placement information for the [WMO](https://wowdev.wiki/WMO "WMO").** Appears to be the same 64 byte structure used in the [WDT](https://wowdev.wiki/WDT "WDT") and [ADT](https://wowdev.wiki/ADT "ADT") MODF chunks.

> [!Note] This section only applies to verisons >= <span class="legion">Legion</span>

In Legion it seems MWMO, MWID and MODF were removed from this file. And MLDD, MLDX, MLMD, MLMX were added instead. They seem to have same structure as in [_obj1.adt](https://wowdev.wiki/ADT "ADT") files

## MLDD

**Placement information for the [M2](https://wowdev.wiki/M2 "M2"). Reference: [MLDD](https://wowdev.wiki/ADT#MLDD_.28Legion.2B.29 "ADT")**

## MLDX

**Defines bounding box and radius for visibility detection for M2 from MLDD. Reference: [MLDX](https://wowdev.wiki/ADT#MLDX_.28Legion.2B.29 "ADT")**

## MLMD

**Placement information for the [WMO](https://wowdev.wiki/WMO "WMO"). Reference: [MLMD](https://wowdev.wiki/ADT#MLMD_.28Legion.2B.29 "ADT")**

## MLMX

**Defines bounding box and radius for visibility detection for WMO from MLMD. Reference: [MLMX](https://wowdev.wiki/ADT#MLMX_.28Legion.2B.29 "ADT")**

_NOTE: as there is no chunks with file names for WMO, both MLDD and MLMD use **[FileDataId](https://wowdev.wiki/CASC#World_of_Warcraft_2 "CASC")** from CASC storage for referencing the file with model_

# MAOF

- **Map Area Offset.**

Contains `64*64` = 4096 unsigned 32-bit integers, these are absolute offsets in the file to each map tile's MapAreaLow-array-entry. For unused tiles the value is 0.

```
/*000h*/ UINT32 areaLowOffsets[4096];
_or_
/*000h*/ UINT32 areaLowOffsets[64][64];
```

# MSSN

> [!Note] This section only applies to version >= <span class="sl">SL</span>

32 bytes per entry (At a cursory glance)ᵘ

uint at start ties this entry to SkySceneXPlayerCondition.db2::SkySceneID

```cpp
 struct mssn_t
 {
     uint32_t SkySceneID;
     uint32_t unk_1;        // Number of records in SkySceneXPlayerCondition?
     int16_t msscIndex;
     int16_t msscRecordsNum;
     uint16_t mssoIndex;
     int16_t mssoRecordsNum;
     uint32_t unk_4;
     uint32_t unk_5;
     uint32_t unk_6;
     uint32_t unk_7;
 };
```

# MSCC

> [!Note] This section only applies to version >= <span class="sl">SL</span>

28 bytes per entry (At a cursory glance)ᵘ

This chunk defines SkySceneCondition

```cpp
 struct mssc_t
 {
     uint32_t unk_0;
     uint32_t unk_1;
     uint32_t conditionType; // 1 - conditionValue is id into AreaTable.db2 (current player's area should be parent to this one)
                             // 2 - conditionValue is id into LightParams.db2
                             // 3 - conditionValue is id into LightSkybox.db2 (target skybox should be assigned as current one)
                             // 5 - conditionValue is id into ZoneLight.db2 
     uint32_t unk_3;
     uint32_t unk_4;
     uint32_t unk_5;
     uint32_t conditionValue;
 };
```

# MSSO

> [!Note] This section only applies to version >= <span class="sl">SL</span>

48 bytes per entry (At a cursory glance)ᵘ

uint at 0x08 is a m2 filedataid

```cpp
 struct msso_t
 {
     uint32_t unk_0;
     uint32_t unk_1;
     uint32_t fileDataID;
     C3Vector translateVec;
     C3Vector rotationInRads;
     float scale;
     uint32_t unk_2;
     uint32_t unk_11;
 };
```

# MapAreaLow Array

WoD (cata?): if neither MAHO nor MARE present: `CMapAreaLow::CreateOceanInstance()`

## MARE

**Map Area**

Heightmap for one map tile. Contains` 17*17` + `16*16` = 545 signed 16-bit integers. So a 17 by 17 grid of height values is given, with additional height values in between grid points. Here, the "outer" 17x17 points are listed (in the usual row major order), followed by 16x16 "inner" points. The height values are on the same scale as those used in the regular height maps.

## MAOC

This chunk appears to define vertices for an occlusion mesh. The values are passed in to `CMapAreaLow::CreateOcclusion`.

> [!Note] This section only applies to versions <= <span class="wod">WoD</span>

```cpp
// optional
struct MAOC
{
  short[];
}
```

## MAOE

> [!Note] This section only applies to version >= <span class="legion">Legion</span>

```cpp
// optional, but shall be before MAHO else ignored
// This defines ocean (float?) texture (m_ocean or AreaOceanAlphaTexture)
struct
{
  // ??? fixed size 0x20, some mask?
};
```

## MAHO

After each MARE chunk there follows a MAHO (MapAreaHOles) chunk.

This chunk is an array of 16 uint16_t values. Each one is a bitmask, representing a boolean value that determines whether or not there is a hole at that position - if the bit is set, there is a hole at that position.

If the MAHO chunk is missing, the client will treat that map area as having a MAHO chunk with all values set to 0. In Blizzard's files, the chunk is always included no matter what the values are. This behavior is most likely a form of backwards compatibility to allow the client to load WDL files from before Wrath of the Lich King. Blizzard seems to set a WDL hole entry if all 16 holes in an ADT chunk are set.

The holes positions seem to be ordered like this :

Values : Y axis, flags(values flags) : X axis. Each flag set for each value is a whole chunk.

Example : Value #4 has bit 8 set, this means the chunk Y4,X8 is a hole. (simplified, id positions start at 0).