- **Authors**: Cryect, Schlumpf
- **Syntax**: `CoverWithWater.exe <map filename> [<depth factor>]`

> [!Warning] Not stable.

Covers the whole ADT by water that is above the terrain.

# Versions

| Name               | Filesize | Author   | Source | Notes |
| ------------------ | -------- | -------- | ------ | ----- |
| CoverWithWater     | 6 KB     | Cryect   | ✔️       |       |
| CoverWithWater_alt | 6 KB     | Schlumpf | ✔️       |       |

The only notable changes in *Schlumpf's* version is a macro for arguments:

```cpp
#define DESCRIPTION "[NOT STABLE] Covers the whole ADT by water that is above the terrain.."
#define ARGUMENTS "<map filename> [<depthfactor>]"

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