wow.export is a node-webkit port of [Marlamin's](https://github.com/Marlamin) [WoW Export Tools](https://github.com/Marlamin/WoWExportTools/) which provides tools for extracting and converting files from the World of Warcraft game client or public CDN servers.

## Features

- Supports both Retail and Classic game clients.
- Complete online support allowing streaming of all files without a client.
- Full 3D preview of both M2 and WMO (doodads included) game models.
- Export into a variety of formats (with more coming soon).
- Overhead map viewer with easy exporting of terrain, textures and objects.
- Includes Blender add-on for advanced map/model importing.
- Preview and export all sound files from the game client.
- Export all video files (cinematics) from the game client.
- Locale support for all 13 languages supported by the client.
- Convert local M2/BLP files by drag-dropping them onto the application.

## Installing

To install wow.export, navigate to the [site](https://www.kruithne.net/wow.export/) and download the latest version. That's it!

> **OSX/Linux**: We are currently not producing builds targeted for non-Windows builds. If you wish to use wow.export on OSX or Linux, you will need to compile your own build from the source. See GH-1 for known issues.

## Updating

When an update to wow.export is available, you will be prompted in the application to update. This process is done entirely automatically once you accept the update!

## Building (Developers Only)

- 🔨 Building wow.export **requires** Node 15.3.0 or above.
- 🧙‍ For building on Windows, [node-gyp prerequisites](https://github.com/nodejs/node-gyp#on-windows) **may** be required.
- 🍷 For building Windows builds on platforms **other** than Windows, Wine 1.6 or above is required.

```
git fetch https://github.com/Kruithne/wow.export.git
npm install

# This will list available builds.
node ./build.js

# This will compile -all- available builds.
node ./build.js *

# Substitute <BUILD> for the build(s) you wish to compile, space-delimitated.
node ./build.js <BUILD1> <BUILD2> ...
```

## Debugging (Developers Only)

> **Note**: Debugging is currently only supported on Windows.

To debug wow.export, compile a `win-x64-debug` build using the build script. This will produce a bare-bones build using the SDK framework and without any production polish. Upon starting the debug version, DevTools will be automatically launched alongside the application.

For the debug build, source code will not be compiled, rather a symlink is created. This means changes to the source code are instantly reflected in the application, simply run `chrome.runtime.reload()` in DevTools console to refresh sources (pressing F5 does not drop references and will lead to memory leaks).

To quickly launch the debug build from the project directory, run `node debug` from your terminal. This will also handle compilation of `.scss` files both on startup and when changes are detected (allowing styling to be hot-reloaded via DevTools).

# Versions

| Version    | Date       | Note                                                |
| ---------- | ---------- | --------------------------------------------------- |
| 0.131      | 04-06-2021 |                                                     |
| 0.132      |            | This build is not available on the Github releases. |
| 0.135      | 30-08-2021 |                                                     |
| 0.136      | 31-08-2021 |                                                     |
| 0.137      | 01-09-2021 |                                                     |
| 0.138      | 13-09-2021 |                                                     |
| 0.139      | 14-09-2021 |                                                     |
| 0.140      |            | This build is not available on the Github releases. |
| 0.143      | 12-03-2022 |                                                     |
| 0.144      | 24-10-2022 |                                                     |
| 0.145      | 22-01-2023 |                                                     |
| 0.146      | 22-01-2023 |                                                     |
| 0.147      | 23-01-2023 |                                                     |
| 0.148      | 10-03-2023 |                                                     |
| 0.149      | 23-05-2023 |                                                     |
| pre-0.2.0k | 29-05-2023 |                                                     |
| 0.150      | 17-08-2023 |                                                     |

# Changelog

0.1.50 (17-08-2023)

- Fixed loading of 10.1.7 installations after Blizzard changed something.

0.1.49 (23-05-2023)

- Added mainline PTR 2 to the product list.
- Added file type detection for .anim (2x), .bls, .tex, .avi and .db2.
- Added exporting of OBJ1/LOD ADT files for raw map exports.
- Fixed an issue that broke unknown file type detection in the raw files tab.
- Fixed an issue where unknown files would fail to export.

0.1.48 (10-03-2023)

- Adds preliminary support for reading DB2 tables in 10.1+.
  
0.1.47 (23-01-2023)

- Fixes an issue with DB2 reading for certain DB2 tables.
  
0.1.46 (22-01-2023)

- Fixes an issue that causes M2 models exported as part of an ADT to have the wrong file extension.
- Removed China as a supported region, as the CDN is no longer available.

0.1.45 (22-01-2023)

- Updated to support World of Warcraft v10.0.5+ and v3.4.1+.
- The "Textures" option for map tile exporting is now enabled by default.
- Improved load times when previewing large WMO models.
- The following breaking changes have been made to raw M2 exporting to keep it consistent with the other export systems:
    - `.skin` files are now named as they appear on the community listfile instead of `{skinName}.skin`. If the fileDataID does not appear on the listfile, `unknown/{fileDataID}.skin` will be used.
    - `.skel` files are now named as they appear on the community listfile instead of `{modelName}.skel`. If the fileDataID does not appear on the listfile, `unknown/{fileDataID}.skel` will be used.
    - `.bone` files are now named as they appear on the community listfile instead of `{modelName}_{X}.bone`. If the fileDataID does not appear on the listfile, `unknown/{fileDataID}.bone` will be used.
    - `.anim` files are now named as they appear on the community listfile instead of `{modelName}{animID}-{animSubID}.anim`. If the fileDataID does not appear on the listfile, `unknown/{fileDataID}.anim` will be used.
    - Raw `.skin`, `.skel`, `.bone` and `.anim` files exported with M2 models now respect the "Enable Shared Children" option and will be exported accordingly.
    - Raw M2 models will now be exported with a manifest file `{modelName}.manifest.json` which contains metadata about any associated files that were exported with it (textures, bones, skins, etc).
- Added ability to export complete ADT tiles as raw client files.
- Fixed issue that prevented unknown sound files from being auto-detected in "Browse Raw Client Files".
- Fixed exporting of WMO MLIQ data.
- Fixed an issue that caused models to export with incorrect names when exporting multiple models at once.
- Fixed issue that would prevent the "Clear Cache" button in settings to work under certain circumstances.
- Fixed various issues that would prevent certain DB2 files from being read.
- Fixed issue that prevented map tile exporting when "Enable Shared Children" is disabled.
- Fixed an issue where strings from decrypted DB2 data could be corrupt.

0.1.44 (24-10-2022)

- Added preview and export support for new texture references used in some Dragonflight WMOs.
- Added expansion icon for Dragonflight.
- Added Classic Era (1.14) to product list.
- Fixed an issue where DB2s could not be exported as raw client files.

0.1.42 (12-03-2022)

- wow.export now has a new website located at [https://www.kruithne.net/wow.export/](https://www.kruithne.net/wow.export/)  
- By default, listfiles will now be downloaded from [https://www.kruithne.net/wow.export/data/listfile/master](https://www.kruithne.net/wow.export/data/listfile/master)  
- By default, TACT encryption keys will now be downloaded from [https://www.kruithne.net/wow.export/data/tact/wow](https://www.kruithne.net/wow.export/data/tact/wow)  
- Files do not exist in the loaded game installation will no longer appear in file lists.

0.1.41 (16-01-2022)

- Added ambientColor field to WMO groups in JSON metadata (MDAL).

0.1.40 (20-10-2021)

- Added vertex colour data to ADT export meta JSON.  
- Added texture height scale/offset to alpha map meta exports.  
- Fixed missing fileDataID column in CSV placement file for ADT exports.  
- Fixed issue that caused missing data in merged alpha map exports.  
- Fixed issue that prevented M2 .skel files from exporting in raw exports.  
- Fixed issue that caused navigation issues from the Blender add-on screen.

0.1.39 (14-09-2021)

- Added option to export M2 bone data into a relative *_bones.json file.
- Added an `exportID` property to `EXPORT_` and `HOOK_EXPORT_COMPLETE` RCP messages.
- M2 models exported with a skin will now be named uniquely based on the selected skin.
- Fixed issue with texture ribbon being overwritten by M2 textures when viewing a WMO.

0.1.38 (13-09-2021)

- Implemented remote control protocol for advanced users.
- Regular expression matching is now case-insensitive.
- Fixed issue that prevented certain models from rendering while the texture ribbon is active.

0.1.37 (01-09-2021)

- Added texture ribbon to the 3D model viewer, allowing inspection of used textures.
- Added ability to copy item names/IDs to the clipboard from the item browser.
- Added ability to view items on Wowhead (external) from the item browser.
- Added button to open maps externally in wow.tools (external) on the map viewer.
- Texture viewer will now export the previewed texture if no user selection has been made.
- Selecting textures/models for an item will now reset the respective filter.
- Consolidated option to view item models/textures into a context menu.
- Removed buttons to toggle sidebar visibility; sidebar is now always visible.
- Changed Discord links in the footer/crash screen to point to new support location.

0.1.36 (31-08-2021)

- Added `colors` property to M2 metadata containing color/alpha timelines for models.
- Added `textureWeights` property to M2 metadata containing global texture transparency timelines for models.
- Added `transparencyLookup` property to M2 metadata for texture unit mapping to transparency entries.
- Added `textureTransforms` property to M2 metadata defining texture animation timelines.
- Added `textureTransformsLookup` property to M2 metadata for texture transform lookups.
- Added `skin.fileName` and `skin.fileDataID` properties to M2 skin metadata.
- Added `boundingBox`, `boundingSphereRadius`, `collisionBox`, `collisionSphereRadius` properties to M2 metadata.
- Added `animFileIDs` property to M2 metadata mapping animation IDs to relative `.anim` files.
- Added option to export all associated raw `.anim` files with M2 models.
- Added option to export liquid (water, lava, etc) data for ADT tiles.

0.1.35 (30-08-2021)

- Fixed issue that caused invalid OBJ files to be produced for M2 collision geometry.
- Added `skin.subMeshes.enabled` property to M2 metadata, indicating which submeshes were exported.
- Added `groups.enabled` property to WMO metadata, indicating which WMO groups were exported.
- Added `textures.fileNameInternal` property to M2 metadata, mapping fileDataID to a listfile entry.
- Added `textures.fileNameExternal` property to M2 metadata, pointing to texture export location (relative to OBJ).
- Added `textures.mtlName` property to M2 metadata, linking to an entry in the MTL file.
- Added `textures` property array to WMO metadata, providing expanded texture mappings.
- Added 'Load Unknown Files' option to toggle loading of unknown files from DB2 tables.
- Added 'Load Model Skins' option to toggle loading of M2 skins for creatures and items.
- Unknown sound files are now listed with the `.unk_sound` extension rather than `.ogg`.
- Unknown sound files are now automatically type-detected on export and given the correct extension.

0.1.34 (24-08-2021)

- Added height textures to ADT alpha map exports, mapped in the metadata layer entries.
- Added effectID (GroundEffectTexture#ID) property to ADT alpha map layer metadata.
- Added advanced foliage meta data exporting (disabled by default).

0.1.33 (13-08-2021)

- Added support for unknown sound files, now listed as "unknown_xxx.ogg".
- Fixed issue that prevented unknown model/textures from appearing in the listfiles.

0.1.32 (28-06-2021)

- Added export/import support for additional UV layers in WMO objects.
- Added export support for additional vertex colour layers in WMO objects.
- Added BLP texture exports for raw WMO files.

# Links

- [Github](https://github.com/Kruithne/wow.export)
- [Website](https://www.kruithne.net/wow.export/)