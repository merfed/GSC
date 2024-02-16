- **Authors**: Cryect, Schlumpf
- **Syntax**: `MakeMap.exe <map name> <xOff> <yOff> <tWidth> <tHeight>`

Combines multiple .raw maps made by Noggit into one big one.

# Versions

| Name    | Filesize                       | Author   | Source ? | Notes |
| ------- | ------------------------------ | -------- | -------- | ----- |
| MakeMap | 2 KB (Source)<br />42 KB (exe) | Cryect   | ✔️       |       |
| MakeMap | 2 KB (Source)<br />48 KB (exe) | Schlumpf | ✔️       |       |
| MakeMap | 157 KB (exe)                   |          | ❌       | Glowing Mushroom      |

The only notable changes in *Schlumpf's* version is a macro for arguments:

```cpp
#define DESCRIPTION "Combines multiple .raw maps made by Noggit into one big one."
#define ARGUMENTS "<map name> <xOff> <yOff> <tWidth> <tHeight>"

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
