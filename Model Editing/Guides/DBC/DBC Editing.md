1. Start up MWCS, go to file then MPQ/archive and than i usually go to enus and patch-2enus.

![[42186909ty8.png]]

2. Now if you don't have the file 'DBFilesClient' on your left don't fret just go back and try another MPQ file untill you find it.

![[82626063ny1.png]]

3. Click on DBFilesClient and go down to creaturedisplayinfo.dbc and right click on it and extract it to your desktop.

![[92040627te1.png]]

4. Next you have to open up DBCUtil1 and use the .exe file in it (DBCUtil) then grab creaturedisplayinfo.dbc from your desktop and drag it over DBCUtil, then drop it onto it and when you look down there should be a new creaturedisplayinfo.dpc.csv on your desktop!

![[74844028ba6.png]]

![[52797167ms4.png]]

5. Ok now go to your WoW Model Viewer folder (not the actual viewer) and go to npcs (this part works best with Microsoft Excell)

![[18103582wr7.png]]

6. When it opens hold ctrl + F and search the name of the creature you want to change to another. In my case it will be Rabbit.

![[31659079oi4.png]]

7. Now make sure you do this part correctly! After you have found your creature look in the coloums of numbers and pick the second number! Copy and past it into a notepad for less lag. That is the DBC number.

![[15452287gh2.png]]

8. Now re-search for the other creature and do the same thing. (make sure you don't get the DBC numbers confused with each other or you'll be in big trouble!)  
  
Now you really start the model changing!  
  
9. Close your npcs.csv and go open up the other program called CSVed. Click file/open and go to your desktop and click on CreatureDisplayInfo.dbc.csv than open it up.

![[92444246gm9.png]]

10. You should be seeing a bunch of newly made colloums full of numbers! Those are every part of information! Remember your DBC number for Ragnaros? Go down until you find it on the first virtical column and double click on it. You should be seeing a popup with new columns on it.

![[10cr5.png]]

11. Now open another notepad and copy this into it :  
  
column2.  
column3.  
column4.  
column5.  
column6.  
column7.  
column8.  
column9.  
column10.  
column11.  
column12.  
column13.  
  
Now copy the information from the columns down to match here, but DO NOT change the very first column because this is the data needed to find the actuly mob without it you will have just a little dice/box thing as a creature.  
Like so :

![[11ea8.png]]
12. Ok next go back to the main columns and search until you find the rabbits DBC code we had earlier, double click on its column.

![[12ae1.png]]

13. Be very careful here because this is the point that changes it. Change all of the information in the column (not the 1st column though) to what you have in your notepad (Ragnaros' data).

![[13ej3.png]]

14. After your done, click apply changes and then ready. Do a file and save then close the program.  
  
15. Open the folder with DBCUtil.exe in it again, but this time, drag THE CSV file onto it. it should ask if u want to overwrite the files already there, press enter then wait for it to finish.

![[14vo0.png]]
16. Open up MWCS and go to archive/Create MPQ archive, and click 'ok' on the little popup that comes up. Name the file Patch-5.MPQ or speech5.MPQ. Make sure this is in your data folder for WoW.

![[15tw4.png]]

17. Now click Pack again but this time go down to 'add file to archive' and click the ... on the box that comes up. Go find creaturedisplayinfo.dbc on your desktop and add it but don't hit 'OK' yet!! Put DBFilesClient\ with that exact spelling inforont of it because of the tree its from. Then hit 'OK'.

![[16rf7.png]]

18. You should be able to see the new folder made on the left side of MWCS and now go to Pack and click on 'save and close archive'. Exit MWCS.

![[17pf5.png]]

19. Feel free to delete CreatureDisplayInfo.dbc, CreatureDisplayInfo.dbc.csv, and CreatureDisplayInfo.dbc.bak if you still have them on your desktop because they are uneeded.  
  
20. Log on and get your Snowshoe rabbit and enjoy!!

# Credits

The original author is unknown.

#unknown_author
