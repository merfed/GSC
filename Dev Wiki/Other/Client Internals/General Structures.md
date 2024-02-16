_Sync'd to version from 20 May 2014._

Here are a few structures you might need if you are going to make a bot or alike. -Malu05

# Macro Structure

```
MacroIndex 		-> Macro1

Macro1 + 0x10 		-> Macro2
Macro1 + 0x20 		= MacroName // Name Given by User
Macro1 + 0x60 		= MacroIcon // Filepath for the icon used in this macro
Macro1 + 0x160 	= MacroBody (Seperated by 0x0A / byte(10) // The macro itself
```

# ActionBar Structure

(the action bars are located in a array with 0 termination)

```
**Offset		Type	Description	Aditional Details**
0x0		BYTE(2)	ID		(Spell ID, MacroID or ItemID)
0x3 		BYTE 	TYPE		(See Types)

**Types (byte):**
0 	= Spell
64 	= General Macro
65 	= Toon Specific Macro
128 	= Item
```