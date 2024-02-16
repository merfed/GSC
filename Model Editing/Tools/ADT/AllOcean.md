- **Author**: Cryect ?, Schlumpf
- **Syntax**: `AllOcean.exe <map filename> [<depth factor>]`

Fills the ADT with ocean 3.* style where no terrain is above 0.

# Versions


- AllOcean3.0 (6 KB)
- AllOcean3.0_Alt (7 KB) - *Schlumpf*

The only notable additions to *Schlumpf's* version is a macro for arguments:

```cpp
#define DESCRIPTION "Fills the ADT with ocean 3.* style where no terrain is above 0."
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