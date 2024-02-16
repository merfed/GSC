# 1.x

```cpp
#ifndef MODELHEADERS_H
#define MODELHEADERS_H

typedef unsigned char uint8;
typedef char int8;
typedef unsigned short uint16;
typedef short int16;
typedef unsigned int uint32;
typedef int int32;

#pragma pack(push,1)

struct ModelHeader {
	char id[4];
	uint8 version[4];
	uint32 nameLength;
	uint32 nameOfs;
	uint32 type;

	uint32 nGlobalSequences;
	uint32 ofsGlobalSequences;
	uint32 nAnimations;
	uint32 ofsAnimations;
	uint32 nC;
	uint32 ofsC;
	uint32 nD;
	uint32 ofsD;
	uint32 nBones;
	uint32 ofsBones;
	uint32 nF;
	uint32 ofsF;

	uint32 nVertices;
	uint32 ofsVertices;
	uint32 nViews;
	uint32 ofsViews;

	uint32 nColors;
	uint32 ofsColors;

	uint32 nTextures;
	uint32 ofsTextures;

	uint32 nTransparency; // H
	uint32 ofsTransparency;
	uint32 nI;   // always unused ?
	uint32 ofsI;
	uint32 nTexAnims;	// J
	uint32 ofsTexAnims;
	uint32 nK;
	uint32 ofsK;

	uint32 nTexFlags;
	uint32 ofsTexFlags;
	uint32 nY;
	uint32 ofsY;

	uint32 nTexLookup;
	uint32 ofsTexLookup;

	uint32 nTexUnitLookup;		// L
	uint32 ofsTexUnitLookup;
	uint32 nTransparencyLookup; // M
	uint32 ofsTransparencyLookup;
	uint32 nTexAnimLookup;
	uint32 ofsTexAnimLookup;

	float floats[14];

	uint32 nBoundingTriangles;
	uint32 ofsBoundingTriangles;
	uint32 nBoundingVertices;
	uint32 ofsBoundingVertices;
	uint32 nBoundingNormals;
	uint32 ofsBoundingNormals;

	uint32 nO;
	uint32 ofsO;
	uint32 nP;
	uint32 ofsP;
	uint32 nQ;
	uint32 ofsQ;
	uint32 nLights; // R
	uint32 ofsLights;
	uint32 nCameras; // S
	uint32 ofsCameras;
	uint32 nT;
	uint32 ofsT;
	uint32 nRibbonEmitters; // U
	uint32 ofsRibbonEmitters;
	uint32 nParticleEmitters; // V
	uint32 ofsParticleEmitters;

};

// block B - animations
struct ModelAnimation {
	uint32 animID;
	uint32 timeStart;
	uint32 timeEnd;

	float moveSpeed;

	uint32 loopType;
	uint32 flags;
	uint32 d1;
	uint32 d2;
	uint32 playSpeed;  // note: this can't be play speed because it's 0 for some models

	Vec3D boxA, boxB;
	float rad;

	int16 s[2];
};


// sub-block in block E - animation data
struct AnimationBlock {
	int16 type;		// interpolation type (0=none, 1=linear, 2=hermite)
	int16 seq;		// global sequence id or -1
	uint32 nRanges;
	uint32 ofsRanges;
	uint32 nTimes;
	uint32 ofsTimes;
	uint32 nKeys;
	uint32 ofsKeys;
};

// block E - bones
struct ModelBoneDef {
	int32 animid;
	int32 flags;
	int16 parent; // parent bone index
	int16 geoid;
	AnimationBlock translation;
	AnimationBlock rotation;
	AnimationBlock scaling;
	Vec3D pivot;
};

struct ModelTexAnimDef {
	AnimationBlock trans, rot, scale;
};

struct ModelVertex {
	Vec3D pos;
	uint8 weights[4];
	uint8 bones[4];
	Vec3D normal;
	Vec2D texcoords;
	int unk1, unk2; // always 0,0 so this is probably unused
};

struct ModelView {
    uint32 nIndex, ofsIndex; // Vertices in this model (index into vertices[])
    uint32 nTris, ofsTris;	 // indices
    uint32 nProps, ofsProps; // additional vtx properties
    uint32 nSub, ofsSub;	 // materials/renderops/submeshes
    uint32 nTex, ofsTex;	 // material properties/textures
	int32 lod;				 // LOD bias?
};


/// One material + render operation
struct ModelGeoset {
	uint16 d1;		// mesh part id?
	uint16 d2;		// ?
	uint16 vstart;	// first vertex
	uint16 vcount;	// num vertices
	uint16 istart;	// first index
	uint16 icount;	// num indices
	uint16 d3;		// number of bone indices
	uint16 d4;		// offset into bone index list
	uint16 d5;		// ?
	uint16 d6;		// root bone?
	Vec3D v;
};

/// A texture unit (sub of material)
struct ModelTexUnit{
	// probably the texture units
	// size always >=number of materials it seems
	uint16 flags;		// Flags
	uint16 order;		// ?
	uint16 op;			// Material this texture is part of (index into mat)
	uint16 op2;			// Always same as above?
	int16 colorIndex;	// color or -1
	uint16 flagsIndex;	// more flags...
	uint16 texunit;		// Texture unit (0 or 1)
	uint16 d4;			// ? (seems to be always 1)
	uint16 textureid;	// Texture id (index into global texture list)
	uint16 texunit2;	// copy of texture unit value?
	uint16 transid;		// transparency id (index into transparency list)
	uint16 texanimid;	// texture animation id
};

// block X - render flags
struct ModelRenderFlags {
	uint16 flags;
	uint16 blend;
};

// block G - color defs
struct ModelColorDef {
	AnimationBlock color;
	AnimationBlock opacity;
};

// block H - transp defs
struct ModelTransDef {
	AnimationBlock trans;
};

struct ModelTextureDef {
	uint32 type;
	uint32 flags;
	uint32 nameLen;
	uint32 nameOfs;
};

struct ModelLightDef {
	int16 type;
	int16 bone;
	Vec3D pos;
	AnimationBlock ambColor;
	AnimationBlock ambIntensity;
	AnimationBlock color;
	AnimationBlock intensity;
	AnimationBlock attStart;
	AnimationBlock attEnd;
	AnimationBlock unk1;
};

struct ModelCameraDef {
	int32 id;
	float fov, farclip, nearclip;
	AnimationBlock transPos;
	Vec3D pos;
	AnimationBlock transTarget;
	Vec3D target;
	AnimationBlock rot;
};


struct ModelParticleParams {
	float mid;
	uint32 colors[3];
	float sizes[3];
	int16 d[10];
	float unk[3];
	float scales[3];
	float slowdown;
	float rotation;
	float f2[16];
};

struct ModelParticleEmitterDef {
    int32 id;
	int32 flags;
	Vec3D pos;
	int16 bone;
	int16 texture;
	int32 nZero1;
	int32 ofsZero1;
	int32 nZero2;
	int32 ofsZero2;
	int16 blend;
	int16 type;
	int16 s1;
	int16 s2;
	int16 cols;
	int16 rows;
	AnimationBlock params[10];
	ModelParticleParams p;
	AnimationBlock unk;
};


struct ModelRibbonEmitterDef {
	int32 id;
	int32 bone;
	Vec3D pos;
	int32 nTextures;
	int32 ofsTextures;
	int32 nUnknown;
	int32 ofsUnknown;
	AnimationBlock color;
	AnimationBlock opacity;
	AnimationBlock above;
	AnimationBlock below;
	float res, length, unk;
	int16 s1, s2;
	AnimationBlock unk1;
	AnimationBlock unk2;
};


#pragma pack(pop)


#endif
```

