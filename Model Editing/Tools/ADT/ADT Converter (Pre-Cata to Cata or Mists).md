- **Authors**: Pagdzin, Mjollnà, feangren

This programs allows conversion for adt pre-Cataclysm to Cataclysm format. Conversion should be ok up to Cataclysm build 11927. This does not include Wow alpha files. World building maps are partly supported (see updates). 

Before launching, open the config file and choose a folder for generated ADTs ("`directory`" parameter). You can also specify a default folder to go when the program opens ("`source_directory`" parameter). Don't bother with debug mode, it just makes the console very talkative :)

The program allows selection of a single file or a whole folder for quick map conversion.

**New**: The ADT Converter is now able to generate the files needed for the MoP client. However keep in mind that ADTs from Vanilla Alpha will not be read by the client, and generate a #132.

# Changelog

**Beta 2013-02-27**
- Generate files needed for MoP client.

**Beta 2011-10-18**
- The collisions problem is still a problem.
- Other quick bugfix with MCSE.
- MCSH fix for some retail adt later edited.

**Beta 2011-09-11**
- Known problem : MCRD/MCRW problem on maps created with Taliis/Noggit (collisions problem on both M2/WMO). Investigating. 
- Support for Cataclysm build 11927.
- Support for maps containing an MH2O created thanks to Gretchin's AllWater Wotlk.

**Beta 2011-08-15**
- Current beta version allows conversion for maps from Wow Beta to 3.3.5 (since ADT format is more or less the same) into 4.x format. It should also work for maps created with Noggit and Taliis, but this probably needs more testing, especially for collisions there's definitely something going wrong.
- WMO now have proper collisions on retail maps. Yay :) 
- Cataclysm build 11927 causes problems. It's going to be fixed.

**Alpha 2011-08-07**
- Conversion ok for Blizzard maps.
- WMO collision has yet to be done.

# Versions

1.1a and 0.1a might be the last two beta's released since they do not have any additional information in the updates section in the readme.

An uncategorized source directory exists, no idea which version this could be.

- 1.1a (have source)
- 0.1a
- Beta 2013-02-27
- Beta 2011-10-18
- Beta 2011-09-11
- Beta 2011-08-15 (Missing)
- Alpha 2011-08-07 (Missing)