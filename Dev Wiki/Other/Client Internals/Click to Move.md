_Sync'd to version from 6 February 2016._

The click to move function can be used to control your toon with the same funtion as... well.... "Click To Move" (click the ground and your toon walks there). This makes it possible to have wow do all the math for the movement and you just having to put in the commands. Not that the Interaction commands are limited, and that your toon must move before it can interact with a object. The interaction can happen to any object and npc so this can be used in a wide range of scenarios.

So to use click to move put in eighter a GUID or a Position. Then Set the interaction distance Then Set the Action Type After the action type is set your toon will automatically begin to walk

Click to move is also used when following a target. If you put in a NPC GUID into the struc you will be able to follow NPC's or opposite faction alike.

# WoD 17658

 _CTM structure for 17658 by Kruithne_ 
 
```
0x4	TurnScale (AKA speed)
0xC	Distance
0x8C	X
0x1C	Push
0x20	Guid
```

 _CTM Action Types for 17658 by Kruithne_ 
 
```
0x1	LeftClick
0x2	Face		// Turns north
0x3	Stop		// Throws Lua error.
0x4	Move
0x5	NpcInteract
0x6	Loot
0x7	ObjectInteract
0x9	Skin		// Stops moving
0xA	AttackPosition
0xB	AttackGuid
0xC	ConstantFace
0x8	FaceOther	// Turns north and moves forward
0xD	None
```

# Main Offset

```
Current: 3.2.2.10505 (9/22/09) 0x01297920
Legacy:
3.1.3      - 0x011180A0
3.1.0      - 0x1111080
3.0.9.9551 - 0x011F20AC
3.0.3.9183 - 0x011f0ff4
3.0.2.9056 - 0x011EEFDC
```

_Memory Click To Move Block by By Malu05 - 2007_

```
**Offset		Type	Description		Additional Details**
0x0 =		float	?			?
0x4 =		float	TURN_SCALE		Value determining the scale of the turn (only when turning more than 180 degrees?),
0x8 =		float	?			?
0xC = 		float	INTERACTION_DISTANCE	Value determining how far from the targeted position the player should stop.
0x1C = 	INT	ACTION_TYPE		The action trigger. See details about Action Type Below.
0x20 = 	8int	InteractGUID
0x74 =		float	X move to
0x78 =		float	Y move to
0x7C =		float	Z move to
```

## INTERACTION_DISTANCE

```
**Type		Distance**
Travel 		= 0,5
Attack and Loot 	= 3,66666650772095
```

## ACTION_TYPES

```
INT	MoveID 
1 =	Face Target (GUID)
3 =	Stop?
4 =	Walk to Assigned POS
5 =	Move to + Interact (NPC ONLY)
6 =	Loot
7 =	Move to + Interact (OBJECT ONLY)
8 =	Faceother
9 =	Skin
10= 	Attack Assigned POS
11= 	Attack GUID pos?
12= 	Walk + Rotate?
```