# 2.x

The following changes occurred from 1.x to 2.x:

- `uint16`, `int16` changed from `short` to `__int16`.
- `uint32`, `int32` changed from `int` to `__int32`.
- `Vertext` struct added.
- `CharModelDetails` struct added.
- `ModelHeader` struct renames:
	- `nK` -> `nTexReplace`.
	- `ofsK` -> `ofsTexReplace`.
	- `nO` -> `nAttachements`.
	- `ofsO` -> `ofsAttachements`.
	- `nP` -> `nAttachLookup`.
	- `osfP` -> `ofsAttachLookup`.
- New int added to the bone definitions in the `ModelBoneDef` struct: `int32 unknown`.
- `ModelGeoset` struct `d1` -> `id`.
- `ModelRenderFlags` struct new values (commented out):
	- `unsigned char f1`
	- `unsigned char f2`
- `ModelParticalParams` struct additions:
	- `float unknown`
	- `float Rot1[3]` - Model Rotation 1
	- `float Rot2[3]` - Model Rotation 2
	- `float Trans[3]` - Model Translastion
- `ModelParticleEmitterDef` struct renames:
	- `nZero1` -> `nModelName`.
	- `ofsZero1` -> `ofsModelName`.
	- `unk` -> `en`.
- `ModelBlockQ` struct added.
- `ModelAttachmentDef` struct added.

