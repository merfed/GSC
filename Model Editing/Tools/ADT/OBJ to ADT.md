- **Authors**: Skarn, Koward

Takes the height coordinates of a `.obj` file and puts them into an `.adt` file of the same name. Launch `run.bat` to convert all files in a directory.

# Process all ADTs in a Directory

```
@echo off

for %%i in (*.adt) do java -jar OBJ_to_ADT.jar "%%i"

pause
```

# Versions

| Name       | Filesize                       | Author | Source ? | Notes                                            |
| ---------- | ------------------------------ | ------ | -------- | ------------------------------------------------ |
| Obj_to_ADT | ?? KB (Source)<br />7 KB (jar) | Koward | ❌       | Version `1.0.1`, Java 7 version also             |
| Obj_to_ADT | ?? KB (Source)<br />7 KB (jar) | Koward | ❌       | Version `1.0.0`                                  |
| Source     | --                             | Koward | ✔️       | Changeset `d841d04`, unknown version ~ 2/19/2016 |
