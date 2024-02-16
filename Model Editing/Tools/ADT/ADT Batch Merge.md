- **Author**: Michichael Folfsunè
- [Youtube](http://www.youtube.com/user/Michichael)

This script is fairly easy to run. This version requires export of data from Machinima Studios Premium which can no longer be purchased, and does not support WoD. I'm trying to work with the developer of WMV to continue this functionality! If you like this script and find it useful, please consider supporting the development of WMV! We make use of the Model and WMO Placement information, ADT Map tiles and textures, WMO's and their models and the Doodad objects available for export. The script is designed to batch import files that have been batch exported,  using the default names given by Machinima Studios. A detailed tutorial is available on my Youtube page! 

# Bugs

- GM Island will not populate. This is due to the formatting filter. Not sure how to fix it yet.
- Occasionally does not apply the alpha fixup for some FBX imports.
- Some non-maptile objects will show in the selection path. Can't filter them out at this time.

# Changelog

- **v 2.7**
- ***Beta Release***
	- Began fixing up Alphamaps.
	- Added Bump Map support. 
	- While FBX support for WMO's is functioning, no doodads are exported rendering the mode kind of moot. Leaving the functionality in place.
	- Note - an enterprising individual can convert the .obj export in maya (after cleaning it up, without changing the location data) and it can import just fine. I have built support in for this
	- FBX support for doodads is in place, but placement information is radically incorrect. Do not recommend using it (Machinima Studios problem, can't be fixed). 
- **v 2.6** 
- ***NON PRODUCTION USE ONLY***
	- WMO portion re-implemented. Unfortunately, improvements are negligible for obj exports.
	- Added FBX compatibility for the WMO's, performance is significantly increased. Recommend users use FBX exports for WMO's.
	- Fixed FBX Scaling issues. 
	- Beginning clean-up for release. 
	- Fixed non-maptiles displaying in maptile selection box. 
- **v 2.5**
	- ***NON PRODUCTION USE ONLY***
	- Began re-enabling placement of doodads. WMO's continue to be disabled at this time pending further logic. 
	- New logic removes need for ModelID, left it in for compatibility purposes but re-enabled support for older Machinima Studios versions. 
- **v 2.4**
- ***NON PRODUCTION USE ONLY***
	- Moved entire doodad importation section to a staging area to be cloned from. This reduces import times drastically.
	- Multiple logic improvements for file importation to confirm it's successful. 
	- Disabled placement of doodads and WMO's at this time. 
- **v 2.3**
	- ***NON PRODUCTION USE ONLY***
	- Further code cleanups taking place. I'm restructuring.
	- Disabled collection of Undo events. This prevents larger jobs from exhausting system resources. 
	- Since this is a population script, this should have no impact.
- **v 2.2**
- ***NON PRODUCTION USE ONLY***
	- Attempting to use instances to conserve memory and reduce render times, with Lorne's help. 
- **v 2.1**
	- ***NON PRODUCTION USE ONLY***
	- Introduced the ability to import FBX animated files exported from other utilities. 
- **v 2.0** 
	- Production Release with the following improvements. Major thanks to 
	- BC for adding new data to the exports that made this possible:
	-  WMO object deduplication at import stage
	-  Object scaling fixed.
	-  Doodad import speed improved.
	-  Automatic smoothing recalculation to eliminate improper shadows and photometric reactions
	-  Import speed improved for map tiles via viewport modification
	-  Anti-overkill mode implemented, which forces wireframe to prevent systems from running out of memory on large imports
	-  Added options to limit data to be imported: Doodads and WMO's can now selectively be ignored. 
	-  Improved variable cleanup and error handling.
	-  Added automatic alpha fixup. All textures will render with proper mono alpha channeling. 
	-  Adjusted map tile texturing - should come in looking decent. Can always use composite textures if you really want to.
- **v 1.3**
	- Added WMO object imports.
- **v 1.2**
	- Improved upon the Doodad placement and imports. Fixed the positioning errors for objects.
- **v 1.1**
	- Added more graceful imports and Doodad import support.
- **v 1.0**
	- Script modified from BatchMerge v1.5 to handle ADT objects and formats. 

# Versions

- 1.0 (Missing)
- 1.1 (Missing)
- 1.2 (Missing)
- 1.3 (Missing)
- 2.0 (Missing)
- 2.1 (Missing)
- 2.2
- 2.3 (Missing)
- 2.4 (Missing)
- 2.5 (Missing)
- 2.6 (Missing)
- 2.7