```cpp
#ifndef MODELHEADERS_H
#define MODELHEADERS_H

typedef unsigned char uint8;
typedef char int8;
typedef unsigned __int16 uint16;
typedef __int16 int16;
typedef unsigned __int32 uint32;
typedef __int32 int32;

#pragma pack(push,1)

struct Vertex {
    float tu, tv;
    float x, y, z;
};

struct CharModelDetails {
	bool closeRHand;
	bool closeLHand;

	bool isChar;
	bool isMounted;

	void Reset() {
		closeRHand = false;
		closeLHand = false;
		isChar = false;
		isMounted = false;
	}
};

struct ModelHeader {
	char id[4];
	uint8 version[4];
	uint32 nameLength;
	uint32 nameOfs;
	uint32 type;

	uint32 nGlobalSequences;
	uint32 ofsGlobalSequences;
	uint32 nAnimations;
	uint32 ofsAnimations;
	uint32 nC;
	uint32 ofsC;
	uint32 nD;
	uint32 ofsD;
	uint32 nBones;
	uint32 ofsBones;
	uint32 nF;
	uint32 ofsF;

	uint32 nVertices;
	uint32 ofsVertices;
	uint32 nViews;
	uint32 ofsViews;

	uint32 nColors;
	uint32 ofsColors;

	uint32 nTextures;
	uint32 ofsTextures;

	uint32 nTransparency; // H
	uint32 ofsTransparency;
	uint32 nI;   // always unused ?
	uint32 ofsI;
	uint32 nTexAnims;	// J
	uint32 ofsTexAnims;
	uint32 nTexReplace;
	uint32 ofsTexReplace;

	uint32 nTexFlags;
	uint32 ofsTexFlags;
	uint32 nY;
	uint32 ofsY;

	uint32 nTexLookup;
	uint32 ofsTexLookup;

	uint32 nTexUnitLookup;		// L
	uint32 ofsTexUnitLookup;
	uint32 nTransparencyLookup; // M
	uint32 ofsTransparencyLookup;
	uint32 nTexAnimLookup;
	uint32 ofsTexAnimLookup;

	float floats[14];

	uint32 nBoundingTriangles;
	uint32 ofsBoundingTriangles;
	uint32 nBoundingVertices;
	uint32 ofsBoundingVertices;
	uint32 nBoundingNormals;
	uint32 ofsBoundingNormals;

	uint32 nAttachments; // O
	uint32 ofsAttachments;
	uint32 nAttachLookup; // P
	uint32 ofsAttachLookup;
	uint32 nQ; // Q
	uint32 ofsQ;
	uint32 nLights; // R
	uint32 ofsLights;
	uint32 nCameras; // S
	uint32 ofsCameras;
	uint32 nT;
	uint32 ofsT;
	uint32 nRibbonEmitters; // U
	uint32 ofsRibbonEmitters;
	uint32 nParticleEmitters; // V
	uint32 ofsParticleEmitters;

};

// block B - animations
struct ModelAnimation {
	uint32 animID;
	uint32 timeStart;
	uint32 timeEnd;

	float moveSpeed;

	uint32 loopType;
	uint32 flags;
	uint32 d1;
	uint32 d2;
	uint32 playSpeed;  // note: this can't be play speed because it's 0 for some models

	Vec3D boxA, boxB;
	float rad;

	int16 s[2];
};


// sub-block in block E - animation data
struct AnimationBlock {
	int16 type;		// interpolation type (0=none, 1=linear, 2=hermite)
	int16 seq;		// global sequence id or -1
	uint32 nRanges;
	uint32 ofsRanges;
	uint32 nTimes;
	uint32 ofsTimes;
	uint32 nKeys;
	uint32 ofsKeys;
};

// block E - bones
struct ModelBoneDef {
	int32 animid;
	int32 flags;
	int16 parent; // parent bone index
	int16 geoid;
	// new int added to the bone definitions.  Added in WoW 2.0
	int32 unknown;
	AnimationBlock translation;
	AnimationBlock rotation;
	AnimationBlock scaling;
	Vec3D pivot;
};

struct ModelTexAnimDef {
	AnimationBlock trans, rot, scale;
};

struct ModelVertex {
	Vec3D pos;
	uint8 weights[4];
	uint8 bones[4];
	Vec3D normal;
	Vec2D texcoords;
	int unk1, unk2; // always 0,0 so this is probably unused
};

struct ModelView {
    uint32 nIndex, ofsIndex; // Vertices in this model (index into vertices[])
    uint32 nTris, ofsTris;	 // indices
    uint32 nProps, ofsProps; // additional vtx properties
    uint32 nSub, ofsSub;	 // materials/renderops/submeshes
    uint32 nTex, ofsTex;	 // material properties/textures
	int32 lod;				 // LOD bias?
};


/// One material + render operation
struct ModelGeoset {
	uint16 id;		// mesh part id?
	uint16 d2;		// ?
	uint16 vstart;	// first vertex
	uint16 vcount;	// num vertices
	uint16 istart;	// first index
	uint16 icount;	// num indices
	uint16 d3;		// number of bone indices
	uint16 d4;		// ? always 1 to 4
	uint16 d5;		// ?
	uint16 d6;		// root bone?
	Vec3D v;
	float unknown[4];	// Added in WoW 2.0?
};

/// A texture unit (sub of material)
struct ModelTexUnit{
	// probably the texture units
	// size always >=number of materials it seems
	uint16 flags;		// Flags
	uint16 order;		// ?
	uint16 op;			// Material this texture is part of (index into mat)
	uint16 op2;			// Always same as above?
	int16 colorIndex;	// color or -1
	uint16 flagsIndex;	// more flags...
	uint16 texunit;		// Texture unit (0 or 1)
	uint16 d4;			// ? (seems to be always 1)
	uint16 textureid;	// Texture id (index into global texture list)
	uint16 texunit2;	// copy of texture unit value?
	uint16 transid;		// transparency id (index into transparency list)
	uint16 texanimid;	// texture animation id
};

// block X - render flags
struct ModelRenderFlags {
	uint16 flags;
	//unsigned char f1;
	//unsigned char f2;
	uint16 blend;
};

// block G - color defs
struct ModelColorDef {
	AnimationBlock color;
	AnimationBlock opacity;
};

// block H - transp defs
struct ModelTransDef {
	AnimationBlock trans;
};

struct ModelTextureDef {
	uint32 type;
	uint32 flags;
	uint32 nameLen;
	uint32 nameOfs;
};

struct ModelLightDef {
	int16 type;
	int16 bone;
	Vec3D pos;
	AnimationBlock ambColor;
	AnimationBlock ambIntensity;
	AnimationBlock color;
	AnimationBlock intensity;
	AnimationBlock attStart;
	AnimationBlock attEnd;
	AnimationBlock unk1;
};

struct ModelCameraDef {
	int32 id;
	float fov, farclip, nearclip;
	AnimationBlock transPos;
	Vec3D pos;
	AnimationBlock transTarget;
	Vec3D target;
	AnimationBlock rot;
};


struct ModelParticleParams {
	float mid;
	uint32 colors[3];
	float sizes[3];
	int16 d[10];
	float unk[3];
	float scales[3];
	float slowdown;
	float rotation;	//Sprite Rotation
	float unknown;
	float Rot1[3];	//Model Rotation 1
	float Rot2[3];	//Model Rotation 2
	float Trans[3];	//Model Translation
	float f2[6];
};

struct ModelParticleEmitterDef {
    int32 id;
	int32 flags;
	Vec3D pos;
	int16 bone;
	int16 texture;
	int32 nModelName;
	int32 ofsModelName;
	int32 nZero2;
	int32 ofsZero2;
	int16 blend;
	int16 type;
	int16 s1;
	int16 s2;
	int16 cols;
	int16 rows;
	AnimationBlock params[10];
	ModelParticleParams p;
	AnimationBlock en;
};


struct ModelRibbonEmitterDef {
	int32 id;
	int32 bone;
	Vec3D pos;
	int32 nTextures;
	int32 ofsTextures;
	int32 nUnknown;
	int32 ofsUnknown;
	AnimationBlock color;
	AnimationBlock opacity;
	AnimationBlock above;
	AnimationBlock below;
	float res, length, unk;
	int16 s1, s2;
	AnimationBlock unk1;
	AnimationBlock unk2;
};



struct ModelBlockQ {
	char id[4];
	int32 dbid;
	int32 bone;
	Vec3D pos;
	int16 type;
	int16 seq;
	uint32 nRanges;
	uint32 ofsRanges;
	uint32 nTimes;
	uint32 ofsTimes;
};


struct ModelAttachmentDef {
	int32 id;
	int32 bone;
	Vec3D pos;
	AnimationBlock unk;
};




#pragma pack(pop)


#endif
```

