- **Author**: urbz
- **Syntax**:

WoWmapview is a 3D map viewer for World of Warcraft. It uses the data files included with the game to display the 3D game world, which you can explore by flying anywhere. It allows access to off-limits developer areas and unfinished instance maps.

The reverse engineering of the game data files is a work in progress, so obviously the viewer is neither perfect nor complete, and definitely not optimized.

# Requirements

Since I'm not as qualified of a programmer as the professionals at Blizzard, this map viewer is not really geared towards being fast or efficient. The WoW client does a good job of determining what is and isn't visible, and only showing a small subset at a time - WoWmapview loads larger map chunks at once, and caches the recent areas, so there are small delays as new map areas are loaded. And of course, loading all this stuff makes it fairly memory-hungry.

- WoW Client

**v0.7.1b**:
- Complete WoTLK install (Background downloader will need to complete)
- OpenGL combatible graphics card

# Usage

Run `wowmapview.exe` to start it in the default settings: 1024x768 fullscreen. Run `windowed.cmd` to start it in windowed mode without opening a command line.

In the main menu, you can select a world on the left or choose one of the bookmarked locations available.
Click on the map to enter the world in the given location. For worlds without maps, click anywhere to enter.

You can always exit back to the main menu with the Esc key; pressing Esc at the main menu will exit the program.

Navigating the game world is done using the mouse and the keyboard: use the mouse to look around, press I to invert the vertical axis.

You can fly forward and backwards using the W and S keys, and strafe left and right with A and D. 

A description of further key commands is available in the main menu.

## Command Line Parameters

| Parameter    | Result               |
| ------------ | -------------------- |
| `-w`         | Windowed Mode        |
| `-f`         | Fullscreen Mode      |
| `-p`         | Use `patch.mpq`      |
| `-np`        | Omit `patch.mpq`     |
| `-1280x1024` | Different resolution |

# Changelog

- **v0.7.1b**:
	- Wrath Maps
	- Copy private server co-ordinates to clipboard
	- All MapID's listed for each map
	- Missing starting bacgrounds
	- Menu format changed
	- Map ID's displayed for selected maps
	- Map listings hidden to give clear view of maps on smaller resolutions
	- Copy functionality added for teleport co-ordinates
- **v0.5**:
	- **Terrain/outdoor**:
		- added fog (F to toggle)
		- added light colors
		- added lowres terrain/some LOD for fogged mode
		- fixed liquid colors/extents
	- **WMOs**:
		- added fog
		- added liquids
	- **Models**:
		- added particle and ribbon effects
- **v0.4**:
	- **Terrain**:
		- Rewritten rendering code to use index buffers
		- Fixed textures a bit
		- Added shadow maps
		- Added high-resolution tesselation, press H to return to the lowres height maps
		- Added support for animated ground textures, like flowing lava (not 100% correct)
		- Fixed holes in the terrain, now the ground doesn't stick into map objects like buildings and caves
	- **WMOs**:
		- Fixed indoor lighting
		- Some minor tweaks
	- **Models**:
		- Added support for skeletal animation
		- Texture animation	(lava flows, waterfalls)
		- Some fixes to transparency etc. (still far from perfect)
	- **Misc**:
		- Changed MPQ library to libmpq, since SFMPQ was closed source
		- Added support for patch.mpq
- **v0.3**:
	- initial public release

# Known Issues

- **v0.7.1b**:
	- Northrend terrain does not render alpha effects
	- Some Northrend water missing
- **v0.5**:
	- secondary water color is missing
	- outdoor fog not complete
	- indoor fog too dense when viewed from a distance
	- lighting is still not 100% correct
	- transparent polygons aren't depth-sorted; this means that there might be some artifacts around partially transparent objects like tree leaves.
	- slowdown in some areas like outside Stormwind or the Undercity
	- as the program loads new areas of the map it will cause short pauses :(
	- still eats a lot of RAM


# Notes

- **Version 0.7.1 Beta**
	- Notes it was based on [WoW Map Viewer 0.5](http://wotlk-beta.be)
	- Due to numerous file format changes in WotLK some effects are currently disabled.

# Versions

| Name    | Filesize                            | Author | Source ? | Notes |
| ------- | ----------------------------------- | ------ | -------- | ----- |
| 0.3     | 185 KB (Source)<br />108 MB (exe)   |        | ✔️       |       |
| 0.4     | 758 KB (Source)<br />184 MB (exe)   |        | ✔️       |       |
| 0.5     | 819 KB (Source)<br />228 MB (exe)   |        | ✔️       |       |
| 0.6 wip | 4.37 (Source)                       |        | ❌       |       |
| 0.6     | 4.37 MB (Source)<br />232 KB (exe)  |        | ✔️       |       |
| 0.6 r90 | 292 KB (exe)                        |        | ❌       |       |
| 0.6.1   | 232 KB (exe)                        |        | ❌       |       |
| 0.6.2   | 236 KB (exe)                        |        | ❌       |       |
| 0.7.1   | 408 KB (exe)                        |        | ❌       |       |
| 0.7.1b  | 408 KB (exe)                        |        | ❌       |       |
| 0.7 r12 | 653 KB (exe)                        |        | ❌       |       |

# Links

- [Sourceforge](https://wowmapview.sourceforge.net/)