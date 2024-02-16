Q. What can I accomplish after reading this guide?  
A. Fast, easy way to change what your weapons, shield, or armor looks like.  
  
Q. Why DBC edit instead of model change?  
A. I prefer DBC because it is faster, easier, and you don't have to waste time looking for a model name.  
  
Q. Why model change instead of DBC edit?  
A. With DBC editing you can only edit items you have seen/have, unless someone gives you their itemcache.wdb file.  
  
Q. Is this all I can do with DBC editing?  
A. No! There is **A LOT** more you can do, this is just a simple introduction to it.  
  
Q. Player x said method y is better/easier/more efficient than this.  
A. There may be better/easier/more efficient methods, but I prefer this one.  
  
Ok lets get started!  
  
**BACK UP YOUR ITEMCACHE.WDB BEFORE EDITING IT!!
  
First you need to download Hex Workshop free trial.  
Serial number if you want the full version is 161660427-502701-9839  
  
All right after you are done installing open up Hex Workshop and open up itemcahce.wdb. (Default location is C:\Program Files\World of Warcraft\Cache\WDB\enUS\itemcache.wdb)  
  
Do not be scared by all the numbers and letters. I will tell you exactly what to do!  
  
Ok now press Ctrl-F to open Search. For Type: drop-down select Text. Type in your item's name. For this tutorial I will change High Warlord's Blade into Gladiator's Slicer.  
  
Once you find your item you will see it written 3 times on the right side:

![[step1lt3.png]]

Highlight the last letter of the last set. (The E in the third High Warlord's Blade in my case).  
  
It should highlight 2 numbers/letters. After those 2 numbers/letters there should be 2 0's. After the 2 0's should be a set of 4 letters/numbers. This is what we are changing.  
  
Red circle = highlighted letter. Blue circle = 2 0's. Black circle = what we are changing.

![[step2ej4.png]]

Ok now we are going to find out what we have to type in there to change it to Gladiator's Slicer. (Or whatever you are changing.) Go to [http://wow.allakhazam.com](http://wow.allakhazam.com) and search for the item you want. (ex. Gladiator's Slicer)  
  
Under the item's stats click on XML. On this page copy the displayinfo number.

![[step3sq0.png]]

Copy that number and go to [http://www.willamette.edu/~gorr/clas...n/convert.html](http://www.willamette.edu/~gorr/classes/cs130/lectures/BinaryConversion/convert.html) Paste the displayinfo number into the decimal field and press convert.  
  
Ok this is the confusing part. You have to put the hex code in backwords. So if the converted hex was A58B, you would put it in as 8BA5.

# Credits

- Unknown author

#unknown_author #broken_links