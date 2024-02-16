- **Author**: Shgck

FBX to WMO converter.

It's a FBX to WMO/v17 (WotLK) converter, written in Python, supposed to be a good replacement for MirrorMachine when it's done. It uses the Autodesk FBX SDK and PyWMO.

This project is *discontinued*. The FBX format has too many differences from WMO that I can't convert them myself. It's not impossible, it's just too complicated : UV maps are set per polygon vertex and not control point, so UV mapping will appeared fucked up in WoW. Splitting the control points for every polygon vertex is a bad hack as it will fix the UV problems, but the WoW engine will render poorly the splitted model (shadows will appear very sharp and the model will be overall too bright, as every polygon will be actually separated from its neighbors). I've yet to hear about a solution (partial splitting doesn't seem to work too). The whole portal system is a mess to add too, so the models has to be outdoor as indoor zones with outdoor flags are badly rendered.

A binary has been built with cx_Freeze and put in the build directory. It isn't tested (I'm in internship so I can't test anything), but should work for most simple stuff. Don't mail me unless you really tried to make it work.

Finally, even if the whole thing is more or less a failure, thanks LIMEEE for your testing time.

# Installation

Download all the files in the build directory (cloning the repo is quicker).

If you want to compile it yourself, you will need (all for x86 arch if possible):

* Python 3.3
* Autodesk FBX SDK for Python 3.3
* cx_Freeze for Python 3.3

Then run setup.py. You may need to manually add some files from the SDK (I had to add fbxsip.pyd directly in the build directory).

# Usage

Drag your files on main.exe. On the CLI, use:

```
python main.py file.fbx
```

or if you feel adventurous:

```
python main.py file.wmo
```

Please follow these instructions or you'll quickly get into trouble :

* Use one texture per material, no more no less
* Don't use layered textures
* Always map correctly your materials.
	* isAllSame mapping won't work and other default settings won't work.
* WMO vertex limit per polygon is around 64k, don't go further.
* Don't split your vertices as it will drastically increase the vertex count.
	* For some reason, I have to split them myself to avoid UV fuckery ATM.
* Triangulate your model before exporting it. For some reason I can't do it myself.

If you're interested by more documentation / tips, tell me. I won't do it if no one show further interest.

# Config

You can create a config.json file next to main.py. Currently the following are used :

* **fallback_textures**: if I can't link a texture file to a material, it uses this path.
	* Should look like "`DUNGEONS\\TEXTURES\\BLABLA.BLP`".
* **pause_before_exit**: if "yes", the program will ask you to press Enter before exiting, letting you reading possible error messages or warnings.
* **bsp_leaf_max_size**: override the max number of polygons the generator can put in a BSP leaf.
	* **Default is 2000**: beyond that, it may solve some collision problem but it can create others.
	* Below that will cause only more collision pb I guess.

All parsed configs are visible from the `config.py` file.

# Tips

* When using a material with transparency, end the name with "`_tr`" (and the texture name too). It will set its blend_mode to 1.

# Links

* [Bitbucket](https://bitbucket.org/Shgck/meshugamh)