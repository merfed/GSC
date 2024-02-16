- **Author**: Somewhiteguy
- **Syntax**:

> [!Note] Welcome (From SWG's Website)
> Well, I created a map editor that could mess with the .adt and .wmo files in the World of Warcraft .MPQ files.  After posting it on mmowned, people were actually more angry than happy.  They said that if this thing got out in an uncontrolled fashion, people would manipulate WoW like no tomorrow, then Blizzard would nerf this along with model editing (Many of them were model editors and that made them pissed).  So after more angry comments and some thinking I decided that they were right, and I took the application down.  Later however people kept PMing me asking for this thing.  It seemed there really was a demand for it, so I decided to make a version that would NOT edit certain map files.  All version release now will NOT edit any Battleground or major PVP area maps or anything else I throw in the blacklist.  Due to many PMs over the forum and ppl saying they want to talk to me about this thing (ask questions or whatever), I decided to make a little website.  
> 
 > I don't have an email address cause I don't see the point in one if I have these message boards, plus email systems just gets overrun by spam.  So use this and feel free to ask any questions  ; )

# Setup and Installation

This guide will show you how setup certain WoWMapEditor features that don't initialize themselves automatically.

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Setup and Installation/1.jpg]]

So after you have downloaded the archive and extracted it to a place like C:\Program Files\WoWMapEditor\ or whatever (the path doesn't really matter).  Go into MyWoWStudio and open up Common.MPQ.  Now click on the **World** folder.  Right click and extract it somewhere.  The files are going to remain to where you extracted it so put it somewhere where it isn't in the way.  
  
If thise takes to long or to much space, go ahead and click on the drop-box to the bottom left of MyWoWStudio and select **World Model Object (.WMO)**.  These files are our real target.

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Setup and Installation/2.jpg]]

Next, go into WoWMapEditor, open any **.**adt file so you get to the main interface.  Then click **Other Opts > Declare dummy MPQ Path** and plug in the path to the World directory, THE PATH SHOULD NOT CONTAIN THE "WORLD" DIRECTORY, just the path TO the directory.

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Setup and Installation/3.jpg]]

And then your done.  To test and make sure things are going correctly do either of both of the following:

