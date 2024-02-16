_Sync'd to version from 20 May 2014._

Warden data. Mostly encrypted.

- **Signature**: WRDN

# Structure

| Column | Field         | Type    | Notes                                                                                                  |
| ------ | ------------- | ------- | ------------------------------------------------------------------------------------------------------ |
| 1      | `hashID`      | String  | MD5 sum of the warden module. This field is 16 bytes, unlike regular WDB IDs.                          |
| 2      | `entryLength` | Integer | Record length.                                                                                         |
| 3      | `dataLength`  | Integer | Length of the next field. This field is always reclen-4 because there is no additional field after it. |
| 4      | `moduleData`  | String  | Encrypted                                                                                              |

 

