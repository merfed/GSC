- **Author**: Cryect, Schlumpf
- **Syntax**: `OffsetFix.exe <map filename> [<z change>]`

Fixes several offsets that are wrong after moving an ADT and can move it upwards.

# Scripts

## Run OffsetFix on all ADTs in Directory

```bat
@echo off
for %%i in (*.adt) do OffsetFix.exe "%%i"
pause
```

# Versions

| Name      | Filesize                       | Author   | Source ? | Notes                                |
| --------- | ------------------------------ | -------- | -------- | ------------------------------------ |
| OffsetFix | 4 KB (Source)<br />15 KB (exe) | Cryect   | ✔️       | <span class="vanilla">Vanilla</span> |
| OffsetFix | 5 KB (Source)<br />21 KB (exe) | Schlumpf | ✔️       |                                      |
| OffsetFix | 168 KB (exe)                   |          | ❌       | Glowing Mushroom                                     |

The only notable additions to *Schlumpf's* version is a macro for arguments:

```cpp
#define DESCRIPTION "Fixes several offsets that are wrong after moving an ADT and can move it upwards."
#define ARGUMENTS "<map filename> [<z change>]"

#define USAGE( minimumArguments, argc, argv )
	if( argc < minimumArguments + 1 )
	{
		printf( "  %s\n", argv[0] );
		printf( "    " DESCRIPTION "\n\n" );
		printf( "    Usage: \"%s " ARGUMENTS "\"\n", argv[0] );
		printf( "    Built at: " __DATE__ "\n" );
		return -1;
	}
```