# 3.x

The following changes occurred from 2.x to 3.x:

- `uint16`, `int16` changed from `__int16` to `short`.
- `uint32`, `int32` changed from `__int32` to `int`.
- `ModelGeoSet` struct moved.
- `ModelBoneDef` struct moved.
- `AnimationBlock` struct moved.
- Additional `ModelTextureDef` struct added, contains only `char fake[16]`.

```cpp
#ifndef MODELHEADERS2_H
#define MODELHEADERS2_H

typedef unsigned char uint8;
typedef char int8;
typedef unsigned short uint16;
typedef short int16;
typedef unsigned int uint32;
typedef int int32;

struct AnimationBlock {
	int16 type;		// interpolation type (0=none, 1=linear, 2=hermite)
	int16 seq;		// global sequence id or -1
	uint32 nRanges;
	uint32 ofsRanges;
	uint32 nTimes;
	uint32 ofsTimes;
	uint32 nKeys;
	uint32 ofsKeys;
};

#pragma pack(push,1)

struct Vertex {
	float tu, tv;
	float x, y, z;
};

struct CharModelDetails {
	bool closeRHand;
	bool closeLHand;

	bool isChar;
	bool isMounted;

	void Reset() {
		closeRHand = false;
		closeLHand = false;
		isChar = false;
		isMounted = false;
	}
};

struct ModelHeader {
	char id[4];
	uint8 version[4];
	uint32 nameLength;
	uint32 nameOfs;
	uint32 type;

	uint32 nGlobalSequences;
	uint32 ofsGlobalSequences;
	uint32 nAnimations;
	uint32 ofsAnimations;
	uint32 nC;
	uint32 ofsC;
	uint32 nD;
	uint32 ofsD;
	uint32 nBones;
	uint32 ofsBones;
	uint32 nF;
	uint32 ofsF;

	uint32 nVertices;
	uint32 ofsVertices;
	uint32 nViews;
	uint32 ofsViews;

	uint32 nColors;
	uint32 ofsColors;

	uint32 nTextures;
	uint32 ofsTextures;	

	uint32 nTransparency;
	uint32 ofsTransparency;
	uint32 nI;  
	uint32 ofsI;
	uint32 nTexAnims;	
	uint32 ofsTexAnims;	
	uint32 nTexReplace;
	uint32 ofsTexReplace;

	uint32 nTexFlags;
	uint32 ofsTexFlags;
	uint32 nY;
	uint32 ofsY;	

	uint32 nTexLookup;
	uint32 ofsTexLookup;	

	uint32 nTexUnitLookup;		
	uint32 ofsTexUnitLookup;	
	uint32 nTransparencyLookup; 
	uint32 ofsTransparencyLookup;	
	uint32 nTexAnimLookup;
	uint32 ofsTexAnimLookup;	

	float floats[14];

	uint32 nBoundingTriangles;
	uint32 ofsBoundingTriangles;	
	uint32 nBoundingVertices;
	uint32 ofsBoundingVertices;		
	uint32 nBoundingNormals;
	uint32 ofsBoundingNormals;		

	uint32 nAttachments;
	uint32 ofsAttachments;		
	uint32 nAttachLookup; 		
	uint32 ofsAttachLookup;		
	uint32 nQ; 
	uint32 ofsQ;				
	uint32 nLights; 
	uint32 ofsLights;			
	uint32 nCameras;
	uint32 ofsCameras;			
	uint32 nT;					
	uint32 ofsT;				
	uint32 nRibbonEmitters;
	uint32 ofsRibbonEmitters;	
	uint32 nParticleEmitters; 
	uint32 ofsParticleEmitters;	

};


struct ModelGeoset {
	uint16 id;		// mesh part id?
	uint16 d2;		// ?
	uint16 vstart;	// first vertex
	uint16 vcount;	// num vertices
	uint16 istart;	// first index
	uint16 icount;	// num indices
	uint16 d3;		// number of bone indices
	uint16 d4;		// ? always 1 to 4
	uint16 d5;		// ?
	uint16 d6;		// root bone?
	Vec3D v;
	float unknown[4];	// Added in WoW 2.0?
};

struct ModelBoneDef {
	int32 animid;
	int32 flags;
	int16 parent; // parent bone index
	int16 geoid;
	// new int added to the bone definitions.  Added in WoW 2.0
	int32 unknown;
	AnimationBlock translation;
	AnimationBlock rotation;
	AnimationBlock scaling;
	Vec3D pivot;
};

// block B - animations
struct ModelAnimation {
	uint32 animID;
	uint32 timeStart;
	uint32 timeEnd;

	float moveSpeed;

	uint32 loopType;
	uint32 flags;
	uint32 d1;
	uint32 d2;
	uint32 playSpeed;  // note: this can't be play speed because it's 0 for some models

	Vec3D boxA, boxB;
	float rad;

	int16 s[2];
};

struct ModelTexAnimDef {
	AnimationBlock trans, rot, scale;
};

struct ModelVertex {
	Vec3D pos;
	uint8 weights[4];
	uint8 bones[4];
	Vec3D normal;
	Vec2D texcoords;
	int unk1, unk2; // always 0,0 so this is probably unused
};

struct ModelView {
	uint32 nIndex, ofsIndex; // Vertices in this model (index into vertices[])
	uint32 nTris, ofsTris;	 // indices
	uint32 nProps, ofsProps; // additional vtx properties
	uint32 nSub, ofsSub;	 // materials/renderops/submeshes
	uint32 nTex, ofsTex;	 // material properties/textures
	int32 lod;				 // LOD bias?
};


/// A texture unit (sub of material)
struct ModelTexUnit{
	// probably the texture units
	// size always >=number of materials it seems
	uint16 flags;		// Flags
	uint16 order;		// ?
	uint16 op;			// Material this texture is part of (index into mat)
	uint16 op2;			// Always same as above?
	int16 colorIndex;	// color or -1
	uint16 flagsIndex;	// more flags...
	uint16 texunit;		// Texture unit (0 or 1)
	uint16 d4;			// ? (seems to be always 1)
	uint16 textureid;	// Texture id (index into global texture list)
	uint16 texunit2;	// copy of texture unit value?
	uint16 transid;		// transparency id (index into transparency list)
	uint16 texanimid;	// texture animation id
};

// block X - render flags
struct ModelRenderFlags {
	uint16 flags;
	//unsigned char f1;
	//unsigned char f2;
	uint16 blend;
};

// block G - color defs
struct ModelColorDef {
	AnimationBlock color;
	AnimationBlock opacity;
};

// block H - transp defs
struct ModelTransDef {
	AnimationBlock trans;
};

struct ModelTextureDef {
	uint32 type;
	uint32 flags;
	uint32 nameLen;
	uint32 nameOfs;
}; 

struct ModelTextureDef {
	char fake[16];
};

struct ModelLightDef {
	int16 type;
	int16 bone;
	Vec3D pos;
	AnimationBlock ambColor;
	AnimationBlock ambIntensity;
	AnimationBlock color;
	AnimationBlock intensity;
	AnimationBlock attStart;
	AnimationBlock attEnd;
	AnimationBlock unk1;
};

struct ModelCameraDef {
	int32 id;
	float fov, farclip, nearclip;
	AnimationBlock transPos;
	Vec3D pos;
	AnimationBlock transTarget;
	Vec3D target;
	AnimationBlock rot;
};


struct ModelParticleParams {
	float mid;
	uint32 colors[3];
	float sizes[3];
	int16 d[10];
	float unk[3];
	float scales[3];
	float slowdown;
	float rotation;	//Sprite Rotation
	float unknown;
	float Rot1[3];	//Model Rotation 1
	float Rot2[3];	//Model Rotation 2
	float Trans[3];	//Model Translation
	float f2[6];
};

struct ModelParticleEmitterDef {
	int32 id;
	int32 flags;
	Vec3D pos;
	int16 bone;
	int16 texture;
	int32 nModelName;
	int32 ofsModelName;
	int32 nZero2;
	int32 ofsZero2;
	int16 blend;
	int16 type;
	int16 s1;
	int16 s2;
	int16 cols;
	int16 rows;
	AnimationBlock params[10];
	ModelParticleParams p;
	AnimationBlock en;
};


struct ModelRibbonEmitterDef {
	int32 id;
	int32 bone;
	Vec3D pos;
	int32 nTextures;
	int32 ofsTextures;
	int32 nUnknown;
	int32 ofsUnknown;
	AnimationBlock color;
	AnimationBlock opacity;
	AnimationBlock above;
	AnimationBlock below;
	float res, length, unk;
	int16 s1, s2;
	AnimationBlock unk1;
	AnimationBlock unk2;
};



struct ModelBlockQ {
	char id[4];
	int32 dbid;
	int32 bone;
	Vec3D pos;
	int16 type;
	int16 seq;
	uint32 nRanges;
	uint32 ofsRanges;
	uint32 nTimes;
	uint32 ofsTimes;
};


struct ModelAttachmentDef {
	int32 id;
	int32 bone;
	Vec3D pos;
	AnimationBlock unk;
};




#pragma pack(pop)


#endif

```

