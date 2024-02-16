# Requirements

- WoW.Tools
- [[WDBX Editor]]
- [[MPQEditor]]
- [[Multi Converter]]
- 3.3.5a Server
- WotLK Client
- TXID
- [[Spell Editor]]
- HeidiSql
- 010 Editor

# Starting

Open your wow.tools, select the box with the best ping, click on the world icon after that -> World of Warcraft 9.1.5 bla bla bla

![[Z. Meta/Attachments/Model Editing/Guides/Retroport Wings (WotLK)/1.png]]

Now click on Models and search for "wings", we're going to use "capewingstiger".

It's better to change the export folder to the one you were already using so it all goes in one place (don't worry, they will create subfolders).

Use my settings and export as M2.

![[Z. Meta/Attachments/Model Editing/Guides/Retroport Wings (WotLK)/2.png]]

Now head to your exported folder, go to spells and slap that capewingstiger.m2 into TXID about 15 times. Click Fix.

Do the same now again, but use MultiConverter 3.3.0. Click Fix.

# Finding Missing Files from 010 Editor

Open `capewingstiger.m2` with 010 Editor, press CTRL + F and search for `blp`.

Make sure you're searching by text(t) (it's to the right of the search bar).

Now, wow.tools exported everything but they are not in the same folder. for example:

![[Z. Meta/Attachments/Model Editing/Guides/Retroport Wings (WotLK)/3.png]]

# Create the Spell

Enter your Database data, so it can connect to your Database.

Select Import/Export and Import every file that begins with Spell

![[Z. Meta/Attachments/Model Editing/Guides/Retroport Wings (WotLK)/4.png]]

After you're done with that, we make a "New Spell", we create it from an existing ID, i'm using the ID = 69188 since it attaches to your back already.

My new SpellID is 90008 since i already have some custom spells. 

Now listen very closely, this is IMPORTANT.

First go to Visual -> Kits & Effects and copy the first VisualKit

![[Z. Meta/Attachments/Model Editing/Guides/Retroport Wings (WotLK)/5.png]]

Now head to Base and delete "Spell Visual 1" and turn it to a 0

Go to Visual ->  Kits & Effects and Paste it there again. If the Paste option is greyed out, go to 69188 (rocket pack) and copy it from there.

![[Z. Meta/Attachments/Model Editing/Guides/Retroport Wings (WotLK)/6.png]]

Should look like this, click on Confirm. (**BEFORE GOING BACK CLICK ON "SAVE SPELL CHANGES"**)

Now we go back to 69188 (rocket pack) and copy the lower part. Go into your new spell and Paste it in Visual Kit Effects & Attachments. Confirm this too!

Our AttachmentID **HAS TO BE 12** since it will be attaching it to our Back, where wings should go to, right?

From there set all the things below to 0 or else you get a weird rotation, weird angles etc..

Weird Rotation:

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/7.png]]

Save Spell Changes once again.

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/8.png]]

# Adjusting Spell Manually

In HeidiSQL open the "spellvisualeffectname" table and click on "Data". Click on "Show all" and scroll to the bottom.

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/9.png]]

There should be a new Entry called "JetPack" or something else if you changed the name before.

We change the name to XuenWing and the FilePath to spells\capewingstiger.mdx and change everything else like i did or else they be too small (for my taste).

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/10.png]]

Go to your spell editor once again and click on "SAVE VISUAL MODIFICATIONS" they should all change to your manually edited entry.

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/11.png]]

Save Spell Changes once more and click on Import/Export, select Export and wait for all Tables to load, just click Export checked to DBC.

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/12.png]]

You can close the Spell Editor if you like to. Go into the folder of the Spell Editor and go inside of "Export". I sorted the files there by Date, so i know what i just changed, drag and drop these into your Server's DBC files.

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/13.png]]

Make sure they are the right Time, mine are from yesterday, but i changed it today (12.02) and my server couldn't find the spell xD.

# Making a Client-side Patch

Open MPQEditor and create a new MPQ, name it patch-4.mpq and hit next until you're in the MPQ. From there you create new Folders called "DBFilesClient"; "spells" ; "Creature" ; "item"

![[Z. Meta/Attachments/Model Editing/Guides/Retroporting to WotLK (Update 1)/14.png]]

Make sure they are separate folders, from there you drag and drop "all" the new dbc files from your Server into DBFilesClient.

Put all the files from your exported spell into the spell folder, then the siberiantigergod and pandarenserpentgod into "Creature".

![[15.png]]

then in the "item" folder create a subfolder called "objectcomponents" and put your shoulder folder in there.

![[16.png]]

If it looks like this, you're good. (no need to restart server since we only edited our mpq and no .dbc files).

Restart your Server, delete your Cache folder and type .cast 90009 (or the ID you used instead).

If you followed my steps correctly, you should look like this!

![[17.jpg]]

If it looks like this tho, you probably didn't add all the .blp files in your mpq patch.

![[18.jpg]]

# Credits

- **Authors**: Tyrallis, Stoneharry
- [Model Changing](https://model-changing.net/index.php?app=tutorials&module=tutorials&controller=view&id=154)