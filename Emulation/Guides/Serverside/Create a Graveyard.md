Before we start, don't forget this, your graveyard won't work if you haven't extracted your map's maps.

**Summary**

- Required tools
- WorldSafeLocs editing
- Database editing
- Ingame command

**Looks like it's time to gear up !**

- Your 3.3.5 client  
- Your WorldSafeLocs.dbc  
- Your World Database access  
- To be GM ingame.

**I send you to graveyard !**

Open WorldSafeLocs.dbc with your favorite DBC editor.

Quick explanation :

First column : Graveyard ID (must be unique ! I start at 1900)  
Second column : Your mapId contained in Map.DBC  
Third column : graveyard's X position  
Fourth column : graveyard's Y position  
Fifth column : graveyard's Z position  
Seventh column : Name your graveyard !  
Eighth : Meh.

To obtain your coords, you'll have to go ingame and make .gps where you want to locate your graveyard.  

Then, fill your DBC. I did this:

![[af2f8cef5f.png]]

"But, what means CI Hyakki-master ?"  
Did you know I'm French ? In France, a graveyard is called "cimetière", you can pronounce it like Google says : [cimetière](https://translate.google.fr/#fr/en/cimeti%C3%A8re)  
Then, CI is the abrevation of Cimetière :)") (We learn so much things with me yay !)

Upload it to your server (and I'm not sure, but I don't think it's necessary in your MPQ)

Next step!

**DB ? You mean Dragon B... No. DataBase.**

Open your world database and open the game_graveyard_table.

Quick explanation 2 :

ID : Your graveyard ID that you have set in WorldSafeLocs (1900 in my example)  
GhostZone : AreaID from Areatable.dbc where the ghost will spawn.  
Faction : Who can spawn in your graveyard ?

```
0 - Any team accepted

469 - Alliance team only

67 - Horde team only
```

Here we are

![[d27c8c2a87.png]]

**It's time to die !**

Go to your custom map and execute this command :

X = your graveyard ID (1900 in my example)

```
.linkgrave X
```

If you obtain an error, check that you have extracted your maps, and if you Areatable.dbc in serverside is valid too.  

otherwise, kill you and you'll see !

This tutorial is finished ! Don't forget to spawn the Spirit Healer ! (ID = 6491)

# Credits

- Hyakkimaru