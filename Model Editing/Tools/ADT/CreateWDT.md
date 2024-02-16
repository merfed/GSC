- **Authors**: Cryect (Vanilla, BC), Schlumpf (Wrath)

| Name       | Filesize                      | Author           | Source ? | Notes                                                                   |
| ---------- | ----------------------------- | ---------------- | -------- | ----------------------------------------------------------------------- |
| CreateWDT  | 11 KB (exe)<br/>2 KB (Source) | Cryect           | ✔️       | <span class="vanilla">Vanilla</span>                                                                        |
| CreateWDT  | 18 KB (exe)<br/>2 KB (Source) | Schlumpf         | ✔️       | <span class="wrath">Wrath</span>                                                                        |
| CreateWDTD | 24 KB (exe)                   |                  | ❌       | Debug version, pretty sure this is just all commented code uncommented. |
| CreateWDT  | 153 KB (exe)                  | Glowing Mushroom | ❌       | <span class="bc">BC</span>                                              |

The only notable changes in *Schlumpf's* version is a macro for arguments:

```cpp
#define DESCRIPTION "Makes a WDT file telling that the specified ADT tiles are present."
#define ARGUMENTS "<MapName> <LowerX> <LowerY> <UpperX> <UpperY>"

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