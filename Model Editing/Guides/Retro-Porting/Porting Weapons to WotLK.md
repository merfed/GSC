# Requirements

- [[WoW.Export]]
- [[WDBX Editor]]
- [[MPQEditor]]
- [[Multi Converter]]
- 3.3.5.a Server
- WotLK Client
- TXID
- HeidiSQL
- 010 Editor

# Speedrunning Retroporting

Open wow.export (or) CASCExplorer, both is fine, really _i'll use wow.tools for this_.

Open your wow.tools, select the box with the best ping, click on the world icon after that -> World of Warcraft 9.1.5 bla bla bla

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/1.png]]

You should automatically be in "Models", good. Search for any weapon.

I looked for "ArtifactSoulrend_d_03" since i was going to add it anyway. Select any color and export it using my settings. (if you want to be extra fancy and add an Icon, go into wow.tools -> files -> Search "`artifactsoulrend_d_03`" and download the `interface/icons/inv_sword_2h_artifactsoulrend_d_03.blp` ) we later will make it into our custom patch no worries.

![[2.png]]

Now head to your exported folder, go to items\objectcomponents\weapons and rename artifactsoulrend_d_03_red (whatever the color is).m2 into 

artifactsoulrend_d_03.m2

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/3.png]]

Now slap that bad boy .m2 file into TXID about 15 times and hit FIX.

Do the same with MultiConverter, but only put it once in there. Click Fix afterwards.

You can utilize 010 Editor [Step 3/6](https://model-changing.net/tutorials/article/154-retroport-to-wotlk-wings/) and search for .blp and if you used wow.tools you can look in the folders it may have created, but for this specific weapon everything is in items\objectcomponents\weapons that we need.

# Editing DBC

Open ItemDisplayInfo.dbc from your servers dbc folder. 

We open ItemDisplayInfo.dbc with WDBX Editor and Select WOTLK from "Load Definition"

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/4.png]]

We start in ItemDisplayInfo.dbc by making a new Line, Right-Click -> Insert Line. 

Make a unique ID (mine is 100050); ModelName_1 = name of your .m2 file + .mdx (sword_2h_artifactsoulrend_d_03.mdx); ModelTexture_1 = color of your weapon (mine will be sword_2h_artifactsoulrend_d_03_red); InventoryIcon = the name of the Icon if you downloaded one (inv_sword_2h_artifactsoulrend_d_03). Everything else can be left blank or 0.

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/5.png]]

Save this into your servers dbc folder and open heidisql.

# Server Side

In HeidiSQL open **item_template**  -> **Data** -> **Show all**

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/6.png]]

look for a weapon you want to duplicate, it's better if they match the criteria of the weapon you just downported = (Artifactsoulrend is 2h Sword) so you duplicate a existing 2h sword aswell. Then you just change the "displayid" to the one in ItemDisplayInfo.dbc and (re)start your server after saving it.

# Client Side

I suppose you know how you make a MPQ already (explained countless time) but i'll explain it quickly again.

Open MPQEditor and create a new MPQ, name it patch-4.mpq and hit next until you're in the MPQ. From there you create new Folders called "DBFilesClient" ; "item"; "interface"

Make sure they are separate folders, from there you drag and drop "all" the new dbc files from your Server into DBFilesClient.

ItemDisplayInfo.dbc in DBFilesClient

then in the "item" folder create a subfolder called "objectcomponents" and put your weapon folder in there.

your weapon folder in item\objectcomponents

create another subfolder in "interface" called "icons" and put your icon that you just downloaded in there.

your icon in interface\icons.

Delete your wow Cache and add your new item, drag it into your weapon slot and it should look very beautiful!

![[7.jpg]]

Invisible = didn't convert with TXID First and then Multi Converter

Weird texture = wrong name in TextureVariation_1

No animation = not everything put into your mpq patch

Crash = ??? maybe wrong name in ModelName_1 or wrong ID used in Heidisql IDEK

Green particles = not everything put into your mpq patch

# Credits

- **Author**: Tyrallis
- [Model Changing](https://model-changing.net/index.php?app=tutorials&module=tutorials&controller=view&id=156)

#rewrite 