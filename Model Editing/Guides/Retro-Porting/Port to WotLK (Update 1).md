# Requirements

- [[CASCExplorer]]
- [[WDBX Editor]]
- [[MPQEditor]]
- [[Multi Converter]]
- 3.3.5a Server
- WotLK Client
- TXID
- 010 Editor

# Folder Structure

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/1.png]]

# Starting

Open CASCExplorer and click on File -> Open Online Storage -> WoW Retail -> Select the only Build there is and wait.

![[2.gif]]

Now we need to decide on what we want to retroport, I think that i'm going to Retroport the [Vicious War Spider](https://www.wowhead.com/item=184014/vicious-war-spider). On the Quick Facts tab, it shows us it's Icon Name, but we just copy the part after inv_.

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/3.png]]

In CASCExplorer we head to Creatures and look for `viciousalliancespider`

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/4.png]]

We extract every file there. Now in our Export folder we open TXID and put viciousalliancespider.m2 about 15 times in there, then click FIX

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/5.png]]

We then open `viciousalliancespider.m2` with 010 Editor. press CTRL + F and change the search type to text(t)

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/6.png]]

There you can scroll through the results, we then look for every .blp in there, but since this .m2 file is weird, it shows 20+ occurences of .blp, but we don't need those since they don't have a path.  
(You can also double-check on [wow.tools](https://wow.tools/files/#search=viciousalliancespider&page=1&sort=1&desc=asc), just search up viciousalliancespider and click on the "I".)

We actually have every file we need, so we open Multi Converter 3.3.0 and put every file in there, don't worry if only one file shows up in there, that's completely normal. Click on Fix again.

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/7.png]]

We can close Multi Converter and TXID (if you didn't already) and open WDBX Editor. Select CreatureModelData.dbc and CreatureDisplayInfo.dbc from your Server's dbc files. Mine are located in \server\data\dbc.

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/8.png]]

We open both with WDBX Editor and Select WOTLK from "Load Definition"

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/9.png]]

We start in CreatureDisplayInfo.dbc by making a new Line, Right-Click -> Insert Line. 

Your ID and ModelID have to be _unique_. Mine are as follows: ID= 32764;  ModelID= 10005. We then only change CreatureModelScale = 1 (how big your Creature will be) ; CreatureModelAlpha= 255 (1 = almost invisible; 255= no transparency). Now we change our TextureVariation_1 to viciousalliancespider.

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/10.png]]

Now we can save CreatureDisplayInfo.dbc and make sure it's saved in your server.

Open CreatureModelData.dbc now and go to ID 30 (it's Creature\MineSpider). Right-Click -> Copy Line, then Right-Click -> Insert Line -> Right-Click -> Paste Line.

It should look like this now.

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/11.png]]

don't worry, i changed my ID to 10006 because ID 10005 was already in use, but somehow i deleted the Line. you can still use 10005.

We then only change "ModelName" to our path, our path is _Creature\viciousalliancespider\viciousalliancespider.mdx_ .

.mdx because else wow can't regognize your Creature.  
We're done now with server sided.  
Now we do client sided, which means we need to make a patch.  
Open MPQEditor and create a new MPQ, name it patch-4.mpq. In your MPQ, we need to make 2 folders. 

Right-Click on the first file and make a new folder called "DBFilesClient", now do the same thing again but make sure they are separated, the other folder is calles "Creature".

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/12.png]]

in Creature we can drag and drop our viciousalliancespider folder in there.

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/13.png]]

We now head to DBFilesClient and drag-and-drop our CreatureModelData.dbc and CreatureDisplayInfo.dbc in there.

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/14.png]]

Now we are done with everything, just start your server again and morph into 32764.

_ALWAYS DELETE YOUR CACHE_

![[15.jpg]]

![[16.jpg]]

If it has cube texture = wow can't find the path you used (typically a typing error; capital letters; no .mdx at the end; no backslash used)

If it has green texture = wow can't find the correct texture (used wrong .blp in CreatureDisplayInfo.dbc like using viciousalliancespider_armor instead of viciousalliancespider)

If it is invisible = have you ran it through both converters? did you accidentally changed  CreatureModelAlpha to 0?

If it crashes = is your ID in CreatureDisplayInfo.dbc populated? Did you make sure your creature uses the same ModelID?


# Credits

- **Author**: Tyrallis
- [Model Changing](https://model-changing.net/index.php?app=tutorials&module=tutorials&controller=view&id=153)