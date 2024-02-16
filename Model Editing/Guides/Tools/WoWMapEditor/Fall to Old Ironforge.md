
This guide will show you how to do basic flag manipulation to .wmo objects.. Getting to Old Ironforge will be used as an example..  .

> [!Note] There is now an easier way to get to OldIF that does not involve flag manipulation.
> [[Get to Old Ironforge]]

First off, what are flags?  Flags in this contexts is a 32bit integer that are applied to the 2-dimensional polygons that make up the 3D object (walls, floors, etc).  They references certain attributes like, will characters collide with this object or go through it?  If a character is on this object, are they outside or inside (allow them to mount?), will the cemera collide with this object? etc.  Editing such flags allows you to manipulate them in ways other than just moving them.

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Fall to Old Ironforge/1.jpg]]

With that said, lets try to get to Old IronForge.  Fist, log in and go to IronForge.  Once there, goto the central area where the Griffin Master is, and then proceed south-west until you are in "The High Seat" (the place where the dwarven king sits).  
  
If you turn around looking away from the dwarven king, you should see two black vault-doors on either side of the entrance you came through.  These are the doors to Old Ironforge.  As of right now though, you cant walk through them.  
  
Can we remove them?  Yes you can, it's not hard really, in fact, it would be allot easier to just .m2 swap them out with something else.  The vault door doodads you see are stored in:  
  
```
WORLD\KHAZMODAN\BLACKROCK\ACTIVEDOODADS\VAULT\ BLACKROCKVAULTDEPOSITDOOR02.MDX  
```
  
But if you do so you will notice that they are not actually the thing blocking your path.  Behind these doodads are invisible walls that are actually the thing from stopping you.  
  
I have spent many hours on typing to remove these walls.  I don't believe they are separate doodads, and yet I cant seem to manipulate their flags, very odd.  I think there may be a separate chunk in group-.wmo files that reference special walls?  I dunno, but the fact of the matter is, we can't get rid of them.  
  
So what do we do now?  Well, we know that Old IronForge exists under "The High Seat" (we can see it in WoWMapViewer), so lets just remove the flooring!

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Fall to Old Ironforge/2.jpg]]

