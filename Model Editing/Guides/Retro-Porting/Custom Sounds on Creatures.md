Well, let's see the simplest way to put custom sounds for your server, or lua scripts. (could also teach how to do that :))


# Requirements

- WDBX Editor
- Local Server

1. Organize your workplace

You may think it's stupid, but it's really useful to know where the tools will be where you'll be working.

2. We will start by making a folder that will be our patch, it can have any name but it IS **IMPORTANT** that it ends with .MPQ, something like this.

![[Z. Meta/Attachments/Model Editing/Guides/Custom Sounds on Creatures/1.png]]

3.  Now we are going to work on the parts of our patch.  
       a) our patch will consist of two folders.

![[Z. Meta/Attachments/Model Editing/Guides/Custom Sounds on Creatures/2.png]]

It is important that within the Sound folder, you make another folder, it can have any name, it is only to keep an order since that is what the DBC directory requests.

![[Z. Meta/Attachments/Model Editing/Guides/Custom Sounds on Creatures/3.png]]

We are going to prepare the DBFilesClient folder, for this, we have to move the DBC file whose name is SoundEntries.dbc

4.  Now let's get the sounds as such.

I recommend for creatures/mounts, to use the wowhead sounds. But if this is not what you want, you can download any .mp4 sound and convert it to .ogg in any online converter.   

When you have the sound, it will move it to the subfolder inside the Sound folder that is in our patches folder.

![[Z. Meta/Attachments/Model Editing/Guides/Custom Sounds on Creatures/4.png]]

5. Start work with the .DBC file  
	- We open the .DBC with any DBC editor, personally I recommend WDBX Editor.  
		- In column 1, the ID will go.  
		- in column 3, the name will go, it can be anything.  
		- in column 4 the name of the file will go, it is important that you put the type of file at the end. Like this:  ![[Z. Meta/Attachments/Model Editing/Guides/Custom Sounds on Creatures/5.png]]
		- in column 24 we will put the path of our sound, so that it looks something like this: ![[Z. Meta/Attachments/Model Editing/Guides/Custom Sounds on Creatures/6.png]]
		- We save the .dbc files

6. To finalize and test our sounds in the game  
	 - We move our patch .dbc file to our local server folder, and reboot.  
  
7. Let's try it!  you can use the `.play (id)` command to play the sound on the server. if all went well, it should be heard. if it says that the sound does not exist make sure you have moved the .dbc file to your local server files.

8. Now that we hear our sound on the server, we can start working on our creature. If your sound did not play, you need to review the steps above.  
	- To start working on the .dbc files, we need to move three new files to our patch: CreatureModelData.dbc, CreatureDisplayInfo.dbc, CreatureSoundData.dbc, these three files will go in the DBFilesClient folder.  
	- Let's start working with CreatureSoundData.dbc  
		- We will duplicate the last row, and to start modifying we have to know the meaning of each column.  
		- To know what each column means, we can use the WDBX editor, I will also give some instructions so that you know what we are talking about.  
			- Column 1: ID  
			- Column 4: Here you will put the ID of the sound you want to play when the creature suffers an injury.  
			- Column 8: Here you will put the ID of the sound you want to play when the creature is standing still, like the roar of the spectral tiger.  
			- Column 10: Here you will put the ID of the sound you want to play when you start a fight with the pet (when calling its aggro)  
			- Column 12: Here you will put the ID of the sound you want to play when the creature plans.  
			- Column 14-18: Here you will put the ID of the sound you want to play when the creature stirs.  
			- Column 19-22: The sound you want to play when the creature hits will go here.  Strongly recommending that you use the WDBX Editor if you have any questions on the tables.  
	- When you made the changes you think necessary to the CreatureSoundData.dbc file you will save it and close it.

9. Now we will make some changes to CreatureDisplayInfo.dbc, and CreatureModelData.dbc  
	- We will start by checking a column of CreatureDisplayInfo.dbc  
		- We will check that in column 12, there is the number 0, this is so that it takes the sound directly from CreatureModelData.  
	- We will now make a change to the CreatureModelData.dbc   
		- In column 13, we'll put the CreatureSoundData id and then save the file.  
  
10. Now, we transform into our creature, and listen to the new sounds!:)

# Credits

- **Author**: Lucky
- [Model Changing](https://model-changing.net/index.php?app=tutorials&module=tutorials&controller=view&id=155)