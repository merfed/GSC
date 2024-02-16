_Take a Shadowlands model and downport to Wotlk including M2's with Skels_


**What I will assume you know for this tutorial.**

- How to acquire files from CASC or Wow.tools
- Your way around the 010 Editor and have the relevant template
- Adding files to MPQ
- Editing the correct DBC files to add model to client
- How to use blender to decrease poly count if required

**Tools you need**

- **[M2Mod 9.0.0](https://bitbucket.org/suncurio/m2mod/src/9.x/)**
- [My MultiConverter fork](https://github.com/callumhutchy/MultiConverter/releases/latest)
- The most recent listfile.csv in the same directory as both of the two previous programs

# Step 1 - TXID Removal

For this step you can use any TXID removal method you want.

This step can also be done at any point before the MultiConverter step but it's just easier to do it now and not forget it.

I will get round to reimplementing the TXID removal that MultiConverter 3.6 has in my version, at which point you won't be reading this step

![[3rwbwf9f.bmp]]

![[5v73wn9a.bmp]]

Sylvanasshadowlands3 is weird and M2Mod requires her Skel to be renamed to sylvanas.skel, I haven't seen another skel model with this issue.

# Step 2 - Convert to M2i

![[e3hdoumr.bmp]]

Load the m2 you want to converter into M2Mod and click Go!

## Option Step

You now have the model in m2i format, this is the stage where you would decrease the poly count and edit submeshes if necessary. 

The max poly count for a model is 21845 in wotlk, probably best to check how many it has before you run into issues later on.

This guide will give you some idea of what to do [HD character model triangle reduction](https://model-changing.net/index.php?app=tutorials&module=tutorials&controller=view&id=96)

# Step 3 - Convert Back to M2

![[dea2sjo2.bmp]]

Whether you or not you have forayed into Blender it's now time to convert back to M2, just Preload and Go! once more.

You will now have an Export folder inside the original model folder, in my example I have an extra skel from before which I will delete now because MultiConverter uses the model name to find the skel.

![[dcnnpj6e.bmp]]

# Step 4 - Change Skin Names

To avoid skin errors we must rename the LOD skin files into normal skin files, however many LOD files there are rename them to be in ascending order after the original skin file. To produce something like below.

![[6gcr7mzm.bmp]]

# Step 5 - Edit M2 Number of Skin Profiles

Now we need to go into 010 and change the number of skin profiles to be 4 or however many skins you now have.

We haven't converted the file yet so you'll need to run the template at the offset 0x8

![[vhhzvr8g.bmp]]

Open up the Template Results and find the entry relating to number of skin profiles and change the value of 1 to your number.

![[zcnlu38t.bmp]]

# Step 6 - MultiConverter

All we have to do now is convert the M2 to Wotlk format

This step will work for models that have skels and ones that don't.

If the model has a skel you will see the size of the m2 drastically increase once it's converted whereas when there is no skel it barely changes.

![[hkbw832b.bmp]]

Drag the M2 into MultiConverter and click Fix, for one file the conversion should be very quick.

![[muf8i27a.bmp]]

The size has increased so if the green progress bar didn't give it away we have now put the skel back into the m2.

![[mm4nlwhg.bmp]]

# Step 7 - Add to MPQ and DBC Editing

Now add the converted files to the MPQ and edit the correct DBCs, [@Tyrallis](https://model-changing.net/index.php?app=core&module=members&controller=profile&id=14615) has a guide on how to do this [Retroport to WOTLK Update-1](https://model-changing.net/index.php?app=tutorials&module=tutorials&controller=view&id=153)

# Step 8 - Admire Ingame

![[ogg8gu1t.bmp]]

# Original Credits

- **Author**: callumhutchy
- [Model Changing](https://model-changing.net/index.php?app=tutorials&module=tutorials&controller=view&id=157)