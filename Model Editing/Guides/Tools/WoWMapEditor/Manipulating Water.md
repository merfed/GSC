This guide will show you how to place water in locations, change altitude, and even delete liquids.  
  
**The Limits:**  First off you should know that what we are messing with it _liquids_.  There are liquids declared for every chunck of the map and their height, and weather they are oceans, rivers, or magma is determined by the MCNK chunk (the red box on the map).  Their for I am pretty sure it's imposable to have water and magma at the same time in the same MCNK chuck (red box).  [Key word there: "think"]  Based on the data format of .adt files it seems like it is also imposable to have more than one layer of water in a given space (cant have one layer of water directly over/under another).  Though, there is video proof that it can be done as there seems to be such a thing Blizzard made in an unfinished unallocated area.  Though I dont know, and WoWMapEditor doesn't know how to make such a thing.

  
**Contents  
**This guide is divided into sections:

- How to place water all over the map with the same height - nice for getting just about anywhere and easy to do
- How to delete water from the map entirely
- How to draw water on the map (control where it is an how high).

**FAQs**

**How do I know what value to set a water level to if I want to make it a certain height in comparison to other objects?**
Go to the main interface and observe the Z axis of other objects of Doodads and WMOs.  Set the water height according to their Z axis and increase or decrease according to where you want the water level.  Keep in mind it's pretty sensitive though. Increasing the water-Z-height by about 4.0 I _think_ is increasing it higher than the height of a human.
    
**Will I get a breath gauge under water I create?**  
No, but you will get a breath gauge regardless if there is water or not on your map for a given location if your XYZ location is in a space where the SERVER thinks water is.  In other words, after testing I am pretty sure breather is controled server side.
    
**How do I get around the breath guage then?  Is there a way?**
Yes, you can increase the water height.  You only get a breath gauge if your XY AND Z location is in a space where the server thinks water is.  So if you swim above the normal water line you will enve get a breath gauge.
    
**Awesome!  What about fatigue?  Can I get around that too?**  
I'm trying to find a way.  Unfortunately you get fatigue based on your characters X and Y position,,,, not Z.  It doesn't seem to pay any attention to Z.   At first I was confused by this, I was thinking; how do boats work?  They go far into the ocean and we never get a fatigue bar...  But then I realized that boats only go to the brink of the ocean before instancing into the next continent.  They don't actually cross over the border to where fatigue starts.

---

# How to place water all over the map with the same height

![[1.jpg]]

This isn't difficult, just open a .adt map from `World/Map/Azeroth/` or whatever, and in the main interface, go **Other Opts > Set global water level**.  Note that _global_ in this context refers to THIS map only.  It will not actually change the entire world.  A default value of like 700 or something was put in because that is waaayyy high.  With that value, for most maps, you can swim just about anywhere.  
  
Pretty easy, now just save it, pack it back into a .MPQ file with MyWoWStudio with the same tree path and log in.  You should have water.  If you problems after saving, see to the FAQs on the main page.

# How to delete water from the map entirely

![[2.jpg]]

LOL, do I really need to make a guide for this.  If your lost read the section above.  It's in the same menu, click it and all water is gone.  It applies to the opened map only.

#  How to draw water on the map (control where it is an how high)

After loading your target .adt file, click **View Map** on the main interface.  Then right click the map, and choose the option to draw water.  When drawing water you must click and drag the RIGHT mouse button.  The left mouse button is used to move the map around so you can get to places if it off the screen.  
  
**ONCE YOU ARE DONE:  You must actually click the done button!**  Or close the map and go back to it (basically make it redraw).  And make sure the results is what you want.  In version 0.1.4 (and .5) the things seems to skip over some chunks and kinda shift a bit.  Look to the two images to see what I'm talking about.  

Also note that (in ver 0.1.5)  WMOs and doodads are not drawn in correct proportion to water and holes in the ground.  It's usually pretty close though.

![[3.jpg]]

![[4.jpg]]