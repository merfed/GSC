This guide will show you how to apply a change to multiple doodads rather than having to go through each and every single one.  
As I am writing this, the multi-manip functions are limited, so I'll try to update this guide as later versions are released.  
To follow this you you must have version 0.1.8 or higher

  
**This guide is divided into sections**:
- How to kill all trees (practically already done for you)
- How to move all of the same objects at the same time (or make them dissappear)
- How to move literally all objects at the same time

# FAQs

**So what happens if I get rid of a tree and I walk right through the path were it existed?**
Nothing on your side, but on another's monitor your will appear to have gone right through the tree.  

**Will I get banned for that?**  
o_O  If the GMs were really THAT nazi I suppose.  I don't see why anyone would care.  The ONLY reason I could think of you getting banned for doing this is doing a "hide-inside exploit" - That's where you hide "inside" the tree, and start shooting at people.  They cant see you because your inside the tree, and mobs usually wont be able to get to you either.  

**Is there any real use for deleting trees?**
Read the one above this.  But do so at your own risk.  Also if your using Glider there is les of a chance your character will get stuck in an obstacle if you remove them all.  

**How do I undo this?**  
You can't.  You will need to restore whatever map file you messed with from a backup.  If your smert, you wont be packing your map changes into Common.MPQ, but rather into a custom patch, so you could get it from there.  Also, if you followed the Setup and Installation guide, then you may have a backup in your DummyMPQ path.  If all else fails, goto worldofwarcraft.com and click to DL the 10-day trial.  Dont make an account, just DL the game.  That comes with a few "tome".MPQs, and you can find 2.0.0 files in there.

---

# How to Kill All Trees

Pff, this is pratically done for you.  Open your target .adt file, and in the main interface, go **Other Opts > Kill All Trees!**

And that's it.  Just save file, and repack it into a .MPQ with the same directory/tree path you get it from in MyWoWStudio.

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Mass Doodad Manipulation/1.jpg]]

# How to Move all the Same Objects at the Same Time

See that big list of doodads?  Well quite a few of them have alot of similar names, so wouldn't that be great if we could just have the program loop through them all and apply a change to ones that have a given string inside them?  Well, that;s basically what the last step did.  With the search string of "_tree_", it went through the list and found any doodad that had "tree" in the model path, and for those that it found, it changed the Z axis to -800 (ok ok, so it doesn't really delete them, but it DOES get them out of site - I'm just lazy, blah)  
  
So what if we wanted to do a similar thing to all bushes or fences?  Well in this case you open your .adt file, and in the main interface go **Other Opts > Do custom Z change to multiple doodads**.

You should first get an input-prompt for a search string.  Lets put "tree" in as an example.  

Then you should get a value request, lets put in -800.

After doing this you should notice we have done the same thing as **Other Opts > Kill All Trees** does  
  
But now you should understand how it works.  You should be able to put in other key words in there like "bush" and "fence" and what-not.  Remember the input (1st prompt) is a search-input - it doesn't look for exact matches, it looks for any doodad that has your input **_somewhere in_** a doodad model path.  
  
Also, the Z value (incase you didn't know) is just the altitude at which the doodad is placed.  Placing it at -800 just places it way far down underground so we will never see it.

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Mass Doodad Manipulation/2.jpg]]

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Mass Doodad Manipulation/3.jpg]]

![[Z. Meta/Attachments/Model Editing/Guides/Tools/WoWMapEditor/Mass Doodad Manipulation/4.jpg]]

# How to move literally all objects at the same time

Same as above, but don't put in a search string, leave the input-box blank.  It should  prompt asking if you really want to target all objects.