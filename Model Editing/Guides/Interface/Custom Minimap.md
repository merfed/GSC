First you have to create an image of `256x256` pixels and **convert** it to blp**.**

The image will be stored in `patch-3.mpq` or **your custom patch** in the following directory path:

`textures/minimap/custommap55.blp`

I will explain below why I named the image like that according to the example given.

Next you have to extract the last version of `md5translate.trs` file found in `textures/minimap/` directory in our case we take it from `patch-3.mpq` which contains the latest version since we are using a **Wrath of the Lich King** client.

Open and edit `md5translate.trs` with notepad and add the following lines where for example `CustomMap_5_5.adt` is your custom map:

**Note**: **CORRECT** “`CustomMap\map5_05.blp`” and **INCORRECT** “`CustomMap\map05_05.blp`”
**Note**: If your adt map tile is named “`MyMap_13_13.adt`” then CORRECT would look like “`MyMap\map13_13.blp`”
**Note**: Don’t worry about the “`map5_05.blp`” and **DO NOT** rename it to “`CustomMap5_05.blp`”

Add the following line in alphabetical order in this example after ChamberofAspectsRed lines as in the picture
below:

**Dir**: CustomMap
`CustomMap\map5_05.blp custommap55.blp`

**Note**: Use &lt;TAB SPACE> between and NOT &lt;SPACE>

![[custom-minimap-1.png]]

This step was to connect minimap image to your adt map tile.

Now this is how my custom `patch-z.mpq` would look like for example I created a custom patch for my custom map
named **battleroyale** where my adt file is from `patch-3.mpq` directory:

`world/maps/battleroyale/battleroyale_8_8.adt`

**PATCH-Z.MPQ**

![[custom-minimap-2.png]]

**PATCH-3.MPQ**

![[custom-minimap-3.png]]

# Original Credits

- **Author**: !Shazam
- [Model Changing](https://model-changing.net/index.php?app=tutorials&module=tutorials&controller=view&id=133)
- [Original PDF](https://drive.google.com/file/d/1VpQnQbVZGaR3ry8n-wUUTtUfTS_DBTYh/view)