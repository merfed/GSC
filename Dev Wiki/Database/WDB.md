_Sync'd to version from 23 November 2020._

The WDB files are found inside the WDB folder. The client caches data it receives from the server. This is mainly done to reduce network traffic.

Not all WDB caches are saved to disk. This is defined in the client by the DBCache's constructor which contains a persistent parameter.

# Header

- WDB files < 1.6: Header length is 16 bytes
- WDB files >= 1.6: Header length is 20 bytes (Verified till 1.9.4)
- WDB files >= 3.0.8-9506: Header length is 24 bytes

| Offset | Type      | Description                                                                                                                        |
| ------ | --------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `0x00` | `char[4]` | **Identifier**: Depends on the WDB file, will be explained later (reversed!)                                                       |
| `0x04` | `uint32`  | **Client Version**: Version of the client (lo -> hi encoding)                                                                      |
| `0x08` | `char[4]` | **Client Locale**: The locale of the client (reversed) >= Vanilla (1.6.0)                                                          |
| `0x0C` | `uint32`  | **Record Size**: Size of the internal structure not of the file contents                                                           |
| `0x10` | `uint32`  | **Record Version**: A manually updated versioning field - except for WoWCache.wdb which is read from `WardenCachedModule::Version` |
| `0x14` | `uint32`  | **Cache Version**: A packet based versioning field set via `SMSG_CLIENTCACHE_VERSION` >= WotLK (3.0.8)                             |

# WDB Files

| File               | Signature | Version                                        |
| ------------------ | --------- | ---------------------------------------------- |
| ArenaTeamCache     | WATM      | WotLK ... Cata                                 |
| BattlePetNameCache | WBPM      | Mists ... WoD (Not seen > 6.2.4)               |
| CreatureCache      | WMOB      |                                                |
| DanceCache         | WDAN      | WotLK ... Cata                                 |
| GameObjectCache    | WGOB      |                                                |
| GuildStatsCache    | WGLD      |                                                |
| ItemCache          | WIDB      | <= WotLK                                       |
| ItemNameCache      | WNDB      | <= WotLK                                       |
| NameCache          | WNAM      |                                                |
| NPCCache           | WNPC      |                                                |
| PageTextCache      | WPTX      |                                                |
| PetitionCache      | WPTN      |                                                |
| PetNameCache       | WPNM      |                                                |
| QuestCache         | WQST      |                                                |
| RealmCache         | WRLM      | Mists ... WoD (6.0.1.18179, Not seen >= 6.2.3) |
| [[WOWCache]]           | WRDN      |                                                |