# Cryects Model Headers

These are included only for legacy purposes, and are identical to the 1.x headers.

```cpp
#ifndef MODELHEADERS_H
#define MODELHEADERS_H

typedef unsigned char uint8;
typedef char int8;
typedef unsigned short uint16;
typedef short int16;
typedef unsigned int uint32;
typedef int int32;

#pragma pack(push,1)

struct ModelHeader {
	char id[4];
	uint8 version[4];
	uint32 nameLength;
	uint32 nameOfs;
	uint32 type;

	uint32 nGlobalSequences;
	uint32 ofsGlobalSequences;
	uint32 nAnimations;
	uint32 ofsAnimations;
	uint32 nC;
	uint32 ofsC;
	uint32 nD;
	uint32 ofsD;
	uint32 nBones;
	uint32 ofsBones;
	uint32 nF;
	uint32 ofsF;

	uint32 nVertices;
	uint32 ofsVertices;
	uint32 nViews;
	uint32 ofsViews;

	uint32 nColors;
	uint32 ofsColors;

	uint32 nTextures;
	uint32 ofsTextures;

	uint32 nTransparency; // H
	uint32 ofsTransparency;
	uint32 nI;   // always unused ?
	uint32 ofsI;
	uint32 nTexAnims;	// J
	uint32 ofsTexAnims;
	uint32 nK;
	uint32 ofsK;

	uint32 nTexFlags;
	uint32 ofsTexFlags;
	uint32 nY;
	uint32 ofsY;

	uint32 nTexLookup;
	uint32 ofsTexLookup;

	uint32 nTexUnitLookup;		// L
	uint32 ofsTexUnitLookup;
	uint32 nTransparencyLookup; // M
	uint32 ofsTransparencyLookup;
	uint32 nTexAnimLookup;
	uint32 ofsTexAnimLookup;

	float floats[14];

	uint32 nBoundingTriangles;
	uint32 ofsBoundingTriangles;
	uint32 nBoundingVertices;
	uint32 ofsBoundingVertices;
	uint32 nBoundingNormals;
	uint32 ofsBoundingNormals;

	uint32 nO;
	uint32 ofsO;
	uint32 nP;
	uint32 ofsP;
	uint32 nQ;
	uint32 ofsQ;
	uint32 nLights; // R
	uint32 ofsLights;
	uint32 nCameras; // S
	uint32 ofsCameras;
	uint32 nT;
	uint32 ofsT;
	uint32 nRibbonEmitters; // U
	uint32 ofsRibbonEmitters;
	uint32 nParticleEmitters; // V
	uint32 ofsParticleEmitters;

};

// block B - animations
struct ModelAnimation {
	uint32 animID;
	uint32 timeStart;
	uint32 timeEnd;

	float moveSpeed;

	uint32 loopType;
	uint32 flags;
	uint32 d1;
	uint32 d2;
	uint32 playSpeed;  // note: this can't be play speed because it's 0 for some models

	Vec3D boxA, boxB;
	float rad;

	int16 s[2];
};


// sub-block in block E - animation data
struct AnimationBlock {
	int16 type;		// interpolation type (0=none, 1=linear, 2=hermite)
	int16 seq;		// global sequence id or -1
	uint32 nRanges;
	uint32 ofsRanges;
	uint32 nTimes;
	uint32 ofsTimes;
	uint32 nKeys;
	uint32 ofsKeys;
};

// block E - bones
struct ModelBoneDef {
	int32 animid;
	int32 flags;
	int16 parent; // parent bone index
	int16 geoid;
	AnimationBlock translation;
	AnimationBlock rotation;
	AnimationBlock scaling;
	Vec3D pivot;
};

struct ModelTexAnimDef {
	AnimationBlock trans, rot, scale;
};

struct ModelVertex {
	Vec3D pos;
	uint8 weights[4];
	uint8 bones[4];
	Vec3D normal;
	Vec2D texcoords;
	int unk1, unk2; // always 0,0 so this is probably unused
};

struct ModelView {
    uint32 nIndex, ofsIndex; // Vertices in this model (index into vertices[])
    uint32 nTris, ofsTris;	 // indices
    uint32 nProps, ofsProps; // additional vtx properties
    uint32 nSub, ofsSub;	 // materials/renderops/submeshes
    uint32 nTex, ofsTex;	 // material properties/textures
	int32 lod;				 // LOD bias?
};


/// One material + render operation
struct ModelGeoset {
	uint16 d1;		// mesh part id?
	uint16 d2;		// ?
	uint16 vstart;	// first vertex
	uint16 vcount;	// num vertices
	uint16 istart;	// first index
	uint16 icount;	// num indices
	uint16 d3;		// number of bone indices
	uint16 d4;		// offset into bone index list
	uint16 d5;		// ?
	uint16 d6;		// root bone?
	Vec3D v;
};

/// A texture unit (sub of material)
struct ModelTexUnit{
	// probably the texture units
	// size always >=number of materials it seems
	uint16 flags;		// Flags
	uint16 order;		// ?
	uint16 op;			// Material this texture is part of (index into mat)
	uint16 op2;			// Always same as above?
	int16 colorIndex;	// color or -1
	uint16 flagsIndex;	// more flags...
	uint16 texunit;		// Texture unit (0 or 1)
	uint16 d4;			// ? (seems to be always 1)
	uint16 textureid;	// Texture id (index into global texture list)
	uint16 texunit2;	// copy of texture unit value?
	uint16 transid;		// transparency id (index into transparency list)
	uint16 texanimid;	// texture animation id
};

// block X - render flags
struct ModelRenderFlags {
	uint16 flags;
	uint16 blend;
};

// block G - color defs
struct ModelColorDef {
	AnimationBlock color;
	AnimationBlock opacity;
};

// block H - transp defs
struct ModelTransDef {
	AnimationBlock trans;
};

struct ModelTextureDef {
	uint32 type;
	uint32 flags;
	uint32 nameLen;
	uint32 nameOfs;
};

struct ModelLightDef {
	int16 type;
	int16 bone;
	Vec3D pos;
	AnimationBlock ambColor;
	AnimationBlock ambIntensity;
	AnimationBlock color;
	AnimationBlock intensity;
	AnimationBlock attStart;
	AnimationBlock attEnd;
	AnimationBlock unk1;
};

struct ModelCameraDef {
	int32 id;
	float fov, farclip, nearclip;
	AnimationBlock transPos;
	Vec3D pos;
	AnimationBlock transTarget;
	Vec3D target;
	AnimationBlock rot;
};


struct ModelParticleParams {
	float mid;
	uint32 colors[3];
	float sizes[3];
	int16 d[10];
	float unk[3];
	float scales[3];
	float slowdown;
	float rotation;
	float f2[16];
};

struct ModelParticleEmitterDef {
    int32 id;
	int32 flags;
	Vec3D pos;
	int16 bone;
	int16 texture;
	int32 nZero1;
	int32 ofsZero1;
	int32 nZero2;
	int32 ofsZero2;
	int16 blend;
	int16 type;
	int16 s1;
	int16 s2;
	int16 cols;
	int16 rows;
	AnimationBlock params[10];
	ModelParticleParams p;
	AnimationBlock unk;
};


struct ModelRibbonEmitterDef {
	int32 id;
	int32 bone;
	Vec3D pos;
	int32 nTextures;
	int32 ofsTextures;
	int32 nUnknown;
	int32 ofsUnknown;
	AnimationBlock color;
	AnimationBlock opacity;
	AnimationBlock above;
	AnimationBlock below;
	float res, length, unk;
	int16 s1, s2;
	AnimationBlock unk1;
	AnimationBlock unk2;
};


#pragma pack(pop)


#endif
```

