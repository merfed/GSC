- **Author**: Jb55 (Darshu/Azgalor)

# How To

## Version 1.x

1. First start by extracting wdbtocsv.exe into your `World of Warcraft\WDB` folder.
2. Drag and Drop any WDB file onto `wdbtocsv.exe` to convert it into a csv file, or click `doallwdb.bat`.
3. Open the CSV with Excel or another CSV viewer.
4. Enjoy!

## Version 2.x

### .exe version

   1. Extract the contents of the `\exe` folder into your `\World of Warcraft\Cache\WDB\enUS` folder 
   	  (enUS may be different depending on your locale)
   2. Drag and drop any WDB file onto `wdbtocsv.exe` to convert it into a csv file, or click `doallwdb.bat` to convert them all.
   
### .py version

   1. Download python, [psyco](http://psyco.sourceforge.net/) and [pyyaml](http://pyyaml.org/wiki/PyYAML) if you haven't already
   2. Extract the contents of the `\py` folder into your `\World of Warcraft\Cache\WDB\enUS` folder
   3. Run the python script with the wdb files as its arguments (multiple arguments work)

# Notes

## Bitmask Fields

> [!Note] Bitmask Fields
> **Version 1.2**
> The large bitmask fields do not appear properly in Excel, to get around this select the
bitmask's column, right-click and choose "Format Cells...". Select Number from the list
and set it to 0 decimal places. Bitmask32 fields should now look correct.
> 
>  **Version 1.3**
>  I decided to disable them for now, the routines I was using was not showing the full bitmask. I also found it
a hassle to view bitmasks within excel/calc so I changed all bitmask fields to unsigned ints.

> [!Note] wdb.yaml
> **Version 2.0**
> Field definitions can now be modified by editing this file. Make sure it is in the same directory as wdbtocsv.


# Changelog

- **Version 2.0** - July 19, 2008
	* `wdbtocsv` has been completely rewritten in Python.
	* Added: Fields can be defined manually in `wdb.yaml`, open it up in your favourite text editor to make changes to broken definitions
	* Fixed: Will report an error when the record's defined size and actual size are different
	* Fixed: Definitions are updated and should work with the latest version of World of Warcraft (as of today)
- **Version 1.5** - March 21, 2007
	* Fixed: Removed auto detection of rows, it was unreliable.
- **Version 1.3** - December 15, 2006
	* Fixed: Updated to the current definitions
	* Fixed: Made it easier to update defintions in the source
	* Fixed: A bug in the bitmask routines
	* Added: Added support for the Burning Crusade in the source, the BC binary will be release seperatly until expansion hits.
- **Version 1.2** - August 4, 2006
	* Added: Linux binary
	* Added: doallwdb.bat which converts all known wdb files into csv
	* Removed: 'press any key to continue', allowing batch jobs
	* Fixed: Bitmask bugs
	* Fixed: Bugs when parsing certain line feeds
	* Fixed: Giving incorrect readout of parsed records
	* Updated: Field definitions
- **Version 1.1** - June 27, 2006
	- Fixed: Excel errors when opening some WDB files
	* Fixed: Crashes when loading `questcache.wdb`
- **Version 1.0** - June 27, 2006
	- Initial Release

# Source

The source code included is released under the GNU GPL license (license.txt). It was written in C++ and compiled with MSVC++.

# doallwdb.bat

```
wdbtocsv.exe creaturecache.wdb
wdbtocsv.exe gameobjectcache.wdb
wdbtocsv.exe itemcache.wdb
wdbtocsv.exe itemnamecache.wdb
wdbtocsv.exe itemtextcache.wdb
wdbtocsv.exe npccache.wdb
wdbtocsv.exe pagetextcache.wdb
wdbtocsv.exe questcache.wdb
wdbtocsv.exe wowcache.wdb
```

# Versions

| Name       | Filesize                         | Author | Source ? | Notes                            |
| ---------- | -------------------------------- | ------ | -------- | -------------------------------- |
| wdbtocsv   | 20 KB (Source)<br/>176 KB (exe)  | JB55   | ✔️       | v1.1                             |
| wdbtocsv   | 20 KB (Source)<br/>100 KB (exe)  | JB55   | ✔️       | v1.2                             |
| wdbtocsv   | 21 KB (Source)<br/>100 KB (exe)  | JB55   | ✔️       | v1.3                             |
| wdbtocsvBC | 21 KB (Source)<br/>100 KB (exe)  | JB55   | ✔️       | v1.3 <span class="bc">BC</span>  |
| wdbtocsv   | 21 KB (Source)<br/>160 KB (exe)  | JB55   | ✔️       | v1.31                            |
| wdbtocsvBC | 21 KB (Source)<br/>165 KB (exe)  | JB55   | ✔️       | v1.31 <span class="bc">BC</span> |
| wdbtocsv   | 21 KB (Source)<br/>168 KB (exe)  | JB55   | ✔️       | v1.5                             |
| wdbtocsv   | 13.8 KB (Source)<br/>22 KB (exe) | JB55   | ✔️       | v2.0                                 |
