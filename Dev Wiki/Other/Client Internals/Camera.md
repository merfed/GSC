_Sync'd to version from 20 May 2014._

The camera memory block is longer than documented here however im not sure where it ends. The first 4 Z,X,Y,Z apears later again in a "unchangeable" format (for refrence or config?). These offets are the only visible changeable values in the block.

# Static Offset

Data For 2.4.1 // 2008 By Malu05

```
Static Offset for Camera (level 2 pointer): 
Level 1 = 0x00DD8FB4
Level 2 + 0x732C
CamZ is located 0x100 over Level 2
```

# Camera Offsets

_Memory CameraBlock by By Malu05_

```
Offset	Type	Description		Aditional Details
0x8	Float	Camera X
0xC	Float	Camera Y
0x10	Float	Camera Z
0x84	int(8)	GUID			The GUID that the camera will follow. Is used when using Mindvision, Eyes of the Beast etc.
0xC4	Float	View 2 Distance
0xC8	Float	View 2 Altitude
0xCC	Float	View 2 Latitude
0xD0	Float	View 3 Distance
0xD4	Float	View 3 Altitude
0xD8	Float	View 3 Latitude
0xDC	Float	View 4 Distance
0xE0	Float	View 4 Altitude
0xE4	Float	View 4 Latitude
0xE8	Float	View 5 Distance
0xEC	Float	View 5 Altitude
0xF0	Float	View 5 Latitude
0X10C	Float	Camera Distance
0x110	float	RotX
0x114	float	RotY    
0x118	float	RotZ       
0x11C	float?	UpdownX			(Ignores Colission) (From $val to $start)      
0x120	float?	YawCam       
0x124	float?	UpdownZ      
0x128	int?	ForcedReturn   
0x12C	float	FOV			(Field Of View)   
0x130	float?	UpdownX 		(Accepts Colission) (From $val to $start)   
0x134		??
0x138		??   
0x13C		??   
0x140		??   
0x144	float?	DownUpX 		(Ignores Colission) (From $start to $val)
0x148		??
0x14C		??
0x150	int?	Scroll Smoothing	(Freezing this value makes the scroll Zooming "laggy")
0x154	int?	Scroll Zoom in 		(Freezing this value makes the scroll Zooming-in instantly "x to min")
0x158	int?	Scroll Zoom out 	(Freezing this value makes the scroll Zooming-out instantly "x to max")
0x15C		??
0x160		??
0x164		??
0x168		??
0x16C		??
0x170	int?	?? 			(reletated to scrolling)
0x174	int?	?? 			(reletated to scrolling)
```

# Camera by kynox

```
class CCamera
{
public:
	virtual void function0(); //
	virtual void function1(); //
	virtual void function2(); //
	virtual void function3(); //
	char unknown4[4]; //0x0004
	idVec3 vecPos; //0x0008          This is just a normal 3D Vector, X,Y,Z
	idMat3 vecViewMatrix; //0x0014   This is a 3x3 Matrix. 9 floats
	float ID02621370; //0x0038  
	float ID025E7F40; //0x003C  
	float fFov; //0x0040  
};
```