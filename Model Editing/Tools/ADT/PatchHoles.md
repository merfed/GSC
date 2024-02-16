- **Author**: Cryect, Schlumpf
- **Syntax**: `PatchHoles.exe <map filename>`

Removes all holes in the terrain.

# Versions

| Name       | Filesize                       | Author   | Source ? | Notes |
| ---------- | ------------------------------ | -------- | -------- | ----- |
| PatchHoles | 2 KB (Source)<br />41 KB (exe) | Cryect   | ✔️       |       |
| PatchHoles | 2 KB (Source)<br />48 KB (exe) | Schlumpf | ✔️       |       |
| PatchHoles | 159 KB (exe)                   |          | ❌       | Glowing Mushroom      |

The only notable change in *Schlumpf's* version is a macro for arguments:

```cpp
#define DESCRIPTION "Removes all holes in the terrain."
#define ARGUMENTS "<map filename>"

#define USAGE( minimumArguments, argc, argv ) \
	if( argc < minimumArguments + 1 ) \
	{	 \
		printf( "  %s\n", argv[0] ); \
		printf( "    " DESCRIPTION "\n\n" ); \
		printf( "    Usage: \"%s " ARGUMENTS "\"\n", argv[0] ); \
		printf( "    Built at: " __DATE__ "\n" ); \
		return -1; \
	}
	
FILE *Input;
```
