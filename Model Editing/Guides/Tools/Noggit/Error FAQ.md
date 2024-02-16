If you have problems with _Noggit_, please read the following **FAQ** before posting a support topic. It is very unlikely that the issue you are experiencing is unique, so someone has probably already encountered it before. That is why we have created the most ultimate and reliable source of information about crashes and other problems with _Noggit_.

# Why is Noggit not opening/closing on start?

**Solution:** There are multiple solutions for this issue depending on its reasons. First of all, check your "**noggit.conf**" file and see if it is not called "**noggit.conf.conf**". If so, remove another "**conf**" thing. Open this file, check if important strings like "**GamePath**" and "**ProjectPath**" do not contain any **#** character before them and make sure that there is a "**\**" after each file path. "**ProjectPath**" should be set to your _WoW_ folder, not to **WoW.exe** or Data. Those are the most common problems.

If your _Noggit_ can't read or load some **MPQs** (according to the **log.txt** file), go to your game client folder properties and disable the "**read-only**" flag. If still not works, make sure that no tool is currently using the **MPQs**, for example, _Ladik's MPQ Editor_.

Noggit currently supports only _World of Wacraft_ **3.3.5a**, so make sure you are not running it on other expansion game clients.

# Why isn't my Noggit working with recent expansions?

**Solution:** _Noggit_ currently supports only _World of Wacraft_ **3.3.5a.** It is very unlikely to be updated to the later expansions, so we would recommend you to check _Cromon's Neo Editor_ for editing _WoD_ and other later expansions.

# Why is my water missing after saving ADTs in Noggit?

**Solution:** You are using an extremely outdated version of _Noggit_ (most likely **SDL 1.2**) which does not support water editing/saving. Get the newest version of the tool.

# Why is my Noggit displaying the message that the MSVC****.dll is missing.

**Solution:** Get _Noggit_ from our **beginner's tutorial** pack which has the necessary libraries included or get all the _Microsoft Visual C++ runtime libarires_ (2005-2013).

#### The FAQ will be updated from time to time if something new pops up.

# How can I get rid of disappearing models and other saving bugs in Noggit?

Lets say you want to edit Howling Fjord in Northrend:

![[image.jpg]]

So, you open Northrend map, go to Howling Fjord and then you should mark all ADTs you will want to work on as edited by doing whatever in them. You can just click with flatten tool somewhere, or move some object a little bit to do so. When you are done, when all ADTs you will want to mod are edited, you can save. By that way you will mark area you will want to work on. So your Northrend will look somehow like this lets say:

![[image(1).jpg]]

And now, EVERYTIME you are working on ANY of these ADTs, you should mark ALL ADTs as edited. So ALWAYS before you save, your Northrend map will look like this:

![[image(2).jpg]]

Do not save your map if all "orange" ADTs are not white-bordered. And always restart Noggit after saving. 2 simple rules - and no there should be no objects which disappear or are duplicated.

# Credits

- Skarn

# Links

- [Model Changing](http://www.model-changing.net/forums/topic/22-ultimate-noggit-error-faq/)