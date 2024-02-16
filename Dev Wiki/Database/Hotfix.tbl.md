_Sync'd to version from 17 May 2016._

The hotfix.tbl file was introduced in wod, it's used for sending hotfixes to the client, when you log in game. It's located in the Cache/ADB folder.

# Structure

## Header

| Offset | Type      | Description                     |
| ------ | --------- | ------------------------------- |
| `0x00` | `char[4]` | Identifier, XFTH for this file. |
| `0x04` | `uint32`  | Unknown, always 1               |
| `0x08` | `uint32`  | Timestamp in unix format        |
| `0x0C` | `uint32`  | Build version                   |

# Block

| Column | Field        | Type    | Notes                                                                 |
| ------ | ------------ | ------- | --------------------------------------------------------------------- |
| 1      | `Table_Hash` | Integer | 4-byte integer identifying the hash as found in the DB2 file's header |
| 2      | `Record_ID`  | Integer | 4-byte integer identifying the ID from the hotfixes/DB2               |
| 3      | `Timestamp`  | Integer | 4-byte integer identifying the timestamp in unix                                                                      |

- [DB2 Header List](https://github.com/TrinityCore/WowPacketParser/blob/master/WowPacketParser/Enums/DB2Hash.cs)
