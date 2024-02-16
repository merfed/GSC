- **Author**: Sigmur
- **Syntax**:

Ground effects are the little plants and rock that the game display on certain parts of your map. They're referenced in GroundEffectTexture.dbc, you can find a lot if various tutorials on how to edit this DBC. On an ADT, you have `16*16` chunks, each chunk can hold up to 4 texture and on each texture you can link one ground effect id from the GroundEffectTexture.dbc. Very important to understand if you want to use the tool.

**This program doesn't automattically**:
- Place ground effects where you used a specific texture.
- Put ground effects everywhere, if you clear a chunk in noggit, you'll need to set ground effects again.

**On a chunk you can**:
- Set which ground effect goes with which texture.
- Set on an 8 by 8 representation of the chunk, where each ground effect will be used.
- Set on an 8 by 8 representation of the chunk, where no ground effect at all will be displayed.
- Toggle ground effect display on/off on a whole chunk.
- Fill a whole chunk with a ground effect.

**On a full ADT you can**:
- Export the current ground effect settings of all chunks
- Import ground effect settings from previous export. Even if you repaint in Noggit and a texture doesn't have the same index, it'll match the previous texture and apply the ground effect datas.

> [!Important] Important
> This progam uses QT5 to parse paths, this means you can use forward and backward slashes in them, even on windows. You can even mix backward and forward slashes ("`E:/Wow 3.3.5\world\maps/azeroth\azeroth_30_30.adt`" is a valid path).

# Usage

```
./"Sigmur's Ground Effect Editor.exe" [x|i] [target_path] (mge_file_path)
```

- `[x|i]`: Export data from ADT to file or import data from file to ADT
- `[target_path]`: On export and import with no source, this can be a path with wildcard selection (see examples)
- `(mge_file_path)`: Optional, used only for import. If not `mge_file_path` is specified, import will look for `.mge` files with the same name as the adt.

# Examples

**ADT Folder Contains**:
```
"E:\Wow 3.3.5\world\maps\azeroth" containing "azeroth_30_30.adt" and "azeroth_30_31.adt"
```

**Exporting ground effects from ADTs**:
```
./"Sigmur's Ground Effect Editor.exe" x "E:/Wow 3.3.5/world/maps/azeroth/*.adt"
```

**Exporting ground effects from specific ADT**:
```
./"Sigmur's Ground Effect Editor.exe" x "E:/Wow 3.3.5/world/maps/azeroth/azeroth_30_30.adt"
```

**Importing ground effect to every ADT, will look for same filename with extension .mge instead of adt**:
```
./"Sigmur's Ground Effect Editor.exe" i "E:/Wow 3.3.5/world/maps/azeroth/*.adt"
```

**Importing ground effect to specific ADT**
```
./"Sigmur's Ground Effect Editor.exe" i "E:/Wow 3.3.5/world/maps/azeroth/azeroth_30_30.adt"
```

**Importing specific ground effect data to specific ADT**
```
./"Sigmur's Ground Effect Editor.exe" i "E:/Wow 3.3.5/world/maps/azeroth/azeroth_30_30.adt" "E:/Wow 3.3.5/world/maps/azeroth/azeroth_30_30_specific_file.mge"
```

# Technical Info

Ground effect datas are stored in MCNK header as a `uint2[8][8]` layer map (128 bits) and an `uint1[8][8]` (64 bits) toggle map.

The data starts right after the holes datas, offset 64 from the MCNK header, 72 from the MCNK magic word beginning.

The first 128 bits (`4 uint32`) are the layer map. It's composed of an `8 x 8` representation of the chunk, each point is a number between 0 and 3. These numbers are indices to MCLY datas, this define what ground effect id (contained in the targeted MCLY) will be displayed at the target subchunk X/Y.

The next 64 bits (`2 uint32`), often miscalled `predTex` & `noEffectDoodad`, are used for a no effect bitmap. It's another 8 x 8 representation of the chunk that contains where no effects will be shown. Since the effect map can only have numbers between 0 and 3, they needed another map to tell where not to put stuff on. Each point is a single bit that tells the game if you want to hide ground effect on X/Y or not.

**Code used to access/save data**:
_made in QT5, so quint16 = uint16_t_

```
quint16* effect_layer_map[8];    //8*8 map of uint2    - uint16 = 16 bits, we'll use 2 bits per point, 1 uint16 = 8 points
quint8* effect_togg{le_map[8];    //8*8 map of uint1    - uint8 = 8 bits, 1 bit per point, ez
quint8 layer_map_edit[8][8];    //8*8 map of uint8    - easier to use
bool toggle_map_edit[8][8];        //8*8 map of bool    - wich subchunk is toggle or not easier to use

char* pos = raw_mcnk_datas_starting_after_magic_and_size; //I store a copy of the raw MCNK data in the structure that loads it and edit it directly
pos += 64; //Skip everything until effect layer map
//Put every pointers at the right position
for (int i = 0; i < 8; i++)
    effect_layer_map[i] = (quint16*)(pos + (i * 2));
pos += 16; //go to toggle map begin, toggle map equiv to 2 uint32
for (int i = 0; i < 8; i++)
    effect_toggle_map[i] = (quint8*)(pos + i);

//Parse layer & toggle maps
for (int mx = 0; mx < 8; mx++)
{
    quint16 tmp = *effect_layer_map[mx];
    for (int my = 0; my < 8; my++)
    {
        layer_map_edit[mx][my] = (tmp & 1) + (tmp & 2);
        tmp = tmp >> 2;
        toggle_map_edit[mx][my] = (*effect_toggle_map[mx] & (1 << my));
    }
}

// Here you can edit your maps using the _edit versions

//Save the stuff back to the adt
for (int mx = 0; mx < 8; mx++)
{ //Rewrite ground effect maps
    quint16 layer_map_row = 0;
    quint8 toggle_map_row = 0;
    for (int my = 7; my >= 0; my--)
    { //Going in reverse this time, or your world will be ass backward
        if (toggle_map_edit[mx][my])
            toggle_map_row += 1;
        layer_map_row += layer_map_edit[mx][my];
        if (my > 0)
        {
            layer_map_row = layer_map_row << 2;
            toggle_map_row = toggle_map_row << 1;
        }
    }

    //Put the rewritten line in the corresponding map
    *(effect_layer_map[mx]) = layer_map_row;
    *(effect_toggle_map[mx]) = toggle_map_row;
}}
```


# Versions

| Name | Filesize | Author | Source ? | Notes |
| ---- | -------- | ------ | -------- | ----- |
|      |          |        |          |       |

# Video

- [Video Tutorial](https://www.youtube.com/watch?v=rNrmRSBZ4iM)