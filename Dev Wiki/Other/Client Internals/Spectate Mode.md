_Sync'd to version from 20 May 2014._

# Spectate Details

While spectator mode is on the movement keys are being used by the camera so you can't move the player with those. However enabling "click to move" makes it possible to move the player while in spectator mode. You toggle spectate mode in the player flags bitmask by setting both 0x00080000 and 0x00400000. Since this is the "haxor" way of doing it no values for the spectate mode have been set.

The values i reversed for the Machinima tool is:

```
Structure originally by Malu05 2008, updated by NightQuest 2012
**Offset  	Type	Discription			Additional Details**
01174160	float	Yaw
01174164	float	Pitch
01174168	float	Auto Yaw Rotate			(Auto rotate will automatically rotate the camera; 0.01 is nice and slow)
0117416C	float	X
01174170	float	Y
01174174	float	Z
01174178	float	AutoPan X 			(AutoPan will make the camera move automatcically)
0117417C	float	AutoPan Y
01174180	float	AutoPan Z
01174188	int	GUID ;Chasecam steady		(Used to make the camera always face a certain target)
0117418C	int	GUID ;Chasecam steady		(Second one will break the first; essentially just pointing the camera at the target)
01174190	int	GUID ;Chasecam relative		(Relative will follow the target while steady will stay and target)
01174194	int	GUID ;Chasecam relative		(Second one will break the first; essentially just pointing the camera at the target)
0117419C	float	Camera Current Zoom
011741A0	float	Camera Target Zoom
011741A4	float	Camera Movement Speed
011741A8	int	COLLISION ;1/0 switch
```

_When toggleing SpectateMode in WoW machinima Tool, it sets Camera_X,Y and Z to the same position as your char, but with Z + 1_ to mimic the normal camera Z position (not 0)

### Legacy Spectate Offsets

```
"3.3.5.12340", "differenceB2_Spectatorcam", "0x00ACE4B4") ;X Spectate
"3.0.1.8471", "diffrenceB2_Spectatercam", "0x00D9690C") ;X Spectate
"2.4.3.8606", "diffrenceB2_Spectatercam", "0x00CEF474") ;X Spectate
"2.4.2.8278", "diffrenceB2_Spectatercam", "0x00E5A93C") ;X Spectate
"2.4.1.8125", "diffrenceB2_Spectatercam", "0x00e548ec") ;X Spectate
"2.3.3.7799", "diffrenceB2_Spectatercam", "0x00e548ec") ;X Spectate
```