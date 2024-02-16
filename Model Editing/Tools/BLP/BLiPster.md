- **Author**: Aieny Celenovia, saluce65 (WoWInterface)
- **Syntax**:
- **AKA**: BLPConverterGUI

This program is a graphical converter for Blizzard’s proprietary BLP format to Portable Network Graphics (PNG). The front end (the Graphical User Interface) was designed by Aieny Celenovia. On the back-end is Patrick Cyr’s BLPConverter command-line program.

I’ve done my best to maintain as much of the functionality of his converter as I can while adding to the overall program. To that end, nearly every switch for that program is available as an option in this GUI. One notable exception is the Multifile switch. To speed the batch conversion of files, I opted instead to run a separate thread for each file being converted and running the BLPConverter program under that thread for that specific file (using the same settings for each thread).

# Compiling the Source Code

The GUI was written under C# using Windows Presentation Foundation (WPF). The solution file for the source code is for Visual Studio C# 2010, which can be downloaded free of charge from Microsoft at [http://www.microsoft.com/express/](http://www.microsoft.com/express/). Due to licensing restrictions, the RibbonControl library is not included in the source code but can be obtained for free from [http://msdn.microsoft.com/en-us/office/aa973809.aspx](http://msdn.microsoft.com/en-us/office/aa973809.aspx) and selecting [License the Office UI](https://profile.microsoft.com/RegSysProfileCenter/wizard.aspx?wizid=5fed1051-2e7b-4049-8177-0fdaae5f475c&lcid=1033).

Patrick Cyr’s source code is included with this program in the BLPConverter_8_1 folder. According to the BLPConverter.rtf file, to use that source code, you must obtain:

- _palbmp_: A pallete library (C) Charles Bloom. ([http://www.cbloom.com](http://www.cbloom.com/)) I'm opting to comply with section 0 of the Bloom Public License: I'm distributing this program using the GPL. I've also made some very small changes to it: I commented out the stderr spam.
- _crblib_: Another library (C) Charles Bloom, which is a dependency of palbmp.
- _libpng_: The offical PNG reference library. ([http://www.libpng.org/](http://www.libpng.org/))
- _squish_: A DXT compression library. ([http://www.sjbrown.co.uk/?code=squish](http://www.sjbrown.co.uk/?code=squish))

# How to Use This Program

Most of the GUI should be self-explanatory. Files are loaded using the “Add Files” button on the Application Menu Tab. Any number of files can be selected and added to the conversion queue (hold the control or shift key while clicking to select multiple files). Once you have queued the files you want to convert, click the “Convert” button on the Application Menu Tab. All files will be converted according to the designated rules and saved into the same folder as the original file.

## Conversion Rules

A series of default conversion rules are set up in the BLPConverter command-line program. Those rules can be viewed by clicking on the “Conversion Rules” button under the Conversion Tab. If you desire to set up your own conversion rules, use the “Custom Conversion” button. Custom rules appear under the “Conversion Rules” button as _italicized_, **bolded** entries in the list; the overridden rule appears greyed out.

Selecting the “Character Texture” option will output palletized BLPs with no alpha channels, the required settings for character skins. Selecting the “Clothing Texture” option will output palletized BLPs with alpha channels, which, as the name implies, is the required format for clothing skins. These settings are mutually exclusive, so only one can be enabled at a time.

## For More Information

For more information about Patrick Cyr’s BLPConverter program, see the BLPConverter.rtf file in the source code directory.

# Compatibility

This program was written for Windows 7 but it fully compatible with Vista and XP SP3. Under XP, the window may appear slightly different than the typical Luna window scheme. Unfortunately, the RibbonControl Window has to approximate the Windows XP chrome. This is especially apparent when using the Silver color scheme, as the window appears a dull gray rather than silvery. Under Windows Vista and 7, the window utilized the Aero theme if enabled on your computer.

# WoWInterface Version Readme

Trying to figure out an easy way to convert Blizzard's BLP files to something more manageable but can't find the right program? Tired of trying to use command-line utilities in a graphical interface world? Look no longer!

BLiPster is a Windows-based Graphical User Interface (GUI) to convert Blizzard's BLP files to Portable Network Graphic (PNG) image files. Utilizing Dandelion's BLPConverter command-line program, this stand-alone utility focuses on giving you, the user, complete control over the conversion process. This multi-threaded application will batch convert BLPs in seconds.

The source code for this program is included in the file. Read the BLPConverterGUI.rtf file for more information (especially since one of the important dll's could not be included with the source code due to licensing restrictions). The program requires .NET 4.0 framework; if the installer does not detect the framework, it will give you the option of downloading and installing the framework from Microsoft.

# Versions

| Name            | Filesize | Author          | Source ? | Notes              |
| --------------- | -------- | --------------- | -------- | ------------------ |
| BLPConverterGUI | 261 KB   | Aieny Celenovia | ✔️       | Unknown Version    |
| BLPConverterGUI |          | Aieny Celenovia | ✔️       | 0.1 *WoWInterface* |

- The *WoWInterface* version is **not** actually version `0.1`, it's just what it's tagged on *WoWInterface*. This *may* be older than the **Unknown Version** BLiPster since the souce is considerably different, and features and installer.

## Links

* [WoW Interface](http://www.wowinterface.com/downloads/info17616-0.1.html)