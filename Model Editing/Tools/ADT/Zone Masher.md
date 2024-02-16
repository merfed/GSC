- **Author**: Riu (Ryan Cornwall)
- **Syntax**:

What it does: This application allows you to select multiple ADT files (and/or folders containing ADT files) and "mash" or combine them into one giant map. Here's an example: Eastern Kingdoms and Kalimdor are two separate continents. With this application, you can combine them into one continent. This application can also create WDT files automatically from a group of ADT files, so no more having to manually edit a WDT (the program also contains a small "database" that's hardcoded, which checks for the new map name when setting flags in the WDT) file.

# Features

1. Automatic offset fixing.
2. Automatic WDT generation.
3. The ability to choose which options you want to enable.
4. Move ADT files around. For example, you could move Azeroth so that Stormwind's location is now the location of Westfall.
5. Combine ADT files into the same map. You can put things like Azeroth and Kalimdor together, or replace Warsong Gulch with a giant pool of water.
6. Change the Z-Offset of the entire map. I'm hoping this will be used for things other than just exploiting...　A value of -2 to -3 will put you below the view of other players on the map.
7. Change WMO X, Y, and Z offsets. This allows you to do such things as hide world map objects or move them in some way that would give you an unfair advantage. For example, I used this in conjunction with the Z-Offset to lower my Warsong Gulch so that I'm underneath the land, but still able to grab the flag and turn it in. I'm sure this could also be used for exploiting bosses, accessing places that you're not supposed to access, and much, much more.

# Usage

1. Run the program.
2. Click on File -> Add File...
3. Select one or more ADT files, and click on "Open." More ADT files can be loaded in at any time.
4. The ADT files will appear on the 64x64 grid. They will be grouped up (and color-coded) with other ADT files that were selected or added at the same time. Drag the ADT files around the grid until you're comfortable with their arrangement.
5. Add more ADT files as necessary.
6. Make sure that there are NO red-colored ADT files. If there are, that means that one or more ADT files are over-lapping. You will need to move ADT files until there is no more red, or the program will have unexpected results when mashing.
7. Enter a new map name in the "New Map Name" box (e.g. Azeroth). Do not use spaces.
8. Press "Mash!" and wait. Note: Don't use MyWarcraftStudio for very large maps when making a patch, because errors can result (this is not a problem with my program, but a problem with MyWarcraftStudio). I recommend Ladik's MPQ Editor.
9. You will find the new folder in the same directory as the program.

# Troubleshooting

1. "The program won't start, and it says I'm missing DLLs!"
Answer: Make sure that "mingwm10.dll" and "wxmsw28u_gcc.dll" are in the same directory as the application. They are both included in the .7z file. If it is not one of those DLLs, please report it to me and I'll fix it in the next revision (should be within 24-48 hours).
2. "What is a .7z file? I can't open it"
Answer: Make sure you have a file extracting program capable of handling 7-zip archives. If you don't, I really recommend getting 7-Zip. Alternatively, you can download the .zip archive instead.

# Known Issues

1. The dragging refreshes the whole grid. This is due to everything being drawn on a single layer and not marking anything as "dirty." I'll look into fixing this, but it is not a priority of mine.
2. "Mash!" does not check for overlapping ADT files.
3. Sometimes when clicking on one ADT group and dragging it, a different group might move. This is caused by the map overlay matrix being off. I am not yet sure why this is occurring, but it seems to be something to do with opening ADT files on top of another ADT group. Quick fix: Just click somewhere else on the ADT group, or move it out of the way before loading in other ADTs.
4. Modifying the Z-Offset does not adjust water height values. This causes water to be above or below the normal height if it is changed. The reason for this is that water height is typically stored in an array in the MH2O chunk. I might fix this later.
5. Combining Wrath of the Lich King maps with non-Lich King maps seems to cause some major issues. I will look into why this is happening. In the meantime, if you're having issues with strange textures, stay away from Lich King maps (like Northrend). I will be looking into this issue over the next 24 hours to determine a cause (and hopefully a fix). Update: After spending about two minutes, I found the problem. In the WDT file, it turns out that there's one byte that is VERY important. It's a flag, and I had it set for Kalimdor (since I modified Kalimdor). It turns out that the flag determines something about the way the map is set up. I will be adding a few options in a new release to address this issue.

# Changelog

**Edit**: Updated to second release, which contains the following changes:
1. Offset fix has been re-enabled and now works as intended.
2. There are now progress bars for opening files and mashing.
3. Screen refresh times have been greatly reduced, but are still not where I want them.

**Edit**: Updated to third release, which contains the following changes:
1. Added Z-Offset spin control. You can now change the height of ADT files.
2. Fixed the icon. It should no longer break for everyone except me.

**Edit**: Updated to the fourth release, which contains the following changes:
1. Added WMO X, Y, and Z-Offset spin controls. You can now move world map objects separately. This is not needed unless you want to hide world map objects or use it to gain an unfair advantage.

**Edit**: If you would like to see any additions to this program, just reply or send me a private message detailing the change or feature that you would like. If it's reasonable, I'll consider adding it. Please note that I will only accept feature requests that have to deal with ADT, WDT, or WDL files.

# Versions

| Name        | Filesize     | Author | Source ? | Notes |
| ----------- | ------------ | ------ | -------- | ----- |
| Zone Masher | 660 KB (exe) | Riu    | ✔️       | Version `0.0.4.8`, 7/23/2010      |
