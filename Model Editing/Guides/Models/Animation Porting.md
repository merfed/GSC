**Tools needed:**  
*ModIt  
*ChangeAnimations.py  
*PyM2  
*A Python Interpreter  
*Notepad++ or any other texteditor  
  
**Step 1: Find the correct Bones**  
  
Open ModIt, navigate to the correct model, then click View->Show model control, enable Bones, disable Render.  
Click Edit Model -> Edit Bones.  
Now search the Bones of head, shoulders and legs(if you enable a bone in Edit Bones, it will be colored):

![[4bb1ed1153d32_BoneStructure.jpg]]

**Step 2: Edit ChangeAnimations.py to your values**  
  
Open ChangeAnimations.py with your texteditor.  
line 3 and 4 define the filenames, inName is the Model, which has the Animations, and outName is the Model, which gets them.  
In line 57: _changeBones = (0,1,2,3,4)_ you can add bones which you want to be ported but not the bones depending on them.  
in line 69 to 88 you need to change the values of Dependent:  
eg: Change left shoulder animation of HuF to SkM  

Code:

```
if (Dependent(i,om2,16,ic) & Dependent(j,im2,10,jc)) & (Depth(i,om2) == Depth(j,im2)):
			ChangeAnims(i,j)
			break
```

becomes  

Code:

```
if (Dependent(i,om2,16,ic) & Dependent(j,im2,9,jc)) & (Depth(i,om2) == Depth(j,im2)):
			ChangeAnims(i,j)
			break
```

if you want change the left shoulder animation of HuF to the Arakkoa one.  
  
In line 114 you can set the output folder.  
  
**Step 3: Run ChangeAnimations.py**  
  
To run ChangeAnimations.py you need to have a Python Interpreter installed.  
Then ChangeAnimations.py has to be in the same folder like m2.py, wowfile.py etc. from PyM2.  
Under Windows, if you've installed a Python Interpreter *.py should automatically be attached to the Interpreter,  
so you can double-click on the file and it'll run.  
Under Linux you need to add a shebang:  

Code:

```
#! /usr/bin/python
```

(something like that)  
and than execute the file.  
Under MacOS I've no idea :P  
Now your animation port is finished and you can add your files to your MPQ ;D  
  
**Appendix:**  
Some model information (will be updatet):

```
  
Worgen:  
rleg: 6  
lleg: 7  
rshoulder: 14  
lshoulder: 13  
head: 10  
else: (0,1,2,3,4)  
  
Zombie:  
rleg: 6  
lleg: 5  
rshoulder: 11  
lshoulder: 10  
head: 12  
else: (0,1,2,3,4)  
  
Ogre:  
rleg: 6  
lleg: 8  
rshoulder: 11  
lshoulder: 10  
head: 9  
else: (0,1,2,3,4)  
  
Arakkoa:  
rleg: 6  
lleg: 5  
rshoulder: 12  
lshoulder: 9  
head: 8  
else: (1,2,3,4)  
  
SkeletonMale:  
rleg: 5  
lleg: 6  
rshoulder: 11  
lshoulder: 10  
head: 9  
else: (0,1,2,3,4)  
  
HumanFemale:  
rleg: 5  
lleg: 6  
rshoulder: 17  
lshoulder: 16  
head: 10  
else: (0,1,2,3,4)
```

**Info**:  
To swap only one animation:  
In line 14 change:  

Code:

```
if (k.animId == n.animId) & (k.subId == n.subId):
```

to:  

Code:

```
if (k.animId == n.animId == YourANIMATION) & (k.subId == n.subId)
```

where YourANIMATION is your animid

# Credits

- Tigurius