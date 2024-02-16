_Sync'd to version from 23 February 2016._

# Static Offset

Static Pointer for M2 Array 1 as for WoW 2.4.1  // 2008 By Malu05

```
0x00CFA874
```

# M2 Offsets 2.4.1

M2Data as for WoW 2.4.1  // 2008 By Malu05

```
**Offset	Type	Description		Aditional Details**
0x0     	= (Always: 9939420 in 3.0.2, seem to be version since 2.4.1 was 9043664) 
0xC	DWORD   = Flags
0x38	float	= Related to X
0x3C	float	= Related to Y
0x40	float	= Related to X
0x44	float	= Related to Y
0x50	float	= Related to X
0x54	float	= Related to Y
0x5c	float	= Related to X
0x60	float	= Related to Y
0x64	float	= Related to Z
0x68	float	= Render X
0x6C	float	= Render Y
0x70	float	= Render Z
0x7C	float	= (Not sure, changes when camera angle changes ;;Cam)
0x84	short   = (This changes to 1 when the object is off the screen;;Cam)
0x94    	= Highlight +
0x98     	= UniqueID
0xAC   DWORD   = NextItem
0xB8	float	= Collision X
0xBC	float	= Collision Y
0xC0	float	= Collision Z
0xC4	float	= Related to X
0xC8	float	= Related to Y
0xD0    	= Stretch_X ;These are used to rotate the model.
0xE0    	= Stretch_Y
0xE4    	= Stretch_Z
0x114	float	= X
0x118	float	= Y
0x11C	float	= Z
0x120	int	= X?! 
```

# M2 Offsets 3.0.9

M2Data as for WoW 3.0.9  

```
**Offset	Type	Description		Aditional Details**
0x0     	= VTable
0x4	int	= entryID?
0x8	int	= flags1
0xC	int	= flags2
0xE	int	= flags3
0x26	short	= isOffScreen
0x28	int	= CounterLifeTimeFrame
0x2C	int	= DistanceFromCamera
0x34	float[3]= RenderPosition
0x98	float	= Gamma
0x9C	int	= UniqueID
0xAC	int	= Pointer_M2Mem
0xC8	float[3]= Collision
0x110	float[3]= Position
```

## Highlight

You can use Highlight+ to highlight models that are selected. Max Highlight is 15.5 so upon selection use:

```
_MemoryWrite("0x" & hex($LightVarInput), $DllInformation, 15.5, 'float')
```

And upon deselection its turned back to the default 0.5

```
_MemoryWrite("0x" & hex($LightdwnVarInput), $DllInformation, 0.5, 'float')
```

0.0 turns the object dark.

## Render X,Y & Z

Render X, Y and Z defines the render position of the object. Normally if you just move the object and the camera leaves the original object position the object stops rendering. Moving Render X,Y and Z along with the object allows you to to extend the render eara to the intire ADT plane.

## UniqueID

The UniqueID is the same as the one stored in the ADT file. This allows you to get info about the object such as filename, MPQ location etc. If anyone was to make a ingame Model tool it would be quite handy to have all relevant MPQ data when selecting a object incase you want to change it. This also allows you to export changes directly into the ADT files after they have been edited ingame.

## Stretch_X

Stretch_X Y and Z seems to be the initiall rotation of a object but im not quite sure how it works. WoWInfinity's squeze function simply turns X and Y 0.00001 making all objects flat.

# Class Definition by kynox

```
class CMapObject
{
public:
	char unknown0[12]; 	//0x0000
	DWORD dwFlags; 		//0x000C  
	char unknown16[92]; 	//0x0010
	idVec3 vecRenderPos; 	//0x006C  
	float ID040D7BC0; 	//0x0078  
	float flDistFromCamera;	//0x007C  Only modified while the object is rendering 
	char unknown128[4]; 	//0x0080
	__int16 IsOffScreen; 	//0x0084  
	char unknown134[14]; 	//0x0086
	float fGamma; 		//0x0094  
	DWORD iUniqueID; 	//0x0098  
	char unknown156[28]; 	//0x009C
 	idVec3 vecBounds[2]; 	//0x00B8  
	idMat4 matProj; 	//0x00D0  Position is the last vector 
	char unknown256[112]; 	//0x0100
}; //Size=0x0170(368)
```