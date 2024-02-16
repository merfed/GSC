- **Authors**: Cryect, Schlumpf, Gretchin
- **Syntax**: `AllWater.exe <map filename> [<level: 0>] [<flags: 20>]`
- **Syntax (Gretchin)**: `AllWater.exe <map filename> [<level: 0>], [<flags: 20>], [<opacity: 50>]`

Add flat water to a ADT.

# Liquid Types

## Build 5428 (Vanilla & BC), 1.12.1.5875

| Type              | Value |
| ----------------- | ----- |
| Water             | 1     |
| Ocean             | 2     |
| Magma             | 3     |
| Slime             | 4     |
| Naxxramas - Slime | 21      |

## Build 12340 (WotLK), 3.3.5a

| Type | Value                    |
| ---- | ------------------------ |
| 1    | Water                    |
| 2    | Ocean                    |
| 3    | Magama                   |
| 4    | Slime                    |
| 5    | Slow Water               |
| 6    | Slow Ocean               |
| 7    | Slow Magma               |
| 8    | Slow Slime               |
| 9    | Fast Water               |
| 10   | Fast Ocean               |
| 11   | Fast Magma               |
| 12   | Fast Slime               |
| 13   | WMO Water                |
| 14   | WMO Ocean                |
| 15   | Green Lava               |
| 17   | WMO Water - Interior     |
| 19   | WMO Magma                |
| 20   | WMO Slime                |
| 21   | Naxxramas - Slime        |
| 41   | Coilfang Raid - Water    |
| 61   | Hyjal Past - Water       |
| 81   | Lake Wintergrasp - Water |
| 100  | Basic Procedural Water   |
| 121  | CoA Black - Magma        |
| 141  | Chamber Magma            |
| 181  | Orange Slime             |

# Versions

- **Note**: One of these versions (or possibly missing entirely) was done by *Gretchin*.

| Name              | Filesize | Author           | Source ? | Notes                                                         |
| ----------------- | -------- | ---------------- | -------- | ------------------------------------------------------------- |
| AllWater-BC       | 162 KB   | Glowing Mushroom | ❌       | <span class="bc">BC</span>                                    |
| AllWater-PreWrath | 162 KB   |                  | ❌       | Might be the same as *AllWater-BC*                            |
| AllWater          | 43 KB    | Cryect           | ✔️       |                                                               |
| All Water (GUI)   | 570 KB   | Gretchin         | ❌       |                                                               |
| AllWater          | 49 KB    | Schlumpf         | ✔️       | This version is also credited to *Gretchin*, may be an error. |
| AllWater (WotLK)  | 43 KB    |                  | ❌       | <span class="wrath">Wrath</span>                              |
| AllWater_WotLK    | 469 KB   |                  | ❌       | <span class="wrath">Wrath</span>, this one *may* be *Gretchin's* CMD line version.                             |

The only notable additions to *Schlumpf's* version is a macro for arguments:

```cpp
#define DESCRIPTION "Adds a flat water layer at the given height or 0."
#define ARGUMENTS "<map filename> [<level: 0>] [<flags: 20>]"

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

#research