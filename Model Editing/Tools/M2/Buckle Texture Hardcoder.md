- **Author**:
- **Syntax**:

This script changes the texture type of a belt buckle m2 to "hardcoded", so you can attach it as a spell in WotLK.

It copies the name of your current model and creates a texture path with the same name. If your model is called "`Buckle_pinkunicorn`" it will create a path called "`Item\ObjectComponents\Waist\buckle_pinkunicorn.blp`".
This script only works if your model has "BUCKLE_" at the start of its name.

If the model has multiple texture variations, just change its name and a different texture path will be created for that specific file. Example:
`Buckle_Leather_RaidMonk_N_01.m2` has 3 textures:

```
Buckle_Leather_RaidMonk_N_01.blp
Buckle_Leather_RaidMonk_N_01Blue.blp
Buckle_Leather_RaidMonk_N_01Red.blp
```

If you wish to have all 3 variations, copy the model and change the name of its copies to "`Buckle_Leather_RaidMonk_N_01Blue.m2`" and "`Buckle_Leather_RaidMonk_N_01Red.m2`" so the path matches.

# Usage

- Put the models you want to modify inside the folder called "*Models*".
- Run `MassBuckleTextureHardcoder.bat` and wait.

# Requirements

- Requires 010 editor.

To make this script work there must be an entry for 010 editor in the environment variables:
- Right click My Computer -> Properties -> Advanced System Settings -> Environment Variables -> Path
- Click Edit
- Add your 010 Editor directory to the list separated from the rest of the entries by a `;`

# Notes

- This script can read all the subfolders inside "models" and modify every M2 file inside of them.
- This script only affects M2 files. If it finds another filetype inside "models" it won't touch it.
- Your model must have "buckle_" at the start of the file or it will be skipped.

# MassBuckleTextureHardcoder.bat

```
@echo off
echo ###### Buckle Texture Hardcoder ######

REM ////// Uppercase to lowercase (IMPORTANT, or script won't work)
@echo off
setlocal enableDelayedExpansion
pushd Models
for %%f in (*.m2) do (
set "filename=%%~f"
for %%A in (a b c d e f g h i j k l m n o p q r s t u v w x y z) do (
set "filename=!filename:%%A=%%A!"
)
ren "%%f" "!filename!" >nul 2>&1
)
endlocal

REM ////// Start counting how many files are going to be converted //////
set countmodels=0
for /r Models\ %%i in (buckle_*.m2) do set /a countmodels+=1

REM ////// Remove path of each file while printing on screen //////
set filename= %%~nxi

REM ////// Start converting //////
for /r Models\ %%i in ("buckle_*.m2") do (
REM ////// "%%~nxi" is the filename without path //////
echo Converting: %%~nxi
010editor "%%i" -script:"BuckleTextureHardcoder.1sc" "%%i" -nowarnings -noui
)

REM ////// Convertion ends //////

echo -----------------------------------------------

REM ////// Show ammount of files converted //////

if %countmodels% == 1 (
	echo 1 model successfully processed.
) else (
	echo %countmodels% models successfully processed.
)
pause
```

# Versions

| Name                   | Filesize      | Author | Source ? | Notes |
| ---------------------- | ------------- | ------ | -------- | ----- |
| BuckleTextureHardCoder | 3 KB (Source) |        | ✔️         |       |