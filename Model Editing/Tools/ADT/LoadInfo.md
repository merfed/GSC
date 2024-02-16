- **Authors**: Cryect, Schlumpf
- **Syntax**: `LoadInfo.exe <adt filename>`

Loads info from a txt file made by FileInfo back into the ADT.

# Versions

| Name     | Filesize                        | Author   | Source ? | Notes |
| -------- | ------------------------------- | -------- | -------- | ----- |
| LoadInfo | 9 KB (Source)<br />48 KB (exe)  | Cryect   | ✔️       |       |
| LoadInfo | 10 KB (Source)<br />54 KB (exe) | Schlumpf | ✔️       |       |
| LoadInfo | 338 KB (exe)                    |          | ❌       | Glowing Mushroom      |

The only notable changes in *Schlumpf's* version is a macro for arguments:

```cpp
#define DESCRIPTION "Loads info from a txt file made by FileInfo back into the ADT."
#define ARGUMENTS "<ADT filename>"

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