- **Author**: Schulmpf
- **Syntax**: `RaiseTerrain.exe <map filename> <difference>`

Raises all terrain.

# Versions

| Name         | Filesize                       | Author   | Source ? | Notes         |
| ------------ | ------------------------------ | -------- | -------- | ------------- |
| RaiseTerrain | 3 KB (Source)<br />48 KB (exe) | Schlumpf | ✔️       |               |
| RaiseTerrain | 3 KB (Source)<br />56 KB (exe) | Schlumpf | ✔️       | *Alt* version |

The only notable changes between the two versions from *Schlumpf* is the *alt* version does not feature a macro for arguments:

```cpp
#define DESCRIPTION "Raises all terrain."
#define ARGUMENTS "<map filename> <difference>"

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