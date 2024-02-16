- **Author**: Patrick Cyr
- **Syntax**: `BLPConverter.exe [options] sourceFile [targetFile]`

This program is very similar to WOWImage (http://www.curse-gaming.com/mod.php?addid=1977) in capability.    The main difference lies in the interface: WOWImage has a drag-and-drop, cross-platform interface, while BLPConverter uses a Windows command line interface which allows it to be incorporated in batch files/scripts.    Also, BLPConverter has a few conversion options available to customize its behavior in ambiguous cases.

An important issue to keep in mind is that for a given texture WoW may only be able to properly display BLPs of a given format.    Your best bet is always to retain the original format when modifying BLPs.

# Getting Started

If you have no idea what the "Command Prompt" is, this section is for you. It is written for Windows XP specifically but should be easily adapted to Vista.

- First, extract BLPConverter.exe from the ZIP file it came in and put it somewhere.
- Next, create a shortcut to it. You can do this by right-clicking on it and selecting "Create Shortcut".
- Right click on the shortcut and select "Properties".
- Somewhere on the Properties dialog there will be an edit box named "Target" that has the path to BLPConverter.exe. After that patch, add "/p /?". It should look something like this: "`C:\MyFiles\BLPConverter.exe /p /?`".
- Run the shortcut and you will see the list of options. You can now see what /p and /? mean: /p is the option that tells the program to pause after it has run (otherwise it just disappears), and /? (not actually listed, I guess) tells it to list the options.
- Close that window and go back to the shortcut's properties. Remove the /? option and save it.
- Drag the shortcut onto Window's Quick Launch toolbar for easy access.
- Using Windows Explorer, find a file you want to convert. Grab it and drag it onto the shortcut you just put on the Quick Launch bar. A window will pop up telling you what format the source file was in and what format of destination file it created. You'll also find that the new file has the same name (though with the opposite extension, of course) and is in the same folder an the source file.

That's pretty much the basics. If you need more control over the formats you can check out the options to see which one(s) will do what you are looking for.

# Controlling Conversion Formats

There are basically 3 ways of controlling conversion formats.

1. If you only want palettized BLP files with no alpha channel (the format required for WoW's character skins), use the /H option. This will guarantee the proper BLP format, and still let you work with RGB PNGs (much easier than working with palettized PNGs).
2. If you only want palettized BLP files but with alpha channel support (the format used for WoW's clothing skins, amongst other things), use the /R option. Again, this lets you work with RGBA PNGs yet create BLPs that WoW likes.
3. If you need more control than that then you need to look at the /L, /U, and /F options. With those you can get complete control over the conversion rules.

# About the -r Option

The trickiest feature of BLPConverter is the -r option.    There is a fundamental problem with these conversions which is that BLPs can handle palettized images with full alpha channels, but no common graphics file formats can.    PNGs can only do 1-bit alpha on palettized images, hence when trying to convert a palettized, 8-bit image to a PNG by default you get a 1-bit alpha PNG.    This default is nice because it preserves the colors, but bad because you lose that extra alpha detail.    This is where the -r option comes in: when the -r option is set BLPConverter will create RGBA PNGs out of palettized, 8-bit BLPs.    This conversion is totally lossless, but there is a catch: if you try to convert the RGBA PNG back to a BLP **without using the -r option** you will wind up with a compressed, non-palettized BLP instead.    WoW doesn't necessarily let you feed it any format you want, so you may well end up with junk on the screen.    (Also note that the palettization done by BLPConverter can be lossy.)    So, the general rule is that if you use the -r option to create a PNG, use it again to remake the BLP.

If the above paragraph was too much, this rule will work 99% of the time: if you are working on clothing textures, always keep the -r option on.    Otherwise, leave it off.

# Usage

```
BLPCONVERTER [options] sourceFile [targetFile]
```

- **sourceFile**: The file to convert.
- **targetFile**: Optionally, the name of the converted file.    If omitted, target file is given the same name as sourceFile but with the opposite extension.

## Options

| Option        | Description                                                                                                                                                                                                                                                                                                                         |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `-p`          | Pause upon completion. (Handy for drag-and-drop operation.)                                                                                                                                                                                                                                                                         |
| `-g (factor)` | (PNG->BLP only) Applies a Gamma factor to the entire image. (factor) is a number between 0.0 and 1.0. If source texture is PNG RGB an alpha channel will be added.                                                                                                                                                                  |
| `-a (value)`  | Sets the Alpha threshold when converting from palettized, 8-bit BLPs to palettized PNGs. Value is a number between 0 and 255. Source alpha values below the threshold are fully transparent, above are fully opaque. Default is 128.                                                                                                |
| `-r`          | `pReserve` alpha. The default conversion from palettized, 8-bit alpha BLPs is to palettized 1-bit alpha PNGs, but when this option is set it will create RGBA PNGs instead. Note that while this will preserve alpha, if you convert it directly back it will not create a BLP of the same format unless you use this option again. |
| `-m`          | Multi-file mode. In this mode, multiple files can be input after options. It is not possible to specify custom output names for them in this mode.                                                                                                                                                                                  |
| `-i`          | Info mode. Only outputs information about the file(s) specified. This option automatically sets the `-v` and `-m` options.                                                                                                                                                                                                          |
| `-c`          | Create mip test image. Outputs an image which contains all of the generated mip levels.                                                                                                                                                                                                                                             |
| `-e`          | Pause on error.                                                                                                                                                                                                                                                                                                                     |
| `-n`          | No mips. No mip levels will be generated when creating a BLP. Note that the game expects mips in certain circumstances. This was mostly added for making interface textures which don't use mip levels smaller.                                                                                                                     |
| `-h`          | Force `cHaracter` texture format (palettized, no alpha) when making BLPs. Incompatible with -r mode.                                                                                                                                                                                                                                                                                                                                    |

# About BLP Files

BLP files are capable of storing data with a few different formats. The primary variables are palettized/RGB and alpha bit depth.    The RGB formats are actually stored using DXT compression (DXT1 for 0-bit alpha and DXT3 for the others), and thus conversion to these formats is somewhat lossy.    Here is a list (with my shorthand for the format in parenthesis):

```
Palettized, 0-bit alpha (P0) - Ex. character skins, clothing.
Palettized, 1-bit alpha (P1) - Ex. clothing (relatively rare).
Palettized, 8-bit alpha (P8) - Ex. clothing.
```

```
RGB, 0-bit alpha (RGB0) - Ex. Sansamroot.blp.
RGB, 1-bit alpha (RGB1) - Ex. Peaceflower.blp.
RGB, 8-bit alpha (RGB8) - Ex. Sungrass.blp.
```

# Conversions

**BLP -> PNG**
```
BLP P0 -> Palettized PNG.
BLP P1 -> Palettized PNG with 1-bit alpha by default.    If -r option is specified, RGBA PNG instead.
BLP P8 -> Palettized PNG with 1-bit alpha by default.    If -r option is specified, RGBA PNG instead.
BLP RGB0 -> RGB PNG (Its technically possible for these images to have 1-bit alpha, though have seen no examples.)
BLP RGB1 -> RGBA PNG    (Full alpha channel, though of course each alpha value is either 0 or 255.)
BLP RGB8 -> RGBA PNG
```

**PNG -> BLP**
```
Palettized PNG -> BLP P0
Palettized PNG with 1-bit alpha (Transparency) -> BLP P8
RGB PNG -> BLP RGB0
RGBA PNG -> BLP RGB8 by default.    If -r option is specified, BLP P8 instead.
```

# Building the Source

You will need the following modules:

- **palbmp**: A pallete library (C) Charles Bloom. (http://www.cbloom.com) I'm opting to comply with section 0 of the Bloom Public License: I'm distributing this program using the GPL. I've also made some very small changes to it: I commented out the stderr spam.
- **crblib**: Another library (C) Charles Bloom, which is a dependency of palbmp.
- **libpng**: The offical PNG reference library. (http://www.libpng.org/)
- **squish**: A DXT compression library. (http://www.sjbrown.co.uk/?code=squish)

Included are the Visual Studio 8 project files. Version 8 is adapted from a copy of Version 7 which was updated by David Holland (david.w.holland@gmail.com) to build on Linux. I hope that Version 8 can still be relatively easily adapted for Linux, but I don't know.

# WoWInterface Description

BLPConverter.exe converts BLP files (Blizzard's proprietary texture file type) into standard PNG files and back again. This is NOT a UI mod: it is a standalone program. BLPConverter uses a Windows command line interface which allows it to be easily incorporated in batch files/scripts and give the user a great amount of control about the conversion and the created file's format.

BLPConverter's emphasis is on giving the user control over the exact format of the textures it creates since WoW can be quite particular about the format of BLPs it will accept in a given situation. Unfortunately I have only had time to give it a command line interface, which I admit can present a learning curve to people unfamiliar with them. The help file included in the download attempts to minimize this hurdle.

# Versions

| Name         | Filesize                          | Author      | Source ? | Notes |
| ------------ | --------------------------------- | ----------- | -------- | ----- |
| BLPConverter | 57 KB (Source)<br/>284 KB (exe)   | Patrick Cyr | ✔️       | `4.0` |
| BLPConverter | 57 KB (Source)<br/>284 KB (exe)   | Patrick Cyr | ✔️       | `5.0` |
| BLPConverter | 360 KB (exe)                      | Patrick Cyr | ❌       | `6.0` |
| BLPConverter | 360 KB (exe)                      | Patrick Cyr | ❌       | `7.0` |
| BLPConverter | 97 KB (Source)<br/>328 KB (exe)   | Patrick Cyr | ✔️       | `8.0` |
| BLPConverter | 99.6 KB (Source)<br/>328 KB (exe) | Patrick Cyr | ✔️       | `8.1` |
| BLPConverter | 79.7 KB (Source)<br/>321 KB (exe) | Patrick Cyr | ✔️       | `8.3` |
| BLPConverter | 876 KB (Source)<br/>325 KB (exe)  | Patrick Cyr | ✔️       | `8.4` |
| BLPConverter | 876 KB (Source)                   | Patrick Cyr | ✔️       | `10-31-11`      |

# Links

* [WoW Interface](http://www.wowinterface.com/downloads/info14110-BLPConverter.html)
* [Github](https://github.com/PatrickCyr/BLPConverter)