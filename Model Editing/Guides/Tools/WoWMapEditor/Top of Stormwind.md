This guide will show you how to place a bridge in front of Storm Wind so that you can get to the top of the castle and walk around on the roof.

> [!Important] Important
> Version 0.1.9 has a bug where the rendering of WMOs is not correctly rotated on the map.  If you have this version please upgrade.  If you want to DL the result file of what you should get by following this guide you can  get it from [the main page](http://somewhiteguy.homelinux.org:178/wowedit/) in the Download section. [-SWG Jul / 02 / 07]

First off, you should know that the WoW map files are located in the World/Maps/Azeroth/~ directory. the .adt files are named like `Azeroth_##_##.adt`  

THESE NUMBERS DO NOT reference the XY numbers commonly used on thotbot to point to locations.  If you want to find out which file to target based on area name, you can do a search in the 1st interface (file loader) you see in the program.  So if we wanted to edit our target area, we might want to search for Elwynn Forest...

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Top of Stormwind/1.jpg]]

Azeroth_31_49.adt seems to contain the west side of Elwynn forest, the very front of StormWind Castle, and GoldShire, so lets start there.  
Go into MyWOWStudio and extract that file, you will find it in World\Maps\Azeroth\

Extract it to somewhere and remember where you put it.

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Top of Stormwind/2.jpg]]

Next we are  going to place a .WMO file into the Azeroth_31_49.adt.  Which one?  Well, after some searching around for bridges the Thousand Needles bridge seems to be the longest so we cant mess up with that right?  For future projects you may want to use a program called [WMO2MaxScript](http://users.telenet.be/u122561/), that will convert your .wmo files into .ms files which you can click and drag into 3D Studio Max.  That way you can actually view what you are about to mess with as shown here.

Anyways, extract the 1000NeedlesBridge.wmo file to.  It can be found at:  

```
World\wmo\Kalimdor\CollidableDoodads\ThousandNeedles\Bridge\1000NeedlesBridge.wmo
```

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Top of Stormwind/3.jpg]]

Now we are going to place this bridge instance into the .adt file.  There are two ways to do this, both _SHOULD_ work, but for reasons I don't understand, there seems to be a sure way, and a not-so-sure way.  
  
The sure way is to sacrifice a currently existing .wmo file, lets use farm.wmo as an example in Elwynn Forest.  You can target `World\wmo\azeroth\buildings\human_farm\farm.wmo` in MyWoWStudio, and delete it.  Then take the 1000NeedlesBridge.wmo file, and import it into the same tree-path as the farm.wmo.  This is called .wmo swapping.  

The not-so-sure way to do it, which seems to work..... half the time,,,, is to click **Other Opts**, and goto **edit .WMO id-to-path table**.  There you can add a new path of WMOs this .adt file loads (see image).  Then go **Other Opts > Insert New .WMO Instance**, and input the new id of the file you added.

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Top of Stormwind/4.jpg]]

Either way you did it, you should now have the bridge in the .adt file.  Now lets move it to the proper location.  Despite the ugly XYZ interface, moving things is actually quite easy!  You will probably never even use the XYZ interface for anything involving movement except for messing with the Z axis.

Now click on the **View Map** button to the right.

You should be confronted with this ugly thing.  Incase you don't recognize what this is, this is a top-side look (eagle's eye view) down onto the west side of Elwynn Forest.  You can just make out the roads of the GoldShire area to the right due to all the fence post doodads (_not shown in this image_).

> [!important] If you don't see dots outlining .wmo files in them please see the Setup and Installation Guide

Anyways, left-click (anywhere) and and drag the map down-right so you can see StormWind and the bridge .wmo file  
Now get your selection to the new bridge .wmo, right click, and go **Target > Mover to where I click next**

Then just click in front of StormWind.   

Positioning it correctly might be kinda hard, while the bridges are rendered pretty much to scale and corectly, .WMOs that have multiple group files (cities) are rendered incorrectly.  The reason for this is because only the WMOName_000.wmo file is wire-frame rendered to save time.  So if there is a WMOName_001 and `_002` and `_003` and so on, they wont get rendered.  
  
So for this exercise, just look at the doodads at the Storm Wind gates and try to orientate yourself with that.  I drew a red circle here showing where the road ends and Storm Wind begins.

Yeah, i know the blue dot showing where storm wind is off, this is because Storm Wind is so freeking large, and the scale drawn is incorrect (as stated above).

![[5.jpg]]

Now save it, repack it into a .MPQ, and log in.  What do you see?  
Nothing?  
Yeah, I thought so, most likely you wont find it because just moving it to a location on the map only effects the X and Y axis.  This is important to remember.  The map makes things easy to move shit around but we cannot forget that we are in a 3-dimension world.  Not 2 dimensional.  There is a Z axis as well as X and Y.  
  
To make the Z value of your object the correct settings, go back to the main interface, right click the .WMO instance and change the Z to the same value of something around the area.  Looking at the Z values of the doodads around, I set mine to 100.  It is easy to look at the Z values in the general area by waving the mouse around the place I circled in red in the image, and watch the box at the top left.  It will tell you information about the closest object to the mouse.

I placed my bridge at **XYZ = {16662.57, 26218.94, 100}**  
If you want you can go to the main interface and manually set those values by right clicking an instance.  
I also set the rotation values to 0 ABC = {0,0,0}  
And got this as a result

![[6.jpg]]

Alrightty, it's close, and we are getting there.  Looking at your first result you can get n idea as to where and roughly how far an object needs to be moved.  Remember that the map you view in WoWMapEditor is set with North/South/East/West in correct position.  So when you look at it in WoW run time, you may want to shift your view to get a better idea how you want to move an object.  
  
Now lets get into rotation. At the main interface, right click the .WMO list and click **ABC Help**.  That will tell you about rotation and which letters correspond to what.  

After setting B to 45 (ABC = {0,45,0}), I get this as a result when going back into WoW...

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Top of Stormwind/7.jpg]]

Alright, it seems like I got the right B rotation, but what about upward tilt?  Clicking **ABC Help** again shows that we need to mess with A-rotation.  

I set A to 30.  It seemed right, but then I also had to move the XY position a tad to get it just at the right spot.  

```
XYZ = {16636.34, 26196.85, 100}  
ABC = {30, 45, 0}  
```

And I got this as a result when going back into WoW....

![[8.jpg]]

Now all that's left to do is walk up it!  w00t~

![[9.jpg]]

![[10.jpg]]

![[11.jpg]]

![[12.jpg]]

![[13.jpg]]

![[14.jpg]]