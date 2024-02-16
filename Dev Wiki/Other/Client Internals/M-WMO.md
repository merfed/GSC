_Sync'd to version from 20 May 2014._

Static Pointer for M2 Array 1 as for WoW 2.4.1  // 2008 By Malu05

```
0x00CFA84C
WMO ARRAY SIZE: 0x140
```

Static Pointer for M2 Array 1 as for WoW 3.0.3  // 2008 By Malu05

```
0x00CFA84C
WMO ARRAY SIZE: 0x160
```

```
0xA4: X
0xA8: Y
0xAC: Z
```

```
struct WMO
{

/* 0000001C */ char[256] Filename 

/* 00000120 */ void* MOHD
/* 00000124 */ void* MOTX
/* 00000128 */ void* MOGN
/* 0000012C */ void* MOSB
/* 00000130 */ void* MOGI
/* 00000134 */ void* MOPV
/* 00000138 */ void* MOPT
/* 0000013C */ void* MOPR
/* 00000140 */ void* MOVV
/* 00000144 */ void* MOVB
/* 00000148 */ void* MOLT
/* 0000014C */ void* MODS
/* 00000150 */ void* MODN
/* 00000154 */ void* MODD
/* 00000158 */ void* MFOG
/* 0000015C */ void* MCVP
/* 00000160 */ int MOTX_size
/* 00000164 */ int MOGN_size
/* 00000168 */ int MOGI_entries
/* 0000016C */ int MOPV_entries
/* 00000170 */ int MOPT_entries
/* 00000174 */ int MOPR_entries
/* 00000178 */ int MOVV_entries
/* 0000017C */ int MOVB_entries
/* 00000180 */ int MOLT_entries
/* 00000184 */ int MODS_entries
/* 00000188 */ int MODN_size
/* 0000018C */ int MODD_entries
/* 00000190 */ int MFOG_entries
/* 00000194 */ int MCVP_entries
/* 00000198 */ color Header_color

/* 000001A0 */ Vec3f boundingbox_1
/* 000001AC */ Vec3f boundingbox_2 

/* 000001C0 */ void* FullFile
/* 000001C4 */ int FileSize

/* 000001CC */ float float_1CC
/* 000001D0 */ void* AsyncObject
/* 000001D4 */ int AsyncObject_isfinished
/* 000001D8 */ void* MOMT
/* 000001DC */ int MOMT_entries

/* 000001F0 */ int nGroupWMOs
/* 000001F4 */ GroupWMO[] GroupWMOs
/* 000001F8 */
}

struct GroupWMO
{

/* 00000030 */ int header_flags
/* 00000034 */ Vec3f boundingbox_1
/* 00000040 */ Vec3f boundingbox_2
/* 0000004C */ int header_indexintoMOPR
/* 00000050 */ int header_MOPR_itemsused
/* 00000054 */ int header_fogs
/* 00000058 */ short header_batches_a
/* 0000005A */ short header_batches_b
/* 0000005C */ short header_batches_c

/* 000000D4 */ byte field_D4 

/* 000000DC */ void* MOPY
/* 000000E0 */ void* MOVI
/* 000000E4 */ void* UnknownChunk
/* 000000E8 */ void* MOVT
/* 000000EC */ void* MONR
/* 000000F0 */ void* MOTV
/* 000000F4 */ void* MOBA
/* 000000F8 */ void* UnknownChunk2
/* 000000FC */ void* MOLR
/* 00000100 */ void* MODR
/* 00000104 */ void* VerticesData
/* 00000108 */ void* VerticesIndexData
/* 0000010C */ void* MOCV
/* 00000114 */ int Water_xverts
/* 00000118 */ int Water_yverts
/* 0000011C */ int Water_xtiles
/* 00000120 */ int Water_ytiles
/* 00000124 */ Vec3f Water_float_base
/* 00000130 */ short Water_materialId
/* 00000134 */ int Water_vertices
/* 00000138 */ int Water_field_138
/* 0000013C */ int Water_field_13C
/* 00000140 */ int Water_field_140
/* 00000144 */ int Water_Something

/* 00000150 */ int MOPY_entries
/* 00000154 */ int MOVI_entries
/* 00000158 */ int UnknownChunk_entries
/* 0000015C */ int MOVT_entries
/* 00000160 */ int MONR_entries
/* 00000164 */ int MOTV_entries
/* 00000168 */ int MOBA_entries
/* 0000016C */ int MOLR_entries
/* 00000170 */ int MODR_entries
/* 00000174 */ int MOCV_entries
/* 00000178 */ int WMOGroupID
/* 0000017C */ void* File
/* 00000180 */ int FileSize
/* 00000184 */ void* SOMESUBCLASS
/* 0000018C */ void* AsyncObject
/* 00000190 */ byte field_190 

/* 0000019C */ 
}
```