- With _Version 0.1.5_ of later, go to the main interface and click **Other Opts > Show Debug Window**.  And then click the **View Map** button.  If you did everything correctly, you should see messages in the debug log saying it's rendering WMOs.  If not, it may say it couldn't find a given file.
- Try opening Azeroth_31_49.adt, you can find it in Common.MPQ (or in you dummy directory if you extracted all the files) in the **World/Maps/Azeroth/** if you setup everything correctly, you should see something like this image to the right (click it to see a larger version).  You should be abel to see additional block dots (marking the verticies) of all the WMO objects indicated by the fat blue dots.

# Guides

_All guides are present in their original form in the folder **WoWMapEditor Guides**._

- [[Fall to Old Ironforge]]
- [[Get to Old Ironforge]]
- [[Manipulating Water]]
- [[Mass Doodad Manipulation]]
- [[Top of Stormwind]]
- (**Never Made**) Editing the AreaID tags to have custom text flash when your enter a certain zone
- (**Never Made**) Basic .WMO morphing, stretching, and reshaping
- (**Never Made**) Putting holes in the ground to get underground

# Patches

*Unknown if these have been archived, I haven't located them yet.*

## Top of Stormwind Castle
*patch_8.mpq*

If you follow the guide above on how to get on top of Storm Wind, you should get something like this.  When making this I didn't add in a new WMO instance, I sacrificed the farm WMOs, and renamed "farm" to "fart" (I decided to change one letter because at the time (older version) changing the ADT file size fucked things up, so I change the path by one letter and then placed the 100NeedelsBridge for the made-up path). All needed WMO/ADT files included, just drop this in your WoW Data directory.

## Get to taxi "graveyard"
*patch_7.mpq*

Well, [in a thread on mmowned](https://web.archive.org/web/20071012022356/http://www.mmowned.com/forums/wow-general/27679-wow-taxi-planes-theroies-how-they-work-messing-zepplin-boats.html#post201504) I made showing research I've done with taxies (boats and the Zepllin) and how they work, I was intrigued on hearing about a taxi "grave yard" - that is, a place where the taxi sits when it supposedly is not in use.  You can read the thread to understand what I mean, but anyways.  This map edit will allow you to get to the center of the world for The Eastern Kingdom, where the taxie(s) are placed when they shouldn't be showing anywhere else.  This effect the area South-West of the  Alteric Mountains.  [See this video on how to get there](https://web.archive.org/web/20071012022356/http://www.guybooru.net/wow/BoatGraveYard.avi).  Note if you log out on the boat-plane, and come back on, you character will be stuck - use your hearth stone to fix this.

## Get to Old Ironforge
*patch_9.mpq*

Well I found a new way to get to OldIF without editing flags of triangles (which are a pain in the ass, and even for me, hard to do right).  Just open the group-WMO file (IronForge_090.wmo) and rotate it aorund so you see the side.  Then select the floor area and shift Z down by about 8.  I got this as a result.  **[View the video](https://web.archive.org/web/20071012022356/http://www.youtube.com/watch?v=66m4EVGBwn4)** on how I used this edited map file.

# FAQs

**Can this program edit battle ground maps and major PVP areas?  
NO**, incase I haven't made it blatantly obvious...  It will stop you from doing that.  This is NOT a hack tool people.

> [!Note] A way around editing battleground maps
> A tool was released named *WoWMEUnblacklisted_PvP_Grounds* that lets you enable BGs.
  
**Can this program create an island in the middle of water? Or change the shape/height of land?**  
Iin the future it will.  I know it's possible to do, though right now I have no experience messing with water level in the hex editor yet, so I first need to do some research.  

[Edit] Man, what a pain in the ass this is going to be.  Im trying but having a hard time.  I am making a DirectX render, and I just cant seem to get the tiles to line up with one another.  *cry*  You can [read more here I guess](https://web.archive.org/web/20071012022356/http://www.wowmodelviewer.org/index.php?option=com_smf&Itemid=44&topic=1115.msg5718).  

**Can this program let me draw on the land or change land textures?**
Iin the future it may.  

**Can this program let me move .WMO intances/objects and doodads around?**
Yes, see the guides for assistance on how to do this.

**I made changes in WoWMapEditor, but now WoW crashes with an error message**
If WoW is saying a file is corrupt, and pointing to the file you edited, then you are either (A) not using ModelChange.exe, or (B) our ModelChange.exe is out dated.  Goto the MMOwmed fourms to get an update on it.  

**I made changes in WoWMapEditor, am using ModelChange.exe, but now WoW crashes with no error message.**  
Yeah, what's up w/ that!?  LOLWell, this can be due to a variety of things**, depending on what you were doing.  I recommend saving a backup copy every step of the way between editing and logging in to find out the cause.  Here are some known things to crash WoW, And no, I don't know why they do it**:**

- Setting all triangles in a .WMO grup file to the same flag
- Changing the unknown flags of .WMO placements in a .adt file- changing slightly seems to be fine, but not to much o_O
- Pressing Ctrl+Alt+Del and killing MyWoWStudio while it's open and in edit mode (even if it's not in the process of saving)

**I made changes in WoWMapEditor, but the changes aren't showing up.  Everything is still the same in WoWMapViewer!**  
WoWMapView does **NOT** load any Path-#.MPQ files other than Blizzards real patch.  So if you want your changes to actually show in the viewer, you need to placed edited files in either Common.MPQ or the first patch (or maybe expansion?).  
  
  
**I made changes in WoWMapEditor, but the changes aren't showing up.  Everything is still the same when I log into WoW!**
First off the basics.  You need to use MyWoWStudio to open Common.MPQ, browse to your target file for editing, right click and go **copy tree path**.  Then right click and **remove** the file.  Click and drag your newly edited file into MyWoWStudio, and **paste** the tree path you just copied in, and then **save** the MPQ.  
  
If you changes still dont show up, make sure your file is not being overridden.  **NOTICE**: _patch_ and _expansion_ override _Common.MPQ_!  
  
If it is not being overridden, and the change you made is a .WMO placement location in a .adt file, then look into the .adt files neighboring to it.  I noticed that .adt files seem to overlap, and if a .WMO sits in this overlap, BOTH .adt files reference it, and BOTH files will nee to be edited in order to get the .WMO to move.  The best example of this is GoldShireInn.WMO referenced in Azeroth_31_49.adt.and its neighbor.  
  
  
**I can make changes to things, but I just cant get this one .WMO to move**
Look into the .adt files neighboring to it.  I noticed that .adt files seem to overlap, and if a .WMO sits in this overlap, BOTH .adt files reference it, and BOTH files will nee to be edited in order to get the .WMO to move.  The best example of this is GoldShireInn.WMO referenced in Azeroth_31_49.adt.and its neighbor.  
  
  
**Can I be caught and banned for this?**
It's possible, but more likely if your one of those dumbasses who edits a common city area or GoldShire, and stands in mid-air, floating above everyone, dancing naked, and asking for gold (then again, I've done exactly that just for the hell of it, and never got the boot), about the only way I can foresee you getting banned is if someone reports you by seeing you do something you normally cant possibly do.  

[Edit] I did something stupid, I edited the WSG BattleGround, and after 2 months FINALLY got caught.... I wasnt banned though, W00T.  lol, but I SERIOUSLY think I got off lucky on that one.  Dont expect to get a warning like I did if you somehow get caught.  [You can read more about how I may have got caught here (click)](https://web.archive.org/web/20071012022356/http://www.mmowned.com/forums/wow-general/24794-can-gms-detect-map-hacks-because-though-i-caught-i-wasnt-banned-o-o.html).

# Known Issues

- **v0.2.4 beta**
	- When drawing water from the map interface, you may want to close the map and go back to it again (make it re-draw), it seems to skip bloches `>_<`
	- WMOs and Doodads may not be correctly placed on the map in proportion to water and holes in the ground.  It's close though (usually)
	- Moving a doodad outside of its originating MCNK chuck (red box in the map) usually results in it disappearing, or letting you walk through it.  This applies to doodads, **not** WMOs
	- Adding in additional WMOs seems to crash WoW most of the time - just try WMO swapping for now... I guess you'll just be limited to the number of WMOs for within a given map :\  Sorry, I'll look into this and fix it, give me some time.

# Versions

| Name                 | Filesize                               | Author | Source ? | Notes |
| -------------------- | -------------------------------------- | ------ | -------- | ----- |
| WoWMapEditor 0.0.1   | 1,662 KB (Release)                     |        | ❌       |       |
| WoWMapEditor 0.1.1   | 1,459 KB (Release)                     |        | ❌       |       |
| WoWMapEditor 0.1.2   | 5,272 KB (Release)                     |        | ❌       |       |
| WoWMapEditor 0.1.3   | 5,032 KB (Release)                     |        | ❌       |       |
| WoWMapEditor 0.1.4   | 5,033 KB (Release)                     |        | ❌       |       |
| WoWMapEditor 0.1.5   | 5,241 KB (Release)                     |        | ❌       |       |
| WoWMapEditor 0.1.7   | 5,260 KB (Release)                     |        | ❌       |       |
| WoWMapEditor 0.1.8   | 5,575 KB (Release)                     |        | ❌       |       |
| WoWMapEditor 0.1.9   | 5,771 KB (Release)                     |        | ❌       |       |
| WoWMapEditor 0.2.0   | 5,772 KB (Release)                     |        | ❌       |       |
| WoWMapEditor 0.2.1   | 5,952 KB (Release)                     |        | ❌       |       |
| WoWMapEditor 0.2.2   | 5,980 KB (Release)                     |        | ❌       |       |
| WoWMapEditor 0.2.3   | 5,994 KB (Release)                     |        | ❌       |       |
| WoWMapEditor 0.2.4   | 5,995 KB (Release)                     |        | ❌       |       |
| WoWMapEditor 0.2.4-2 | 1.97 MB (Source)<br />519 KB (Release) |        | ✔️       | <span class="bc">BC</span>       |
| WoWMapEditor 0.2.5   | 6,310 KB (Release)                     |        | ❌       |       |

# Links

- [Website](https://web.archive.org/web/20071012022356/http://www.somewhiteguy.homelinux.org:178/wowedit/) (*Archived*)