# Fake Model Headers

Likely this was used between 1.x and 2.x, lots of unknown elements that would eventually be defined.

```cpp
#ifndef FAKEHEADERS_H
#define FAKEHEADERS_H

typedef unsigned char uint8;
typedef char int8;
typedef unsigned short uint16;
typedef short int16;
typedef unsigned int uint32;
typedef int int32;

#pragma pack(push,1)

struct ModelHeader {
	char id[4];
	uint8 version[4];
	uint32 nameLength;
	uint32 nameOfs; // <<
	uint32 type;

	uint32 nGlobalSequences;
	uint32 ofsGlobalSequences; // <<
	uint32 nAnimations;
	uint32 ofsAnimations; // <<
	uint32 nC;
	uint32 ofsC; // <<
	uint32 nD;
	uint32 ofsD; // <<
	uint32 nBones;             // !!!!!!!!!
	uint32 ofsBones; // <<     // !!!!!!!!!
	uint32 nF;
	uint32 ofs1; // <<

	uint32 nVertices;
	uint32 ofs2; // <<
	uint32 nViews;
	uint32 ofs3; // <<

	uint32 nColors;
	uint32 ofs4; // <<

	uint32 nTextures;
	uint32 ofs5; // <<

	uint32 nTransparency; 
	uint32 ofs6; // <<
	uint32 nI;  
	uint32 ofs7; // <<
	uint32 nTexAnims;
	uint32 ofs8; // <<
	uint32 nTexReplace;
	uint32 ofs9; // <<

	uint32 nTexFlags;
	uint32 ofs10; // <<
	uint32 nY;
	uint32 ofs11; // <<

	uint32 nTexLookup;
	uint32 ofs12; // <<

	uint32 nTexUnitLookup;
	uint32 ofs13; // <<
	uint32 nTransparencyLookup;
	uint32 ofs14; // <<
	uint32 nTexAnimLookup;
	uint32 ofs15; // <<

	float floats[14];

	uint32 nBoundingTriangles;
	uint32 ofs16; // <<
	uint32 nBoundingVertices;
	uint32 ofs17; // <<
	uint32 nBoundingNormals;
	uint32 ofs18; // <<

	uint32 nAttachments;
	uint32 ofs19; // <<
	uint32 nAttachLookup;
	uint32 ofs20; // <<
	uint32 nQ;
	uint32 ofs21; // <<
	uint32 nLights;
	uint32 ofs22; // <<
	uint32 nCameras; 
	uint32 ofs23; // <<
	uint32 nT;
	uint32 ofs24; // <<
	uint32 nRibbonEmitters; 
	uint32 ofs25; // <<
	uint32 nParticleEmitters;
	uint32 ofs26; // <<

};

// FAKES!!


struct ModelGeoset1 {
	char fake[24];
};

struct ModelGeoset2 {
	char fake[24];
	float unknown[4];
};

struct ModelBoneDef1 {
	char fake1[12];
	char fake2[92];
};

struct ModelBoneDef2 {
	char fake1[12];
	int32 unknown;
	char fake2[92];
};

struct ModelView {
    char fake[44];
};

/*

struct ModelAnimation {
    char fake[68];
};

struct ModelTexAnimDef {
    char fake[84];
};

struct ModelVertex {
	Vec3D pos;
	uint8 weights[4];
	uint8 bones[4];
	Vec3D normal;
	Vec2D texcoords;
	int unk1, unk2;
};
*/
/*
struct ModelTexUnit{
    char fake[24];
};

struct ModelRenderFlags {
    char fake[4];
};

struct ModelColorDef {
    char fake[56];
};

struct ModelTransDef {
    char fake[28];
};

struct ModelTextureDef {
    char fake[16];
};

struct ModelLightDef {
    char fake[212];
};

struct ModelCameraDef {
    char fake[124];
};

struct ModelParticleParams {
    char fake[152];
};

struct ModelParticleEmitterDef {
    char fake[504];
};

struct ModelRibbonEmitterDef {
    char fake[220];
};

struct ModelBlockQ {
	char id[44];
};

struct ModelAttachmentDef {
	char fake[48];
};*/

#pragma pack(pop)

#endif
```