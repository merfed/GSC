# Required Files

- WoW.Export Tool

# Blender Configuration

1. Download [THIS](https://download.blender.org/release/Blender2.79/blender-2.79-windows64.msi) Blender version
2. Download Blender Add-On
3. Open Blender
4. Select File -> User Preferences... -> Add-Ons -> Install Add-On from File
5. Search for your Blender Add-On
6. Select the .ZIP File (do not unpack/unzip) -> Install Add-On from File
7. Tick the Box -> Save User Setttings

**Optional**:

- If Blender then shows you the list of many Add-Ons, then Search for "Import-Export: WoW Tools"

# Download M2Mod

1. Download [M2Mod 9.0](https://bitbucket.org/suncurio/m2mod/downloads/)
2. Download latest Listfile.csv from [Wow.Tools](https://wow.tools/casc/listfile/download/csv)
3. Put M2Mod into a folder of your liking
4. Create a folder called "Mappings" inside the M2Mod folder
5. Put the listfile.csv File in there

## Convert .m2 into .m2i

1. Export your .m2 from wow.export
2. Open M2Mod
3. Go to "M2 -> M2I"
4. Select your .m2 as the "Source M2"
5. Hit "Go!"

Converting should go without error.

## Edit M2I in Blender

1. Open Blender (if closed)
2. Go to File -> Import -> "M2 Intermediate (.m2i)
3. Select your converted M2I
4. Once Imported, Delete the Cube (if it's there) by right-click -> delete (or X -> delete)
5. Press "A" until every texture glows Orange
6. In the top-right corner you see a Box with "Armature" -> Open
7. Delete every Mesh, except for those you want to have in-game (i'll be doing Gloves)
8. If there is only one Mesh left, that are your Gloves -> Press "TAB"
9. The gloves should be yellow-ish
10. Right-Click on them to make them both grey
11. Hold "L" on one of the gloves to make their parts yellow-ish again
12. Press "X" and select "Only Edges and Faces"
13. Do that until **only** one glove is left.

> [!important] Important
> Before exporting, make sure you press TAB again to go out of the Edit mode. Else your export will fail.

14. Click on File -> Export -> "M2 Intermediate (.m2i)
15. Name it something like you did (example: collections_mail_maldraxxus_d_01_hu_m_LAL.m2i) LAL= Lower Arm (glove) + L (Left)

# Convert back to .m2 -> TXID + MultiConvert

1. Open M2Mod
2. Go to -> "M2I->M2"
3. Select SOURCE **M2I** -> Use your exported Blender M2I
4. First "Preload" then "Go!"
5. If you changed your .m2 name, differently than it's original, you also have to name the .SKIN files accordingly.
- original .m2 = collections_mail_maldraxxus_d_01_hu_m.m2
- edited   .m2 = collections_mail_maldraxxus_d_01_hu_m_gloves_lal.m2 => change .Skin files to "collections_mail_maldraxxus_d_01_hu_m_gloves_lal_lod00.skin"
5. Open [TXID](https://github.com/Intemporel/FixTXID/releases)
6. Put your .m2 with all the Files that came with it in there and hit "FIX", no error should pop out
7. Use [MultiConvert](https://model-changing.net/index.php?app=downloads&module=downloads&controller=view&id=62) in the same way as TXID, no error should pop out

# Create a Database

Create new Database in Heidisql

1. Connect to your database
2. Right-click on the very first Table in heidisql (mine is Acore) -> New -> New Database -> name it something you like -> OK

# Create a Spell

Create Spell in [Stoneharry's Spell Editor](https://github.com/stoneharry/WoW-Spell-Editor/releases/download/v2.0.3/WoW_Spell_Editor_v2_0_3.exe)

1. Open the Spell Editor
2. Fill everything out and when it asks which Database to use, enter your custom name created in heidisql
3. Click on "Import/Export" and then wait until everything is loaded -> hit "Import"
4. Click on "New Spell" -> 71589 -> 90000 (unique Spell ID)
5. Scroll all the way down to your spell and edit the name.
6. Go to "Visual" then "Kits & Effects"  and copy the "StateKit" AND the "Back Attachment" (you can copy them both at the same time)
7. Go back to "Base" -> Set "Spell Visual 1:" to 0
8. Back to "Visual" then "Kits & Effects" -> Right-Click on the first Box -> Paste -> select StateKit -> Confirm Paste
9. On the second Box, do the same
6. Hit "Save Visual Modifications" (dont forget to set all the offsets to 0)

# Open Heidisql

1. Go into your new created Database
2. Scroll down to "spellvisualeffectname"
3. Scroll to the very first Entry -> (normally 7101) and change the name to whatever you like
4. FilePath is where the .m2 is located (usually) `item\objectcomponents\collectionscollections_mail_maldraxxus_d_01_hu_m `

**NOTE**: change the file ending to .mdx instead of .m2 in spellvisualeffectname

5. Save

# Open Spell Editor again

1. Go to your Spell
2. Go to "Visual" then "Kits & Effects"
3. If it changed it automatically to your new entry in heidisql then -> "Save Visual Modifications" -> "Import/Export" -> "Export", wait a second or two, then export all the files it *automatically* selected
4. Go into the Export folder of your Spell Editor
5. Copy all .dbc files from there into your WoWServer's dbc files (mine is in `E:\WowServer\data\dbc`"

# Create a patch

1. Go into your wow\data\ folder and create a new *folder* called "patch-b.mpq"
2. In `wow\data\patch-b.mpq\` paste the contents of **CHARACTER.rar** folder in there it's for the new attachments we are using
2. In the folder, create another folder called "DBFilesClient" <- Copy and Paste all your .dbc files from your Export in there
3. Create another folder in `wow\data\patch-b.mpq\` called "item", in item create a new folder "objectcomponents" and in THAT folder create another folder called "collections"
4. Put your converted .m2 files in `wow\data\patch-b.mpq\item\objectcomponents\collections\`

# Start the Game 

1. Type .aura 90000
2. Be disappointed because it's a white Texture
3. Close the game

# 010 Editor + M2 Template

1. Open 010 Editor
2. Click on "Templates"
3. Click on "View Installed Templates"
4. Click on the Right on "Add"
5. Select your M2Alastor.bt File -> OK

It should now appear when you are clicking on "Templates" as "M2 Blizzard"

6. Either open your .m2 manually with 010 Editor or double-click on your .m2 and "Open With 010 Editor" -> Always open with 010 Editor
7. Once opened run the "M2 Blizzard" Template
8. Scroll all the way to te Bottom of the Code
9. If the line there doesnt end with "00 00 00" etc, just manually add them until you get to a new Line
10. Type in the Box to the right of the Code "`item\objectcomponents\collections\collections_mail_maldraxxus_d_01_renown.blp`" or whatever your .blp is called
11. Select the entirety of your text and at the bottom should be a Number: "Sel: 77[XX]"
12. Now open the "struct M2_file"
13. Scroll all the way down to "struct_Textures"
14. Then "struct Textures_Textures[0] (struct Textures_Textures[0] if there is no hardcoded texture already)
15. in "uint32 FileName_length" we set it to our Sel Number (it was 77)
16. Now we select our text once again, but this time we press CTRL+SHIFT+A
17. A small window at the bottom appears and we just copy the "Start:" Value
18. Paste the "Start" value into "uint32 FileName_offset"

Now CTRL+S or save manually

If you opened your .m2 from your patch folder, there is no need to replace anything, but if you opened it from your wow.export folder, then you have to replace it in your patch

Now your texture should have it's appropiate texture

19. Open spellvisualmodelattach
20. Copy and Paste the last Line
21. Change ID, Parentspellvisual, Spellvisualeffect to 90000
22. Change AttachmentID to either ONE of the following:

```
50 = ?
53 = belt
51  = right feet
55 = left feet
54 = lower Arm right
58 = lower Arm left
59 = upper chest (neck)
56 = lower leg right
52 = lower leg left
57 = ?
```

23. Change it to 58, cuz that's what we are using
24. Save

orginal name + Txid -> Multiconverter = good
change only at beginning of file (chest_collections) + txid -> Multiconverter = good

if u scroll to here subzskribe to mai chanel plz

# Video

- [Video](https://www.youtube.com/watch?v=GTWTzD_q30U)

# Original Credits

- **Author**: Tyrallis
- [Model Changing](https://model-changing.net/index.php?app=tutorials&module=tutorials&controller=view&id=158)