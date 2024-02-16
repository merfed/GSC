- **Author**: Schlumpf

- Up converts pre-8.1.5 <span class="bfa">BFA</span> **root** and **split** files to `filedataid` format.
- Down converts `post-filedataid` files (8.1.5 - 10.0.0 and up) so they can be MultiConverted to <span class="wrath">Wrath</span>.

# Usage

1. Open CMD
2. Point to the folder with the tools.
3. Folder with `listfile.csv`, folder for output, folder for adt files.
4. Example: `D:/input/down.exe D:/input/listfile.csv D:/output d:/input/*.adt`

> [!important] Important
> Due to WMO scaling (I think?) the down-converted files need to be updated (take the widest brush on 0 power and update everything) and save in Noggit or they will cause a crash.

