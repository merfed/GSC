- **Authors**: Cryect, Schlumpf
- **Syntax**: `ModelSwamp.exe <map filename> <old filename> <new filename>`

Replaces a model filename with another one of the same or less length in an ADT.

# Versions

| Name      | Filesize                       | Author   | Source ? | Notes |
| --------- | ------------------------------ | -------- | -------- | ----- |
| ModelSwap | 5 KB (Source)<br />44 KB (exe) | Cryect   | ✔️       |       |
| ModelSwap | 6 KB (Source)<br />50 KB (exe) | Schlumpf | ✔️       |       |

The only notable changes in *Schlumpf's* version is a macro for arguments:

```cpp
#define DESCRIPTION "Replaces a model filename with another one of the same or less length in an ADT."
#define ARGUMENTS "<map filename> <old filename> <new filename>"

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