- **Author**: Zezula
- **Syntax**:

*This may have been the original name of CASC View.*

Since 2014, Blizzard Entertainment has changed data format in their games from MPQ to CASC (Content Addressable Storage Container). A library that can parse the storages can be downloaded from Github.

## Extracting data from Casc Storage

The CascView tool is available for World of Warcraft - Warlords of Draenor, Heroes of the Storm and Diablo III. 

## Why can't I see all files in WoW storage?

Unlike old MPQ archives, CASC storage for World of Warcraft does NOT hold file names (Diablo III and Heroes of the Storm do). For extracting World of Warcraft files, you need to use a listfile. You can download one here. Note that the listfile is incomplete for current WoW builds and I have no plans to fill in the missing files.

## What about Overwatch?

Support on Overwatch is in early stage. Based on how I have time and information about how to extract files, I'll add the support there. At the moment, CascLib is able to extract most files by their encoding key.

## What files and directories form a CASC storage?

When browsing the data subdirectory in the game directory, you may notice several files in various subdirectories. There are data files in the "data" subdirectory that contain the files. However, unlike MPQs, the data files are not standalone archives. You need the complete storage directory with several extra files to make CascView open the storage and extract files from it. The following list contains the complete list of files and directories that you need to preserve in order to be able to extract files:

* The entire data subdirectory ("Data", "BNTData" or "HeroesData", whichever is present)
* Make sure that the "config" subdirectory under data folder is present
* The ".build.info" file
* The ".build.db" file, if there is no ".build.info"

## How to open CASC storage with CascView?

When opening a game storage directory, you can either enter the storage at the command line or select "File\Open Storage" in the application UI. To open the storage, you either select a game directory or one of the storage subdirectories (no matter how deep). Examples:

	CascView.exe "c:\Games\Diablo III"
	CascView.exe "C:\Games\Heroes of the Storm\HeroesData"
	CascView.exe "C:\Games\World of Warcraft\Data"
	CascView.exe "C:\Games\Overwatch\data\casc\config\66\77"

# Versions

| Name | Filesize | Author | Source ? | Notes |
| ---- | -------- | ------ | -------- | ----- |
|      |          |        |          |       |

## Links
* [Github](https://github.com/ladislav-zezula/CascLib)
* [Website](http://www.zezula.net/cz/casc/main.html)