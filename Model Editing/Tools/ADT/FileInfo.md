- **Authors**: Cryect, Schlumpf, Snobaste
- **Syntax**: `FileInfo.exe <adt filename>`

# Versions

| Name         | Filesize                        | Author           | Source ? | Notes                                |
| ------------ | ------------------------------- | ---------------- | -------- | ------------------------------------ |
| FileInfo     | 6 KB (Source)<br/>44 KB (exe)   | Cryect           | ✔️       | <span class="vanilla">Vanilla</span> |
| FileInfo     | 6 KB (Source)<br/> 50 KB (exe)  | Schlumpf         | ✔️       | <span class="wrath">Wrath</span>     |
| FileInfo     | 334 KB (exe)                    | Glowing Mushroom | ❌       | <span class="bc">BC</span>           |
| FileInfo     | 6 KB (source)<br />495 KB (exe) | Snobaste         | ✔️       | <span class="wrath">Wrath</span>     |
| FileInfo-Alt | 587 KB (exe)                    | Snobaste         | ❌       | <span class="wrath">Wrath</span>     |

The only notable changes in *Schlumpf's* version is a macro for arguments:

```cpp
#define DESCRIPTION "Saves info about an ADT into a txt file."
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