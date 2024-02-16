- **Authors**: Cryect, Schlumpf
- **Syntax**: `MapMover.exe <OldMapName> <LowerX> <LowerY> <UpperX> <UpperY> <NewMapName> <OffsetX> <OffsetY>`

Moves ADT tiles according to the given parameters. Needs to have [[OffsetFix]] in the same directory.

# Versions

| Name     | Filesize                       | Author   | Source ? | Notes |
| -------- | ------------------------------ | -------- | -------- | ----- |
| MapMover | 1 KB (Source)<br />10 KB (exe) | Cryect   | ✔️       |       |
| MapMover | 2 KB (Source)<br />17 KB (exe) | Schlumpf | ✔️       |       |
| MapMover | 208 KB (exe)                   |          | ❌       | Glowing Mushroom      |

The only notable changes in *Schlumpf's* version is a macro for arguments:

```cpp
#define DESCRIPTION "Moves ADT tiles according to the given parameters.\n    Needs to have \"OffsetFix\" in the same directory."
#define ARGUMENTS "<OldMapName> <LowerX> <LowerY> <UpperX> <UpperY> <NewMapName> <OffsetX> <OffsetY>"

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
