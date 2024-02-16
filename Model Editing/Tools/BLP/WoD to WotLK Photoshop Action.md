- **Author**: Inico
- **Syntax**:

Press alt+F9 to open the action window. Click on the upper right icon and choose "load actions...". Select the action file and load it.
For batch conversion go to File> Automate> Batch... and choose the required action and folder.

I made some Photoshop actions that automatically resize, move and crop the WoD character textures to make them work correctly in WOTLK. You can run them in a batch to convert multiple textures with just 1 click.
With this method you can retro-port almost every hd character model in a few minutes (you still need to modify the UV inside the M2 file but that's easy).

- The "Body texture" action automatically copies the face region, resizes and moves it to the lower left corner of the body texture. Then saves and closes the file.
- The "Face Texture" (upper and lower) action simply resizes and cuts the face files. You must duplicate each wod face texture and apply the upper action to to one of them and the lower action to the other (Wod only has 1 face texture file but wotlk has two, one for the upper half and other for the lower half).
- The facial hair action is similar to the face action. Also works for scalps. It cuts and resizes the texture but preserves transparency for facial hair textures (like beards or eyebrows).
- Tauren, Pandaren, Draenei and undead have some extra stuff (like tails, hooves, bones) where the head is supposed to be, so i made an action that cuts that region and saves it, so you can use it as an extra texture.

For batch conversion go to "file> automate> Batch...", choose the action and the folder you want and hit "OK".

Tested in Photoshop CS6. It should work in older versions, but i am not 100% sure.

**TIP**: Character textures in Lich King MUST be in INDEXED format to work. Remember to index them if you use blpconverter (command: BLPConverter.exe /FBLP_PAL_A8 "file").

# Versions

| Name                          | Filesize | Author | Source ? | Notes |
| ----------------------------- | -------- | ------ | -------- | ----- |
| WoD to WotLK Photoshop Action | 4 KB     | Inico  |          |       |