Go into MyWOWStudio, and brows to the path of: `World\wmo\KhazModan\Cities\Ironforge\`
  
The Ironforge.wmo is called by a .adt map file for placing the city there, but the one file alone does NOT contain all of the city data.  Ironforge.wmo is what we call a .wmo root file, and all the Ironforge_###.wmo files are what we call .wmo-group files.  Each group file contains a small section of the city, so if we want to edit part of this city, we need to know which one of the group files to edit.

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Fall to Old Ironforge/3.jpg]]

So how do we know?  

Well, that's where [WMO2MaxScript](http://users.telenet.be/u122561/) comes in.  After extracting the directory, use that program (linked) on the root-.wmo file.  This converts all the group-wmo files into .ms files which you can click and drag into 3DStudio Max.  After clicking and dragging a .ms file into 3DS, you can tell if that is your target or not.  If not, delete it from 3DS Max and drag the next one in.  Eventually you will get to the group-wmo you want to edit.  
  
In this case, you should get to Ironforge_090 and recognize it.  It's "The High Seat" and the beginning of the passage ways to Old Ironforge.

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Fall to Old Ironforge/4.jpg]]

Well then, now that we know which file is our target, lets open it in WoWMapEditor. Target Ironforge_090.wmo and you should see a GUI like this.  
  
Here, we see all the vertices (points of intersection) of triangles (yes, .wmos are made up of triangles, and not squares oddly  enough).  We can rotate it and shit it around, but that's not our main focus.  The button at the bottom right labeled **Options** is.  
  
From this menu click **View list of flag numbers be used**  
What this shows you is pretty self explanatory.- there are sever triangles, but several seem to use the same flags as one another.  So this is list of all the flags being used with repetitions take out.  
  
Obviously one (or more) of these flag numbers tells a triangle that a character will collide with it, as when we walk into walls we collide with them.  But is there any flags in this list that lets you go through a triangle?  
  
Well the real question there is;  Can you get your character to walk through anything that is not a doodad (and actually part of the .wmo).  Well, get your character there and look around.  At first it seems no, but then... if you bring you character up the ramp near the king, walk to the right, and jump off trying to collide with the lap post hanging from the ceiling what happens?  
  
W00T!  You go through it!  And seeing as this isn't a doodad, this is really part of the .wmo!  
  
And if it's part of the .wmo, and you went through it, that means one of the flags on the flag lists lets you go through a triangle.  Get it?

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Fall to Old Ironforge/5.jpg]]

Alright, so we know now that one of these flags lets you walk though a 2-densional object it is associated with, but which one?  Well, lets find out!  
  
**First make a backup copy of the group-.wmo file!  
Then move your character out of the high seat area you are about to edit!**  

Then experiment and see what happen by going **Options > For ALL triangles replace a value of # with #**

Replace a number you see on that list with another number.  Go **Opions > Save As..,** Pack it into an .MPQ with MyWOWStudio, and login.  
  
**WARNING:**: There is a good chance you will fall through the floor into nothing-ness and die.  If you are a hunter I highly recommend you use _Eyes of The Beast_, and have your pet walk into the room, don't go in yourself.  I don't know if falling off the map sends a notice to Blizzard admins or not, but there is a good chance they log it.  If you use Eyes of the Beast, and you pets falls through the floor into nothing-ness, cancel the spell while your pet is falling.  Your pet will instantly be moved to your character's XYZ location and not die.  
  
Seeing as there are only a few numbers there it shouldn't take long to realize that value 100 lets you go through objects!

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Fall to Old Ironforge/6.jpg]]

Almighty, so we know what flag we want to use as a value to set to.  Now all we godda do is target the right triangle and set the flag to them.  
  
So goto the WoWMapEditor GUI, and click and drag a selection box over the top half down to the high seat.  After releasing the mouse button selected points should be red.  
  
Now go **Options > Hide Selected Points**

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Fall to Old Ironforge/7.jpg]]

Next select the right side and middle section, and hide them as well.  We want only the bottom left corner (everything to the left of the king's seating area, and lower/south of where the ramp starts to the seating area) to be showing after we are done hiding our points.  
  
Remember you can use the arrow keys to move the thing around making it easier to get to points behind the control set.

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Fall to Old Ironforge/8.jpg]]

This next thing you might wanna skip if it's to hard.  I did it because skipping this seemed to crash wow for some reason.  What  I did was hide the ceiling and only keep the floor vertices visible by using the A,S,D,W keys to rotate the thing around.  
  
After hiding the ceiling vertices (if you decided to do that), go **Options > Set flag for any triangle connected to a visible vertex.**  And use the flag we decided on (input the number 100).  
  
I don't know why applying the 100 flag to the ceiling crashed WoW for me (heck I don't even know if it's ceiling that did it).  Maybe it was a fluke?  But then again, I notice if I set the 100 flag to all triangle in the group-.wmo, it also crashes WoW.  It makes me think that there are certain key triangles there that cannot have this value, though I dunno which ones they are or even how to detect them.  
  
Now go **Options > Save As...**  and pack the .wmo into a .MPQ with the correct tree path and log in and see what happens.  
  
If it crashes try starting over again and this time try to hide more vertices (thus applying 100 to less triangles).  
  
If not then position you character on the king's seating area, point your character to the wall we edited..........

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Fall to Old Ironforge/9.jpg]]

Like so, and....

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Fall to Old Ironforge/10.jpg]]

Charge forth **JUMPING**, and make sure you keep going.  
**DO NOT** simply let yourself fall directly down, I think you'll miss it if you do that.

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Fall to Old Ironforge/11.jpg]]

Hopefully if you did it right you'll go through the wall of "The High Seat" area.  Getting through the walls of Old Ironforge is not problem seeing as (all?) walls in WoW are one-way.  They only stop you from going one direction through them.  So yeah, you should go right through.

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Fall to Old Ironforge/12.jpg]]

And then your there!  W00T!  
(btw, you'll need to use your hearth-stone, or die in the lava,  to get out)