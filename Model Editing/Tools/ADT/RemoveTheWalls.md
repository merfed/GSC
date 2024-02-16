- **Author**: Cryect, Schlumpf
- **Syntax**: `RemoveTheWalls.exe <map filename>`

Removes unpassable chunks of an ADT.

# Versions

| Name           | Filesize                      | Author   | Source ? | Notes |
| -------------- | ----------------------------- | -------- | -------- | ----- |
| RemoveTheWalls | 2 KB (Source)<br/>41 KB (exe) | Cryect   | ✔️       |       |
| RemoveTheWalls | 2 KB (Source)<br/>48 KB (exe) | Schlumpf | ✔️       |       |
| RemoveTheWalls | 159 KB (exe)                  |          | ❌       | Glowing Mushroom      |

The only notable difference in *Schlump's* version is a macro for arguments:

```cpp
#define DESCRIPTION "Removes unpassable chunks of an ADT."
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
```
