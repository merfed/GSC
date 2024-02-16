Today I'd like to share some of my knowledge regarded to creating a working world map in-game. I will try to cover the most basic things, but I have to admit there are still some unknowns to me such as clickable zones on the world map, however, I 'd like to cover those and continents map in the future.

In this tutorial I will cover a basic in-game map creation for GM Island.

![[meokwnkj.bmp]]

# Required Tools

1. DBC Editor
2. MPQ Editor
3. Photoshop
4. World Map Creating Package

Before sinking teeth into this in-game map making process you might want to take a look at Skarn's tutorial on making a map for WoW in photoshop:

> [!Warning] Skarn's Tutorial is missing, cannot find it.

So first of all some theory. When it comes to Dbc files what really matters to us right now is WorldMapArea.dbc. This Dbc looks somethings like this:

![[jf6rfakz.bmp]]

| Column | Description                                                                                                                |
| ------ | -------------------------------------------------------------------------------------------------------------------------- |
| 2      | Refers to `map.dbc` and says on which map in the world this will be placed. `1` is Kalimdor.                               |
| 3      | Area Name (DBC Number), in this case its `876` (GM Island)                                                                 |
| 4      | Map file name, refers to your filenames. If you name it `GmIsland` all files must be named this way; `GmIsland_1.blp` etc. |
| 5      | Upper Y Coordinates of your map                                                                                            |
| 6      | Lower Y Coordinates of your map                                                                                            |
| 7      | Upper X Coordinates of your map                                                                                            |
| 8      | Lower X Coordinates of your map                                                                                            |
| 9      | Has to be -1 ?                                                                                                             |
| 10     | Has to be 0 ?                                                                                                              |
| 11     | Has to be 0 ?                                                                                                              |

So this was some Dbc stuff. Now let's move to the real map stuff. Obviously what you need to is to create yourself a world map, Skarn has covered this topic some time ago, there is a link to his tutorial mentioned above if you need to create a map I recommend you going there.

But now comes the tidious stuff. In order to make your map working you have to divide it into 12 256x256 images and name them just like this - GmIsland1.blp, GmIsland2.blp, this however, comes for GmIsland map, if you name your map in WorldAreaMap.dbc TelAbim you have to name your files TelAbim1.blp and so on.  When it comes to chronology you have to follow the one shown in the picture down below. So GmIsland1.blp represents sector 1 and so on.

![[map-segments.png]]

This is obviously some really boring stuff, but it is essential. In addition, I think it is good for you to know that all the segments and the right (4, 8, 12) and all those on the bottom (9, 10, 11 ,12) have to be transparent and won't take the entire 256x256 area. Skarn has thought of this when making his map templates, so you don't really have to worry about this one.

Now we need to put all the files into a patch, so that the game can loads those. The Dbc stuff is kind of obvious, you put that into DBFilesClient folder, and as for the blp files you have follow this chronology :Interface/WorldMap/GmIsland (Dbc name of your map)/GmIsland1.blp ...

![[chronologie.thumb.png.5687d3fc21d0b16754175ebffb8d6c78.png]]

So once we are done with all of this, we can check the map in-game and see if it works.

![[WoWScrnShot_091219_072013.jpg.c0c72c26f27cc0a6a55c071177c81fa0.jpg]]

The maps seems to be working. If you are trying to create a world map for yourself, you should start by taking down the map coordinates (in-game or in the Noggit) and then according to that create the map.

_I hope this quick tutorial was helpful in some ways, and hopefully I will find myself some more time to extend it one day. Maybe I could cover making a new continent or making a zone clickable on world map._

# Original Credits

- **Author**: Krysík
- [Model Changing](https://model-changing.net/index.php?app=tutorials&module=tutorials&controller=view&id=135)