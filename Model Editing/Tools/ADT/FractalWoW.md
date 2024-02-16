- **Author**:

Generate ADTs from an image. The image should be divisible by 256, if not the tool will repeat the image after reaching it's borders. Only the red value of the image will be taken into consideration when reading the file, while 0 (black) is the lowest, and 255 (white) is the highest value.

# Options

**Height Multiplier**
Takes integer and float values and multiplies the height of the image. Allows easier creation of shallow or steep cliffs.

**X1 to X2, Y1 to Y2**
Defines the area on the WDT you want to generate. So when you want to create a map named TestMap and you want to use the ADTs `TestMap_0_0` to `TestMap_10_5` you'd enter:

**X1**: 0, **X2**: 10, **Y1**: 0, **Y2**: 5

It can only generate rectangles.

**Map name**
The name of the map that is used as the filename.

**Base Image**
The image you want to use for generation of the ADTs.  Accepts png, jpg, bmp, gif (possibly).

**Use Coordinates on Image**
This controls whether or not the tool used the x1-2, y1-2 coordinates on the image. If you check this and start at something other than **X1**:0 or **Y1**:0 you will not start at the top left of the image.

This might be useful if you want to partially generate small chunks ofa big world map or regenerate only a single ADT in the middle of an image.

# Notes

The ADTs are generated based on the one ADT in the input folder. Don't remove it and don't change it. This tool isn't very flexible in reading ADTs, so it won't work correctly with other ADTs. As of version `0.4`, this shouldn't be the case anymore. Name your input ADT `Adventuria_20_20.adt`, and it *should* read it.

[[OffsetFix]] will break ADTs generated with this tool.

Normal maps are **not** generated, use [[Noggit]] for that. Change the brush size to max with no speed, and then paint. All normals will get created. 

Water is fixed on the ADT, so every ADT has water.

# Changelog

- **0.4**
	- More support for other ADTs as base, untested.
- **0.3**
	- Allow relative positioning.
- **0.2**
	- Allow generation of multiple ADTs based on a single image.
- **0.1**
	- Allow generation of one ADT based on one image.

# Versions

| Name             | Filesize    | Author | Source ? | Notes         |
| ---------------- | ----------- | ------ | -------- | ------------- |
| FractalWoW `0.1` |             |        |          | *Do not have* |
| FractalWoW `0.2` |             |        |          | *Do not have* |
| FractalWoW `0.3` |             |        |          | *Do not have* |
| FractalWoW `0.4` | 42 KB (exe) |        | ❌       |               |

#missing_files 