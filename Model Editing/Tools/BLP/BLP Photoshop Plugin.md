- **Author**: Digital Utopia
- **Syntax**:

# Supported Formats
  
## Windows  
  
**x64**
- CS4
- CS5
- CS6
- CC
- CC 2014

  
**x86 (32-bit)**
- 6.0
- 7.0
- CS
- CS2
- CS3
- CS4
- CS5
- CS6
- CC
- CC 2014  
  
## Mac OS X  
  
Mac OS X plugin requires OS X 10.6 (Lion)+  
  
**x64**
- CS5
- CS6
- CC
- CC 2014
  
# Installation
  
## Windows
1. Find your Photoshop Folder  

```
a. eg1: (x64) C:\Program Files\Adobe\Adobe Photoshop CS6 (64 Bit)\  
b. eg2: (32-bit) C:\Program Files\Adobe\Adobe Photoshop CS6\  
```

2. From that folder, go to \Plug-ins\File Formats\ (create "File Formats" folder if it doesn't exist)  
3. Drop the appropriate plugin (x64 or x86) in that folder.  
4. Run Photoshop  
  
## OS X
1. Find your Photoshop Folder  eg: `/Applications/Photoshop CS6/  `
2. From that folder, go to \Plug-ins\File Formats\ (create "File Formats" folder if it doesn't exist)  
3. Drop BLP.plugin in that folder  
4. Run Photoshop  
  
# Supported Variants
  
It was my goal to support every variant of the BLP format that Blizzard uses in WoW - for both opening and saving. The end result is a total of 11 different combinations of compression and transparency. Below is a listing of these.  
  
## Alpha Bit Depths
This is the amount of detail allowed in transparency of your image.

- 0-bit - No transparency at all
- 1-bit - simple transparency, similar to GIFs. It's either transparent or not.
- 4-bit - slightly better range of transparency, but will turn smooth fades into visible "steps"
- 8-bit - This is the same level of transparency you'll ordinarily see in PNG/TGA formats, with 256 levels of transparency.

## Compression Types
- **Indexed (256 Color)** - Very similar to a GIF, as it uses a palette that can fit up to 256 colors, but BLP files have indipendent transparency. Indexed BLPs can make use of all 4 types of alpha.
- **DXT** - This is the defacto compression type used in modern games, with the most popular format that uses this, being .dds. DXT compression gives you a better color range, with a slightly larger size, than indexed. It also supports all 4 levels of transparency.
- **DXT-5** - Would normally be lumped in with the above category, however it's the second DXT type that supports 8-bit alpha. The result is a bit better color, and a slightly larger file size than the 8-bit alpha under the DXT category.
- **Uncompressed** - Very much like a Bitmap, with no compression to speak of. It can support either 0-bit or 8-bit alpha. This version is only used by Blizzard for sky textures, where every bit of color detail is necessary.

# Known Issues
The Mac Plugin will not properly load DXT compressed BLP files, with its Alpha Depth set to anything but 0, 1, 4, or 8. This means some DXT(5) compressed files that have their Alpha Depth set at 72, will not load correctly. Unfortunately I have lost the source code for the Mac version, as well as access to OS X, so I'm unsure when or if I'll be able to release an update.  
  
As a work around, change the Alpha Depth in such files to "8" - using a hex editor, or an upcoming tool, and they will load correctly.  

# Versions

| Name                 | Filesize | Author         | Source ? | Notes                         |
| -------------------- | -------- | -------------- | -------- | ----------------------------- |
| BLP Photoshop Plugin | 443 KB   | Digital Utopia |          | Mac                           |
| BLP Photoshop Plugin | 765 KB   | Digital Utopia |          | Win x86                       |
| BLP Photoshop Plugin | 983 KB   | Digital Utopia |          | Win x64                       |
| BLP Photoshop Plugin | 395 KB   | Digital Utopia |          | Win x64/x86                   |
| BLP Photoshop Plugin | 408 KB   | Digital Utopia |          | Win x64/x86 `0.X2`            |
| BLP Photoshop Plugin | 408 KB   | Digital Utopia |          | Win x64/x86 `0.X3`            |
| BLP Photoshop Plugin | 529 KB   | Digital Utopia |          | Win x64/x86, Mac `0.X3a`      |
| BLP Photoshop Plugin | 708 KB   | Digital Utopia |          | Win x64/x86, Mac `1.0`        |
| BLP Photoshop Plugin | 712 KB   | Digital Utopia |          | Win x64/x86, Mac `1.0-repack` |

# Links

- [WoWInterface](https://www.wowinterface.com/downloads/info22445-BLPFormatPlug-inforPhotoshop.html)