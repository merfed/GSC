_Sync'd to version from 2 June 2021._

NOTE: All SERVER opcodes are now uint16's, as of patch 4 (3807/0.9.0) Client opcodes are still uint32 as far as we know. 3.0.2 client opcodes: CMSG=ClientMessage, SMSG=ServerMessage!

|Name|Opcode|Description|
|---|---|---|
|[MSG_NULL_ACTION](https://wowdev.wiki/index.php?title=MSG_NULL_ACTION&action=edit&redlink=1 "MSG NULL ACTION (page does not exist)")|0x000||
|[CMSG_BOOTME](https://wowdev.wiki/index.php?title=CMSG_BOOTME&action=edit&redlink=1 "CMSG BOOTME (page does not exist)")|0x001||
|[CMSG_DBLOOKUP](https://wowdev.wiki/index.php?title=CMSG_DBLOOKUP&action=edit&redlink=1 "CMSG DBLOOKUP (page does not exist)")|0x002||
|[SMSG_DBLOOKUP](https://wowdev.wiki/index.php?title=SMSG_DBLOOKUP&action=edit&redlink=1 "SMSG DBLOOKUP (page does not exist)")|0x003||
|[CMSG_QUERY_OBJECT_POSITION](https://wowdev.wiki/index.php?title=CMSG_QUERY_OBJECT_POSITION&action=edit&redlink=1 "CMSG QUERY OBJECT POSITION (page does not exist)")|0x004||
|[SMSG_QUERY_OBJECT_POSITION](https://wowdev.wiki/index.php?title=SMSG_QUERY_OBJECT_POSITION&action=edit&redlink=1 "SMSG QUERY OBJECT POSITION (page does not exist)")|0x005||
|[CMSG_QUERY_OBJECT_ROTATION](https://wowdev.wiki/index.php?title=CMSG_QUERY_OBJECT_ROTATION&action=edit&redlink=1 "CMSG QUERY OBJECT ROTATION (page does not exist)")|0x006||
|[SMSG_QUERY_OBJECT_ROTATION](https://wowdev.wiki/index.php?title=SMSG_QUERY_OBJECT_ROTATION&action=edit&redlink=1 "SMSG QUERY OBJECT ROTATION (page does not exist)")|0x007||
|[CMSG_WORLD_TELEPORT](https://wowdev.wiki/index.php?title=CMSG_WORLD_TELEPORT&action=edit&redlink=1 "CMSG WORLD TELEPORT (page does not exist)")|0x008||
|[CMSG_TELEPORT_TO_UNIT](https://wowdev.wiki/index.php?title=CMSG_TELEPORT_TO_UNIT&action=edit&redlink=1 "CMSG TELEPORT TO UNIT (page does not exist)")|0x009||
|[CMSG_ZONE_MAP](https://wowdev.wiki/index.php?title=CMSG_ZONE_MAP&action=edit&redlink=1 "CMSG ZONE MAP (page does not exist)")|0x00A||
|[SMSG_ZONE_MAP](https://wowdev.wiki/index.php?title=SMSG_ZONE_MAP&action=edit&redlink=1 "SMSG ZONE MAP (page does not exist)")|0x00B||
|[CMSG_DEBUG_CHANGECELLZONE](https://wowdev.wiki/index.php?title=CMSG_DEBUG_CHANGECELLZONE&action=edit&redlink=1 "CMSG DEBUG CHANGECELLZONE (page does not exist)")|0x00C||
|[CMSG_MOVE_CHARACTER_CHEAT](https://wowdev.wiki/index.php?title=CMSG_MOVE_CHARACTER_CHEAT&action=edit&redlink=1 "CMSG MOVE CHARACTER CHEAT (page does not exist)")|0x00D||
|[SMSG_MOVE_CHARACTER_CHEAT](https://wowdev.wiki/index.php?title=SMSG_MOVE_CHARACTER_CHEAT&action=edit&redlink=1 "SMSG MOVE CHARACTER CHEAT (page does not exist)")|0x00E||
|[CMSG_RECHARGE](https://wowdev.wiki/index.php?title=CMSG_RECHARGE&action=edit&redlink=1 "CMSG RECHARGE (page does not exist)")|0x00F||
|[CMSG_LEARN_SPELL](https://wowdev.wiki/index.php?title=CMSG_LEARN_SPELL&action=edit&redlink=1 "CMSG LEARN SPELL (page does not exist)")|0x010||
|[CMSG_CREATEMONSTER](https://wowdev.wiki/index.php?title=CMSG_CREATEMONSTER&action=edit&redlink=1 "CMSG CREATEMONSTER (page does not exist)")|0x011||
|[CMSG_DESTROYMONSTER](https://wowdev.wiki/index.php?title=CMSG_DESTROYMONSTER&action=edit&redlink=1 "CMSG DESTROYMONSTER (page does not exist)")|0x012||
|[CMSG_CREATEITEM](https://wowdev.wiki/index.php?title=CMSG_CREATEITEM&action=edit&redlink=1 "CMSG CREATEITEM (page does not exist)")|0x013||
|[CMSG_CREATEGAMEOBJECT](https://wowdev.wiki/index.php?title=CMSG_CREATEGAMEOBJECT&action=edit&redlink=1 "CMSG CREATEGAMEOBJECT (page does not exist)")|0x014||
|[SMSG_CHECK_FOR_BOTS](https://wowdev.wiki/index.php?title=SMSG_CHECK_FOR_BOTS&action=edit&redlink=1 "SMSG CHECK FOR BOTS (page does not exist)")|0x015||
|[CMSG_MAKEMONSTERATTACKGUID](https://wowdev.wiki/index.php?title=CMSG_MAKEMONSTERATTACKGUID&action=edit&redlink=1 "CMSG MAKEMONSTERATTACKGUID (page does not exist)")|0x016||
|[CMSG_BOT_DETECTED2](https://wowdev.wiki/index.php?title=CMSG_BOT_DETECTED2&action=edit&redlink=1 "CMSG BOT DETECTED2 (page does not exist)")|0x017||
|[CMSG_FORCEACTION](https://wowdev.wiki/index.php?title=CMSG_FORCEACTION&action=edit&redlink=1 "CMSG FORCEACTION (page does not exist)")|0x018||
|[CMSG_FORCEACTIONONOTHER](https://wowdev.wiki/index.php?title=CMSG_FORCEACTIONONOTHER&action=edit&redlink=1 "CMSG FORCEACTIONONOTHER (page does not exist)")|0x019||
|[CMSG_FORCEACTIONSHOW](https://wowdev.wiki/index.php?title=CMSG_FORCEACTIONSHOW&action=edit&redlink=1 "CMSG FORCEACTIONSHOW (page does not exist)")|0x01A||
|[SMSG_FORCEACTIONSHOW](https://wowdev.wiki/index.php?title=SMSG_FORCEACTIONSHOW&action=edit&redlink=1 "SMSG FORCEACTIONSHOW (page does not exist)")|0x01B||
|[CMSG_PETGODMODE](https://wowdev.wiki/index.php?title=CMSG_PETGODMODE&action=edit&redlink=1 "CMSG PETGODMODE (page does not exist)")|0x01C||
|[SMSG_PETGODMODE](https://wowdev.wiki/index.php?title=SMSG_PETGODMODE&action=edit&redlink=1 "SMSG PETGODMODE (page does not exist)")|0x01D||
|[SMSG_REFER_A_FRIEND_EXPIRED](https://wowdev.wiki/index.php?title=SMSG_REFER_A_FRIEND_EXPIRED&action=edit&redlink=1 "SMSG REFER A FRIEND EXPIRED (page does not exist)")|0x01E||
|[CMSG_WEATHER_SPEED_CHEAT](https://wowdev.wiki/index.php?title=CMSG_WEATHER_SPEED_CHEAT&action=edit&redlink=1 "CMSG WEATHER SPEED CHEAT (page does not exist)")|0x01F||
|[CMSG_UNDRESSPLAYER](https://wowdev.wiki/index.php?title=CMSG_UNDRESSPLAYER&action=edit&redlink=1 "CMSG UNDRESSPLAYER (page does not exist)")|0x020||
|[CMSG_BEASTMASTER](https://wowdev.wiki/index.php?title=CMSG_BEASTMASTER&action=edit&redlink=1 "CMSG BEASTMASTER (page does not exist)")|0x021||
|[CMSG_GODMODE](https://wowdev.wiki/index.php?title=CMSG_GODMODE&action=edit&redlink=1 "CMSG GODMODE (page does not exist)")|0x022||
|[SMSG_GODMODE](https://wowdev.wiki/index.php?title=SMSG_GODMODE&action=edit&redlink=1 "SMSG GODMODE (page does not exist)")|0x023||
|[CMSG_CHEAT_SETMONEY](https://wowdev.wiki/index.php?title=CMSG_CHEAT_SETMONEY&action=edit&redlink=1 "CMSG CHEAT SETMONEY (page does not exist)")|0x024||
|[CMSG_LEVEL_CHEAT](https://wowdev.wiki/index.php?title=CMSG_LEVEL_CHEAT&action=edit&redlink=1 "CMSG LEVEL CHEAT (page does not exist)")|0x025||
|[CMSG_PET_LEVEL_CHEAT](https://wowdev.wiki/index.php?title=CMSG_PET_LEVEL_CHEAT&action=edit&redlink=1 "CMSG PET LEVEL CHEAT (page does not exist)")|0x026||
|[CMSG_SET_WORLDSTATE](https://wowdev.wiki/index.php?title=CMSG_SET_WORLDSTATE&action=edit&redlink=1 "CMSG SET WORLDSTATE (page does not exist)")|0x027||
|[CMSG_COOLDOWN_CHEAT](https://wowdev.wiki/index.php?title=CMSG_COOLDOWN_CHEAT&action=edit&redlink=1 "CMSG COOLDOWN CHEAT (page does not exist)")|0x028||
|[CMSG_USE_SKILL_CHEAT](https://wowdev.wiki/index.php?title=CMSG_USE_SKILL_CHEAT&action=edit&redlink=1 "CMSG USE SKILL CHEAT (page does not exist)")|0x029||
|[CMSG_FLAG_QUEST](https://wowdev.wiki/index.php?title=CMSG_FLAG_QUEST&action=edit&redlink=1 "CMSG FLAG QUEST (page does not exist)")|0x02A||
|[CMSG_FLAG_QUEST_FINISH](https://wowdev.wiki/index.php?title=CMSG_FLAG_QUEST_FINISH&action=edit&redlink=1 "CMSG FLAG QUEST FINISH (page does not exist)")|0x02B||
|[CMSG_CLEAR_QUEST](https://wowdev.wiki/index.php?title=CMSG_CLEAR_QUEST&action=edit&redlink=1 "CMSG CLEAR QUEST (page does not exist)")|0x02C||
|[CMSG_SEND_EVENT](https://wowdev.wiki/index.php?title=CMSG_SEND_EVENT&action=edit&redlink=1 "CMSG SEND EVENT (page does not exist)")|0x02D||
|[CMSG_DEBUG_AISTATE](https://wowdev.wiki/index.php?title=CMSG_DEBUG_AISTATE&action=edit&redlink=1 "CMSG DEBUG AISTATE (page does not exist)")|0x02E||
|[SMSG_DEBUG_AISTATE](https://wowdev.wiki/index.php?title=SMSG_DEBUG_AISTATE&action=edit&redlink=1 "SMSG DEBUG AISTATE (page does not exist)")|0x02F||
|[CMSG_DISABLE_PVP_CHEAT](https://wowdev.wiki/index.php?title=CMSG_DISABLE_PVP_CHEAT&action=edit&redlink=1 "CMSG DISABLE PVP CHEAT (page does not exist)")|0x030||
|[CMSG_ADVANCE_SPAWN_TIME](https://wowdev.wiki/index.php?title=CMSG_ADVANCE_SPAWN_TIME&action=edit&redlink=1 "CMSG ADVANCE SPAWN TIME (page does not exist)")|0x031||
|[SMSG_DESTRUCTIBLE_BUILDING_DAMAGE](https://wowdev.wiki/index.php?title=SMSG_DESTRUCTIBLE_BUILDING_DAMAGE&action=edit&redlink=1 "SMSG DESTRUCTIBLE BUILDING DAMAGE (page does not exist)")|0x032||
|[CMSG_AUTH_SRP6_BEGIN](https://wowdev.wiki/index.php?title=CMSG_AUTH_SRP6_BEGIN&action=edit&redlink=1 "CMSG AUTH SRP6 BEGIN (page does not exist)")|0x033||
|[CMSG_AUTH_SRP6_PROOF](https://wowdev.wiki/index.php?title=CMSG_AUTH_SRP6_PROOF&action=edit&redlink=1 "CMSG AUTH SRP6 PROOF (page does not exist)")|0x034||
|[CMSG_AUTH_SRP6_RECODE](https://wowdev.wiki/index.php?title=CMSG_AUTH_SRP6_RECODE&action=edit&redlink=1 "CMSG AUTH SRP6 RECODE (page does not exist)")|0x035||
|[CMSG_CHAR_CREATE](https://wowdev.wiki/CMSG_CHAR_CREATE "CMSG CHAR CREATE")|0x036||
|[CMSG_CHAR_ENUM](https://wowdev.wiki/CMSG_CHAR_ENUM "CMSG CHAR ENUM")|0x037||
|[CMSG_CHAR_DELETE](https://wowdev.wiki/CMSG_CHAR_DELETE "CMSG CHAR DELETE")|0x038||
|[SMSG_AUTH_SRP6_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_AUTH_SRP6_RESPONSE&action=edit&redlink=1 "SMSG AUTH SRP6 RESPONSE (page does not exist)")|0x039||
|[SMSG_CHAR_CREATE](https://wowdev.wiki/SMSG_CHAR_CREATE "SMSG CHAR CREATE")|0x03A||
|[SMSG_CHAR_ENUM](https://wowdev.wiki/SMSG_CHAR_ENUM "SMSG CHAR ENUM")|0x03B||
|[SMSG_CHAR_DELETE](https://wowdev.wiki/SMSG_CHAR_DELETE "SMSG CHAR DELETE")|0x03C||
|[CMSG_PLAYER_LOGIN](https://wowdev.wiki/CMSG_PLAYER_LOGIN "CMSG PLAYER LOGIN")|0x03D||
|[SMSG_NEW_WORLD](https://wowdev.wiki/index.php?title=SMSG_NEW_WORLD&action=edit&redlink=1 "SMSG NEW WORLD (page does not exist)")|0x03E||
|[SMSG_TRANSFER_PENDING](https://wowdev.wiki/index.php?title=SMSG_TRANSFER_PENDING&action=edit&redlink=1 "SMSG TRANSFER PENDING (page does not exist)")|0x03F||
|[SMSG_TRANSFER_ABORTED](https://wowdev.wiki/index.php?title=SMSG_TRANSFER_ABORTED&action=edit&redlink=1 "SMSG TRANSFER ABORTED (page does not exist)")|0x040||
|[SMSG_CHARACTER_LOGIN_FAILED](https://wowdev.wiki/SMSG_CHARACTER_LOGIN_FAILED "SMSG CHARACTER LOGIN FAILED")|0x041||
|[SMSG_LOGIN_SETTIMESPEED](https://wowdev.wiki/index.php?title=SMSG_LOGIN_SETTIMESPEED&action=edit&redlink=1 "SMSG LOGIN SETTIMESPEED (page does not exist)")|0x042||
|[SMSG_GAMETIME_UPDATE](https://wowdev.wiki/index.php?title=SMSG_GAMETIME_UPDATE&action=edit&redlink=1 "SMSG GAMETIME UPDATE (page does not exist)")|0x043||
|[CMSG_GAMETIME_SET](https://wowdev.wiki/index.php?title=CMSG_GAMETIME_SET&action=edit&redlink=1 "CMSG GAMETIME SET (page does not exist)")|0x044||
|[SMSG_GAMETIME_SET](https://wowdev.wiki/index.php?title=SMSG_GAMETIME_SET&action=edit&redlink=1 "SMSG GAMETIME SET (page does not exist)")|0x045||
|[CMSG_GAMESPEED_SET](https://wowdev.wiki/index.php?title=CMSG_GAMESPEED_SET&action=edit&redlink=1 "CMSG GAMESPEED SET (page does not exist)")|0x046||
|[SMSG_GAMESPEED_SET](https://wowdev.wiki/index.php?title=SMSG_GAMESPEED_SET&action=edit&redlink=1 "SMSG GAMESPEED SET (page does not exist)")|0x047||
|[CMSG_SERVERTIME](https://wowdev.wiki/index.php?title=CMSG_SERVERTIME&action=edit&redlink=1 "CMSG SERVERTIME (page does not exist)")|0x048||
|[SMSG_SERVERTIME](https://wowdev.wiki/index.php?title=SMSG_SERVERTIME&action=edit&redlink=1 "SMSG SERVERTIME (page does not exist)")|0x049||
|[CMSG_PLAYER_LOGOUT](https://wowdev.wiki/index.php?title=CMSG_PLAYER_LOGOUT&action=edit&redlink=1 "CMSG PLAYER LOGOUT (page does not exist)")|0x04A||
|[CMSG_LOGOUT_REQUEST](https://wowdev.wiki/index.php?title=CMSG_LOGOUT_REQUEST&action=edit&redlink=1 "CMSG LOGOUT REQUEST (page does not exist)")|0x04B||
|[SMSG_LOGOUT_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_LOGOUT_RESPONSE&action=edit&redlink=1 "SMSG LOGOUT RESPONSE (page does not exist)")|0x04C||
|[SMSG_LOGOUT_COMPLETE](https://wowdev.wiki/index.php?title=SMSG_LOGOUT_COMPLETE&action=edit&redlink=1 "SMSG LOGOUT COMPLETE (page does not exist)")|0x04D||
|[CMSG_LOGOUT_CANCEL](https://wowdev.wiki/index.php?title=CMSG_LOGOUT_CANCEL&action=edit&redlink=1 "CMSG LOGOUT CANCEL (page does not exist)")|0x04E||
|[SMSG_LOGOUT_CANCEL_ACK](https://wowdev.wiki/index.php?title=SMSG_LOGOUT_CANCEL_ACK&action=edit&redlink=1 "SMSG LOGOUT CANCEL ACK (page does not exist)")|0x04F||
|[CMSG_NAME_QUERY](https://wowdev.wiki/CMSG_NAME_QUERY "CMSG NAME QUERY")|0x050||
|[SMSG_NAME_QUERY_RESPONSE](https://wowdev.wiki/SMSG_NAME_QUERY_RESPONSE "SMSG NAME QUERY RESPONSE")|0x051||
|[CMSG_PET_NAME_QUERY](https://wowdev.wiki/index.php?title=CMSG_PET_NAME_QUERY&action=edit&redlink=1 "CMSG PET NAME QUERY (page does not exist)")|0x052||
|[SMSG_PET_NAME_QUERY_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_PET_NAME_QUERY_RESPONSE&action=edit&redlink=1 "SMSG PET NAME QUERY RESPONSE (page does not exist)")|0x053||
|[CMSG_GUILD_QUERY](https://wowdev.wiki/index.php?title=CMSG_GUILD_QUERY&action=edit&redlink=1 "CMSG GUILD QUERY (page does not exist)")|0x054||
|[SMSG_GUILD_QUERY_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_GUILD_QUERY_RESPONSE&action=edit&redlink=1 "SMSG GUILD QUERY RESPONSE (page does not exist)")|0x055||
|[CMSG_ITEM_QUERY_SINGLE](https://wowdev.wiki/index.php?title=CMSG_ITEM_QUERY_SINGLE&action=edit&redlink=1 "CMSG ITEM QUERY SINGLE (page does not exist)")|0x056||
|[CMSG_ITEM_QUERY_MULTIPLE](https://wowdev.wiki/index.php?title=CMSG_ITEM_QUERY_MULTIPLE&action=edit&redlink=1 "CMSG ITEM QUERY MULTIPLE (page does not exist)")|0x057||
|[SMSG_ITEM_QUERY_SINGLE_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_ITEM_QUERY_SINGLE_RESPONSE&action=edit&redlink=1 "SMSG ITEM QUERY SINGLE RESPONSE (page does not exist)")|0x058||
|[SMSG_ITEM_QUERY_MULTIPLE_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_ITEM_QUERY_MULTIPLE_RESPONSE&action=edit&redlink=1 "SMSG ITEM QUERY MULTIPLE RESPONSE (page does not exist)")|0x059||
|[CMSG_PAGE_TEXT_QUERY](https://wowdev.wiki/index.php?title=CMSG_PAGE_TEXT_QUERY&action=edit&redlink=1 "CMSG PAGE TEXT QUERY (page does not exist)")|0x05A||
|[SMSG_PAGE_TEXT_QUERY_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_PAGE_TEXT_QUERY_RESPONSE&action=edit&redlink=1 "SMSG PAGE TEXT QUERY RESPONSE (page does not exist)")|0x05B||
|[CMSG_QUEST_QUERY](https://wowdev.wiki/index.php?title=CMSG_QUEST_QUERY&action=edit&redlink=1 "CMSG QUEST QUERY (page does not exist)")|0x05C||
|[SMSG_QUEST_QUERY_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_QUEST_QUERY_RESPONSE&action=edit&redlink=1 "SMSG QUEST QUERY RESPONSE (page does not exist)")|0x05D||
|[CMSG_GAMEOBJECT_QUERY](https://wowdev.wiki/index.php?title=CMSG_GAMEOBJECT_QUERY&action=edit&redlink=1 "CMSG GAMEOBJECT QUERY (page does not exist)")|0x05E||
|[SMSG_GAMEOBJECT_QUERY_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_GAMEOBJECT_QUERY_RESPONSE&action=edit&redlink=1 "SMSG GAMEOBJECT QUERY RESPONSE (page does not exist)")|0x05F||
|[CMSG_CREATURE_QUERY](https://wowdev.wiki/index.php?title=CMSG_CREATURE_QUERY&action=edit&redlink=1 "CMSG CREATURE QUERY (page does not exist)")|0x060||
|[SMSG_CREATURE_QUERY_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_CREATURE_QUERY_RESPONSE&action=edit&redlink=1 "SMSG CREATURE QUERY RESPONSE (page does not exist)")|0x061||
|[CMSG_WHO](https://wowdev.wiki/index.php?title=CMSG_WHO&action=edit&redlink=1 "CMSG WHO (page does not exist)")|0x062||
|[SMSG_WHO](https://wowdev.wiki/index.php?title=SMSG_WHO&action=edit&redlink=1 "SMSG WHO (page does not exist)")|0x063||
|[CMSG_WHOIS](https://wowdev.wiki/index.php?title=CMSG_WHOIS&action=edit&redlink=1 "CMSG WHOIS (page does not exist)")|0x064||
|[SMSG_WHOIS](https://wowdev.wiki/index.php?title=SMSG_WHOIS&action=edit&redlink=1 "SMSG WHOIS (page does not exist)")|0x065||
|[CMSG_CONTACT_LIST](https://wowdev.wiki/index.php?title=CMSG_CONTACT_LIST&action=edit&redlink=1 "CMSG CONTACT LIST (page does not exist)")|0x066||
|[SMSG_CONTACT_LIST](https://wowdev.wiki/index.php?title=SMSG_CONTACT_LIST&action=edit&redlink=1 "SMSG CONTACT LIST (page does not exist)")|0x067||
|[SMSG_FRIEND_STATUS](https://wowdev.wiki/index.php?title=SMSG_FRIEND_STATUS&action=edit&redlink=1 "SMSG FRIEND STATUS (page does not exist)")|0x068||
|[CMSG_ADD_FRIEND](https://wowdev.wiki/index.php?title=CMSG_ADD_FRIEND&action=edit&redlink=1 "CMSG ADD FRIEND (page does not exist)")|0x069||
|[CMSG_DEL_FRIEND](https://wowdev.wiki/index.php?title=CMSG_DEL_FRIEND&action=edit&redlink=1 "CMSG DEL FRIEND (page does not exist)")|0x06A||
|[CMSG_SET_CONTACT_NOTES](https://wowdev.wiki/index.php?title=CMSG_SET_CONTACT_NOTES&action=edit&redlink=1 "CMSG SET CONTACT NOTES (page does not exist)")|0x06B||
|[CMSG_ADD_IGNORE](https://wowdev.wiki/index.php?title=CMSG_ADD_IGNORE&action=edit&redlink=1 "CMSG ADD IGNORE (page does not exist)")|0x06C||
|[CMSG_DEL_IGNORE](https://wowdev.wiki/index.php?title=CMSG_DEL_IGNORE&action=edit&redlink=1 "CMSG DEL IGNORE (page does not exist)")|0x06D||
|[CMSG_GROUP_INVITE](https://wowdev.wiki/index.php?title=CMSG_GROUP_INVITE&action=edit&redlink=1 "CMSG GROUP INVITE (page does not exist)")|0x06E||
|[SMSG_GROUP_INVITE](https://wowdev.wiki/index.php?title=SMSG_GROUP_INVITE&action=edit&redlink=1 "SMSG GROUP INVITE (page does not exist)")|0x06F||
|[CMSG_GROUP_CANCEL](https://wowdev.wiki/index.php?title=CMSG_GROUP_CANCEL&action=edit&redlink=1 "CMSG GROUP CANCEL (page does not exist)")|0x070||
|[SMSG_GROUP_CANCEL](https://wowdev.wiki/index.php?title=SMSG_GROUP_CANCEL&action=edit&redlink=1 "SMSG GROUP CANCEL (page does not exist)")|0x071||
|[CMSG_GROUP_ACCEPT](https://wowdev.wiki/index.php?title=CMSG_GROUP_ACCEPT&action=edit&redlink=1 "CMSG GROUP ACCEPT (page does not exist)")|0x072||
|[CMSG_GROUP_DECLINE](https://wowdev.wiki/index.php?title=CMSG_GROUP_DECLINE&action=edit&redlink=1 "CMSG GROUP DECLINE (page does not exist)")|0x073||
|[SMSG_GROUP_DECLINE](https://wowdev.wiki/index.php?title=SMSG_GROUP_DECLINE&action=edit&redlink=1 "SMSG GROUP DECLINE (page does not exist)")|0x074||
|[CMSG_GROUP_UNINVITE](https://wowdev.wiki/index.php?title=CMSG_GROUP_UNINVITE&action=edit&redlink=1 "CMSG GROUP UNINVITE (page does not exist)")|0x075||
|[CMSG_GROUP_UNINVITE_GUID](https://wowdev.wiki/index.php?title=CMSG_GROUP_UNINVITE_GUID&action=edit&redlink=1 "CMSG GROUP UNINVITE GUID (page does not exist)")|0x076||
|[SMSG_GROUP_UNINVITE](https://wowdev.wiki/index.php?title=SMSG_GROUP_UNINVITE&action=edit&redlink=1 "SMSG GROUP UNINVITE (page does not exist)")|0x077||
|[CMSG_GROUP_SET_LEADER](https://wowdev.wiki/index.php?title=CMSG_GROUP_SET_LEADER&action=edit&redlink=1 "CMSG GROUP SET LEADER (page does not exist)")|0x078||
|[SMSG_GROUP_SET_LEADER](https://wowdev.wiki/index.php?title=SMSG_GROUP_SET_LEADER&action=edit&redlink=1 "SMSG GROUP SET LEADER (page does not exist)")|0x079||
|[CMSG_LOOT_METHOD](https://wowdev.wiki/index.php?title=CMSG_LOOT_METHOD&action=edit&redlink=1 "CMSG LOOT METHOD (page does not exist)")|0x07A||
|[CMSG_GROUP_DISBAND](https://wowdev.wiki/index.php?title=CMSG_GROUP_DISBAND&action=edit&redlink=1 "CMSG GROUP DISBAND (page does not exist)")|0x07B||
|[SMSG_GROUP_DESTROYED](https://wowdev.wiki/index.php?title=SMSG_GROUP_DESTROYED&action=edit&redlink=1 "SMSG GROUP DESTROYED (page does not exist)")|0x07C||
|[SMSG_GROUP_LIST](https://wowdev.wiki/index.php?title=SMSG_GROUP_LIST&action=edit&redlink=1 "SMSG GROUP LIST (page does not exist)")|0x07D||
|[SMSG_PARTY_MEMBER_STATS](https://wowdev.wiki/index.php?title=SMSG_PARTY_MEMBER_STATS&action=edit&redlink=1 "SMSG PARTY MEMBER STATS (page does not exist)")|0x07E||
|[SMSG_PARTY_COMMAND_RESULT](https://wowdev.wiki/index.php?title=SMSG_PARTY_COMMAND_RESULT&action=edit&redlink=1 "SMSG PARTY COMMAND RESULT (page does not exist)")|0x07F||
|[UMSG_UPDATE_GROUP_MEMBERS](https://wowdev.wiki/index.php?title=UMSG_UPDATE_GROUP_MEMBERS&action=edit&redlink=1 "UMSG UPDATE GROUP MEMBERS (page does not exist)")|0x080||
|[CMSG_GUILD_CREATE](https://wowdev.wiki/index.php?title=CMSG_GUILD_CREATE&action=edit&redlink=1 "CMSG GUILD CREATE (page does not exist)")|0x081||
|[CMSG_GUILD_INVITE](https://wowdev.wiki/index.php?title=CMSG_GUILD_INVITE&action=edit&redlink=1 "CMSG GUILD INVITE (page does not exist)")|0x082||
|[SMSG_GUILD_INVITE](https://wowdev.wiki/index.php?title=SMSG_GUILD_INVITE&action=edit&redlink=1 "SMSG GUILD INVITE (page does not exist)")|0x083||
|[CMSG_GUILD_ACCEPT](https://wowdev.wiki/index.php?title=CMSG_GUILD_ACCEPT&action=edit&redlink=1 "CMSG GUILD ACCEPT (page does not exist)")|0x084||
|[CMSG_GUILD_DECLINE](https://wowdev.wiki/index.php?title=CMSG_GUILD_DECLINE&action=edit&redlink=1 "CMSG GUILD DECLINE (page does not exist)")|0x085||
|[SMSG_GUILD_DECLINE](https://wowdev.wiki/index.php?title=SMSG_GUILD_DECLINE&action=edit&redlink=1 "SMSG GUILD DECLINE (page does not exist)")|0x086||
|[CMSG_GUILD_INFO](https://wowdev.wiki/index.php?title=CMSG_GUILD_INFO&action=edit&redlink=1 "CMSG GUILD INFO (page does not exist)")|0x087||
|[SMSG_GUILD_INFO](https://wowdev.wiki/index.php?title=SMSG_GUILD_INFO&action=edit&redlink=1 "SMSG GUILD INFO (page does not exist)")|0x088||
|[CMSG_GUILD_ROSTER](https://wowdev.wiki/index.php?title=CMSG_GUILD_ROSTER&action=edit&redlink=1 "CMSG GUILD ROSTER (page does not exist)")|0x089||
|[SMSG_GUILD_ROSTER](https://wowdev.wiki/index.php?title=SMSG_GUILD_ROSTER&action=edit&redlink=1 "SMSG GUILD ROSTER (page does not exist)")|0x08A||
|[CMSG_GUILD_PROMOTE](https://wowdev.wiki/index.php?title=CMSG_GUILD_PROMOTE&action=edit&redlink=1 "CMSG GUILD PROMOTE (page does not exist)")|0x08B||
|[CMSG_GUILD_DEMOTE](https://wowdev.wiki/index.php?title=CMSG_GUILD_DEMOTE&action=edit&redlink=1 "CMSG GUILD DEMOTE (page does not exist)")|0x08C||
|[CMSG_GUILD_LEAVE](https://wowdev.wiki/index.php?title=CMSG_GUILD_LEAVE&action=edit&redlink=1 "CMSG GUILD LEAVE (page does not exist)")|0x08D||
|[CMSG_GUILD_REMOVE](https://wowdev.wiki/index.php?title=CMSG_GUILD_REMOVE&action=edit&redlink=1 "CMSG GUILD REMOVE (page does not exist)")|0x08E||
|[CMSG_GUILD_DISBAND](https://wowdev.wiki/index.php?title=CMSG_GUILD_DISBAND&action=edit&redlink=1 "CMSG GUILD DISBAND (page does not exist)")|0x08F||
|[CMSG_GUILD_LEADER](https://wowdev.wiki/index.php?title=CMSG_GUILD_LEADER&action=edit&redlink=1 "CMSG GUILD LEADER (page does not exist)")|0x090||
|[CMSG_GUILD_MOTD](https://wowdev.wiki/index.php?title=CMSG_GUILD_MOTD&action=edit&redlink=1 "CMSG GUILD MOTD (page does not exist)")|0x091||
|[SMSG_GUILD_EVENT](https://wowdev.wiki/index.php?title=SMSG_GUILD_EVENT&action=edit&redlink=1 "SMSG GUILD EVENT (page does not exist)")|0x092||
|[SMSG_GUILD_COMMAND_RESULT](https://wowdev.wiki/index.php?title=SMSG_GUILD_COMMAND_RESULT&action=edit&redlink=1 "SMSG GUILD COMMAND RESULT (page does not exist)")|0x093||
|[UMSG_UPDATE_GUILD](https://wowdev.wiki/index.php?title=UMSG_UPDATE_GUILD&action=edit&redlink=1 "UMSG UPDATE GUILD (page does not exist)")|0x094||
|[CMSG_MESSAGECHAT](https://wowdev.wiki/index.php?title=CMSG_MESSAGECHAT&action=edit&redlink=1 "CMSG MESSAGECHAT (page does not exist)")|0x095||
|[SMSG_MESSAGECHAT](https://wowdev.wiki/index.php?title=SMSG_MESSAGECHAT&action=edit&redlink=1 "SMSG MESSAGECHAT (page does not exist)")|0x096||
|[CMSG_JOIN_CHANNEL](https://wowdev.wiki/index.php?title=CMSG_JOIN_CHANNEL&action=edit&redlink=1 "CMSG JOIN CHANNEL (page does not exist)")|0x097||
|[CMSG_LEAVE_CHANNEL](https://wowdev.wiki/index.php?title=CMSG_LEAVE_CHANNEL&action=edit&redlink=1 "CMSG LEAVE CHANNEL (page does not exist)")|0x098||
|[SMSG_CHANNEL_NOTIFY](https://wowdev.wiki/index.php?title=SMSG_CHANNEL_NOTIFY&action=edit&redlink=1 "SMSG CHANNEL NOTIFY (page does not exist)")|0x099||
|[CMSG_CHANNEL_LIST](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_LIST&action=edit&redlink=1 "CMSG CHANNEL LIST (page does not exist)")|0x09A||
|[SMSG_CHANNEL_LIST](https://wowdev.wiki/index.php?title=SMSG_CHANNEL_LIST&action=edit&redlink=1 "SMSG CHANNEL LIST (page does not exist)")|0x09B||
|[CMSG_CHANNEL_PASSWORD](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_PASSWORD&action=edit&redlink=1 "CMSG CHANNEL PASSWORD (page does not exist)")|0x09C||
|[CMSG_CHANNEL_SET_OWNER](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_SET_OWNER&action=edit&redlink=1 "CMSG CHANNEL SET OWNER (page does not exist)")|0x09D||
|[CMSG_CHANNEL_OWNER](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_OWNER&action=edit&redlink=1 "CMSG CHANNEL OWNER (page does not exist)")|0x09E||
|[CMSG_CHANNEL_MODERATOR](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_MODERATOR&action=edit&redlink=1 "CMSG CHANNEL MODERATOR (page does not exist)")|0x09F||
|[CMSG_CHANNEL_UNMODERATOR](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_UNMODERATOR&action=edit&redlink=1 "CMSG CHANNEL UNMODERATOR (page does not exist)")|0x0A0||
|[CMSG_CHANNEL_MUTE](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_MUTE&action=edit&redlink=1 "CMSG CHANNEL MUTE (page does not exist)")|0x0A1||
|[CMSG_CHANNEL_UNMUTE](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_UNMUTE&action=edit&redlink=1 "CMSG CHANNEL UNMUTE (page does not exist)")|0x0A2||
|[CMSG_CHANNEL_INVITE](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_INVITE&action=edit&redlink=1 "CMSG CHANNEL INVITE (page does not exist)")|0x0A3||
|[CMSG_CHANNEL_KICK](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_KICK&action=edit&redlink=1 "CMSG CHANNEL KICK (page does not exist)")|0x0A4||
|[CMSG_CHANNEL_BAN](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_BAN&action=edit&redlink=1 "CMSG CHANNEL BAN (page does not exist)")|0x0A5||
|[CMSG_CHANNEL_UNBAN](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_UNBAN&action=edit&redlink=1 "CMSG CHANNEL UNBAN (page does not exist)")|0x0A6||
|[CMSG_CHANNEL_ANNOUNCEMENTS](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_ANNOUNCEMENTS&action=edit&redlink=1 "CMSG CHANNEL ANNOUNCEMENTS (page does not exist)")|0x0A7||
|[CMSG_CHANNEL_MODERATE](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_MODERATE&action=edit&redlink=1 "CMSG CHANNEL MODERATE (page does not exist)")|0x0A8||
|[SMSG_UPDATE_OBJECT](https://wowdev.wiki/SMSG_UPDATE_OBJECT "SMSG UPDATE OBJECT")|0x0A9||
|[SMSG_DESTROY_OBJECT](https://wowdev.wiki/index.php?title=SMSG_DESTROY_OBJECT&action=edit&redlink=1 "SMSG DESTROY OBJECT (page does not exist)")|0x0AA||
|[CMSG_USE_ITEM](https://wowdev.wiki/index.php?title=CMSG_USE_ITEM&action=edit&redlink=1 "CMSG USE ITEM (page does not exist)")|0x0AB||
|[CMSG_OPEN_ITEM](https://wowdev.wiki/index.php?title=CMSG_OPEN_ITEM&action=edit&redlink=1 "CMSG OPEN ITEM (page does not exist)")|0x0AC||
|[CMSG_READ_ITEM](https://wowdev.wiki/index.php?title=CMSG_READ_ITEM&action=edit&redlink=1 "CMSG READ ITEM (page does not exist)")|0x0AD||
|[SMSG_READ_ITEM_OK](https://wowdev.wiki/index.php?title=SMSG_READ_ITEM_OK&action=edit&redlink=1 "SMSG READ ITEM OK (page does not exist)")|0x0AE||
|[SMSG_READ_ITEM_FAILED](https://wowdev.wiki/index.php?title=SMSG_READ_ITEM_FAILED&action=edit&redlink=1 "SMSG READ ITEM FAILED (page does not exist)")|0x0AF||
|[SMSG_ITEM_COOLDOWN](https://wowdev.wiki/index.php?title=SMSG_ITEM_COOLDOWN&action=edit&redlink=1 "SMSG ITEM COOLDOWN (page does not exist)")|0x0B0||
|[CMSG_GAMEOBJ_USE](https://wowdev.wiki/index.php?title=CMSG_GAMEOBJ_USE&action=edit&redlink=1 "CMSG GAMEOBJ USE (page does not exist)")|0x0B1||
|[CMSG_DESTROY_ITEMS](https://wowdev.wiki/index.php?title=CMSG_DESTROY_ITEMS&action=edit&redlink=1 "CMSG DESTROY ITEMS (page does not exist)")|0x0B2||
|[SMSG_GAMEOBJECT_CUSTOM_ANIM](https://wowdev.wiki/index.php?title=SMSG_GAMEOBJECT_CUSTOM_ANIM&action=edit&redlink=1 "SMSG GAMEOBJECT CUSTOM ANIM (page does not exist)")|0x0B3||
|[CMSG_AREATRIGGER](https://wowdev.wiki/index.php?title=CMSG_AREATRIGGER&action=edit&redlink=1 "CMSG AREATRIGGER (page does not exist)")|0x0B4||
|[MSG_MOVE_START_FORWARD](https://wowdev.wiki/index.php?title=MSG_MOVE_START_FORWARD&action=edit&redlink=1 "MSG MOVE START FORWARD (page does not exist)")|0x0B5||
|[MSG_MOVE_START_BACKWARD](https://wowdev.wiki/index.php?title=MSG_MOVE_START_BACKWARD&action=edit&redlink=1 "MSG MOVE START BACKWARD (page does not exist)")|0x0B6||
|[MSG_MOVE_STOP](https://wowdev.wiki/index.php?title=MSG_MOVE_STOP&action=edit&redlink=1 "MSG MOVE STOP (page does not exist)")|0x0B7||
|[MSG_MOVE_START_STRAFE_LEFT](https://wowdev.wiki/index.php?title=MSG_MOVE_START_STRAFE_LEFT&action=edit&redlink=1 "MSG MOVE START STRAFE LEFT (page does not exist)")|0x0B8||
|[MSG_MOVE_START_STRAFE_RIGHT](https://wowdev.wiki/index.php?title=MSG_MOVE_START_STRAFE_RIGHT&action=edit&redlink=1 "MSG MOVE START STRAFE RIGHT (page does not exist)")|0x0B9||
|[MSG_MOVE_STOP_STRAFE](https://wowdev.wiki/index.php?title=MSG_MOVE_STOP_STRAFE&action=edit&redlink=1 "MSG MOVE STOP STRAFE (page does not exist)")|0x0BA||
|[MSG_MOVE_JUMP](https://wowdev.wiki/index.php?title=MSG_MOVE_JUMP&action=edit&redlink=1 "MSG MOVE JUMP (page does not exist)")|0x0BB||
|[MSG_MOVE_START_TURN_LEFT](https://wowdev.wiki/index.php?title=MSG_MOVE_START_TURN_LEFT&action=edit&redlink=1 "MSG MOVE START TURN LEFT (page does not exist)")|0x0BC||
|[MSG_MOVE_START_TURN_RIGHT](https://wowdev.wiki/index.php?title=MSG_MOVE_START_TURN_RIGHT&action=edit&redlink=1 "MSG MOVE START TURN RIGHT (page does not exist)")|0x0BD||
|[MSG_MOVE_STOP_TURN](https://wowdev.wiki/index.php?title=MSG_MOVE_STOP_TURN&action=edit&redlink=1 "MSG MOVE STOP TURN (page does not exist)")|0x0BE||
|[MSG_MOVE_START_PITCH_UP](https://wowdev.wiki/index.php?title=MSG_MOVE_START_PITCH_UP&action=edit&redlink=1 "MSG MOVE START PITCH UP (page does not exist)")|0x0BF||
|[MSG_MOVE_START_PITCH_DOWN](https://wowdev.wiki/index.php?title=MSG_MOVE_START_PITCH_DOWN&action=edit&redlink=1 "MSG MOVE START PITCH DOWN (page does not exist)")|0x0C0||
|[MSG_MOVE_STOP_PITCH](https://wowdev.wiki/index.php?title=MSG_MOVE_STOP_PITCH&action=edit&redlink=1 "MSG MOVE STOP PITCH (page does not exist)")|0x0C1||
|[MSG_MOVE_SET_RUN_MODE](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_RUN_MODE&action=edit&redlink=1 "MSG MOVE SET RUN MODE (page does not exist)")|0x0C2||
|[MSG_MOVE_SET_WALK_MODE](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_WALK_MODE&action=edit&redlink=1 "MSG MOVE SET WALK MODE (page does not exist)")|0x0C3||
|[MSG_MOVE_TOGGLE_LOGGING](https://wowdev.wiki/index.php?title=MSG_MOVE_TOGGLE_LOGGING&action=edit&redlink=1 "MSG MOVE TOGGLE LOGGING (page does not exist)")|0x0C4||
|[MSG_MOVE_TELEPORT](https://wowdev.wiki/index.php?title=MSG_MOVE_TELEPORT&action=edit&redlink=1 "MSG MOVE TELEPORT (page does not exist)")|0x0C5||
|[MSG_MOVE_TELEPORT_CHEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_TELEPORT_CHEAT&action=edit&redlink=1 "MSG MOVE TELEPORT CHEAT (page does not exist)")|0x0C6||
|[MSG_MOVE_TELEPORT_ACK](https://wowdev.wiki/index.php?title=MSG_MOVE_TELEPORT_ACK&action=edit&redlink=1 "MSG MOVE TELEPORT ACK (page does not exist)")|0x0C7||
|[MSG_MOVE_TOGGLE_FALL_LOGGING](https://wowdev.wiki/index.php?title=MSG_MOVE_TOGGLE_FALL_LOGGING&action=edit&redlink=1 "MSG MOVE TOGGLE FALL LOGGING (page does not exist)")|0x0C8||
|[MSG_MOVE_FALL_LAND](https://wowdev.wiki/index.php?title=MSG_MOVE_FALL_LAND&action=edit&redlink=1 "MSG MOVE FALL LAND (page does not exist)")|0x0C9||
|[MSG_MOVE_START_SWIM](https://wowdev.wiki/index.php?title=MSG_MOVE_START_SWIM&action=edit&redlink=1 "MSG MOVE START SWIM (page does not exist)")|0x0CA||
|[MSG_MOVE_STOP_SWIM](https://wowdev.wiki/index.php?title=MSG_MOVE_STOP_SWIM&action=edit&redlink=1 "MSG MOVE STOP SWIM (page does not exist)")|0x0CB||
|[MSG_MOVE_SET_RUN_SPEED_CHEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_RUN_SPEED_CHEAT&action=edit&redlink=1 "MSG MOVE SET RUN SPEED CHEAT (page does not exist)")|0x0CC||
|[MSG_MOVE_SET_RUN_SPEED](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_RUN_SPEED&action=edit&redlink=1 "MSG MOVE SET RUN SPEED (page does not exist)")|0x0CD||
|[MSG_MOVE_SET_RUN_BACK_SPEED_CHEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_RUN_BACK_SPEED_CHEAT&action=edit&redlink=1 "MSG MOVE SET RUN BACK SPEED CHEAT (page does not exist)")|0x0CE||
|[MSG_MOVE_SET_RUN_BACK_SPEED](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_RUN_BACK_SPEED&action=edit&redlink=1 "MSG MOVE SET RUN BACK SPEED (page does not exist)")|0x0CF||
|[MSG_MOVE_SET_WALK_SPEED_CHEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_WALK_SPEED_CHEAT&action=edit&redlink=1 "MSG MOVE SET WALK SPEED CHEAT (page does not exist)")|0x0D0||
|[MSG_MOVE_SET_WALK_SPEED](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_WALK_SPEED&action=edit&redlink=1 "MSG MOVE SET WALK SPEED (page does not exist)")|0x0D1||
|[MSG_MOVE_SET_SWIM_SPEED_CHEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_SWIM_SPEED_CHEAT&action=edit&redlink=1 "MSG MOVE SET SWIM SPEED CHEAT (page does not exist)")|0x0D2||
|[MSG_MOVE_SET_SWIM_SPEED](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_SWIM_SPEED&action=edit&redlink=1 "MSG MOVE SET SWIM SPEED (page does not exist)")|0x0D3||
|[MSG_MOVE_SET_SWIM_BACK_SPEED_CHEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_SWIM_BACK_SPEED_CHEAT&action=edit&redlink=1 "MSG MOVE SET SWIM BACK SPEED CHEAT (page does not exist)")|0x0D4||
|[MSG_MOVE_SET_SWIM_BACK_SPEED](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_SWIM_BACK_SPEED&action=edit&redlink=1 "MSG MOVE SET SWIM BACK SPEED (page does not exist)")|0x0D5||
|[MSG_MOVE_SET_ALL_SPEED_CHEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_ALL_SPEED_CHEAT&action=edit&redlink=1 "MSG MOVE SET ALL SPEED CHEAT (page does not exist)")|0x0D6||
|[MSG_MOVE_SET_TURN_RATE_CHEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_TURN_RATE_CHEAT&action=edit&redlink=1 "MSG MOVE SET TURN RATE CHEAT (page does not exist)")|0x0D7||
|[MSG_MOVE_SET_TURN_RATE](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_TURN_RATE&action=edit&redlink=1 "MSG MOVE SET TURN RATE (page does not exist)")|0x0D8||
|[MSG_MOVE_TOGGLE_COLLISION_CHEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_TOGGLE_COLLISION_CHEAT&action=edit&redlink=1 "MSG MOVE TOGGLE COLLISION CHEAT (page does not exist)")|0x0D9||
|[MSG_MOVE_SET_FACING](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_FACING&action=edit&redlink=1 "MSG MOVE SET FACING (page does not exist)")|0x0DA||
|[MSG_MOVE_SET_PITCH](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_PITCH&action=edit&redlink=1 "MSG MOVE SET PITCH (page does not exist)")|0x0DB||
|[MSG_MOVE_WORLDPORT_ACK](https://wowdev.wiki/index.php?title=MSG_MOVE_WORLDPORT_ACK&action=edit&redlink=1 "MSG MOVE WORLDPORT ACK (page does not exist)")|0x0DC||
|[SMSG_MONSTER_MOVE](https://wowdev.wiki/index.php?title=SMSG_MONSTER_MOVE&action=edit&redlink=1 "SMSG MONSTER MOVE (page does not exist)")|0x0DD||
|[SMSG_MOVE_WATER_WALK](https://wowdev.wiki/index.php?title=SMSG_MOVE_WATER_WALK&action=edit&redlink=1 "SMSG MOVE WATER WALK (page does not exist)")|0x0DE||
|[SMSG_MOVE_LAND_WALK](https://wowdev.wiki/index.php?title=SMSG_MOVE_LAND_WALK&action=edit&redlink=1 "SMSG MOVE LAND WALK (page does not exist)")|0x0DF||
|[MSG_MOVE_SET_RAW_POSITION_ACK](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_RAW_POSITION_ACK&action=edit&redlink=1 "MSG MOVE SET RAW POSITION ACK (page does not exist)")|0x0E0||
|[CMSG_MOVE_SET_RAW_POSITION](https://wowdev.wiki/index.php?title=CMSG_MOVE_SET_RAW_POSITION&action=edit&redlink=1 "CMSG MOVE SET RAW POSITION (page does not exist)")|0x0E1||
|[SMSG_FORCE_RUN_SPEED_CHANGE](https://wowdev.wiki/index.php?title=SMSG_FORCE_RUN_SPEED_CHANGE&action=edit&redlink=1 "SMSG FORCE RUN SPEED CHANGE (page does not exist)")|0x0E2||
|[CMSG_FORCE_RUN_SPEED_CHANGE_ACK](https://wowdev.wiki/index.php?title=CMSG_FORCE_RUN_SPEED_CHANGE_ACK&action=edit&redlink=1 "CMSG FORCE RUN SPEED CHANGE ACK (page does not exist)")|0x0E3||
|[SMSG_FORCE_RUN_BACK_SPEED_CHANGE](https://wowdev.wiki/index.php?title=SMSG_FORCE_RUN_BACK_SPEED_CHANGE&action=edit&redlink=1 "SMSG FORCE RUN BACK SPEED CHANGE (page does not exist)")|0x0E4||
|[CMSG_FORCE_RUN_BACK_SPEED_CHANGE_ACK](https://wowdev.wiki/index.php?title=CMSG_FORCE_RUN_BACK_SPEED_CHANGE_ACK&action=edit&redlink=1 "CMSG FORCE RUN BACK SPEED CHANGE ACK (page does not exist)")|0x0E5||
|[SMSG_FORCE_SWIM_SPEED_CHANGE](https://wowdev.wiki/index.php?title=SMSG_FORCE_SWIM_SPEED_CHANGE&action=edit&redlink=1 "SMSG FORCE SWIM SPEED CHANGE (page does not exist)")|0x0E6||
|[CMSG_FORCE_SWIM_SPEED_CHANGE_ACK](https://wowdev.wiki/index.php?title=CMSG_FORCE_SWIM_SPEED_CHANGE_ACK&action=edit&redlink=1 "CMSG FORCE SWIM SPEED CHANGE ACK (page does not exist)")|0x0E7||
|[SMSG_FORCE_MOVE_ROOT](https://wowdev.wiki/index.php?title=SMSG_FORCE_MOVE_ROOT&action=edit&redlink=1 "SMSG FORCE MOVE ROOT (page does not exist)")|0x0E8||
|[CMSG_FORCE_MOVE_ROOT_ACK](https://wowdev.wiki/index.php?title=CMSG_FORCE_MOVE_ROOT_ACK&action=edit&redlink=1 "CMSG FORCE MOVE ROOT ACK (page does not exist)")|0x0E9||
|[SMSG_FORCE_MOVE_UNROOT](https://wowdev.wiki/index.php?title=SMSG_FORCE_MOVE_UNROOT&action=edit&redlink=1 "SMSG FORCE MOVE UNROOT (page does not exist)")|0x0EA||
|[CMSG_FORCE_MOVE_UNROOT_ACK](https://wowdev.wiki/index.php?title=CMSG_FORCE_MOVE_UNROOT_ACK&action=edit&redlink=1 "CMSG FORCE MOVE UNROOT ACK (page does not exist)")|0x0EB||
|[MSG_MOVE_ROOT](https://wowdev.wiki/index.php?title=MSG_MOVE_ROOT&action=edit&redlink=1 "MSG MOVE ROOT (page does not exist)")|0x0EC||
|[MSG_MOVE_UNROOT](https://wowdev.wiki/index.php?title=MSG_MOVE_UNROOT&action=edit&redlink=1 "MSG MOVE UNROOT (page does not exist)")|0x0ED||
|[MSG_MOVE_HEARTBEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_HEARTBEAT&action=edit&redlink=1 "MSG MOVE HEARTBEAT (page does not exist)")|0x0EE||
|[SMSG_MOVE_KNOCK_BACK](https://wowdev.wiki/index.php?title=SMSG_MOVE_KNOCK_BACK&action=edit&redlink=1 "SMSG MOVE KNOCK BACK (page does not exist)")|0x0EF||
|[CMSG_MOVE_KNOCK_BACK_ACK](https://wowdev.wiki/index.php?title=CMSG_MOVE_KNOCK_BACK_ACK&action=edit&redlink=1 "CMSG MOVE KNOCK BACK ACK (page does not exist)")|0x0F0||
|[MSG_MOVE_KNOCK_BACK](https://wowdev.wiki/index.php?title=MSG_MOVE_KNOCK_BACK&action=edit&redlink=1 "MSG MOVE KNOCK BACK (page does not exist)")|0x0F1||
|[SMSG_MOVE_FEATHER_FALL](https://wowdev.wiki/index.php?title=SMSG_MOVE_FEATHER_FALL&action=edit&redlink=1 "SMSG MOVE FEATHER FALL (page does not exist)")|0x0F2||
|[SMSG_MOVE_NORMAL_FALL](https://wowdev.wiki/index.php?title=SMSG_MOVE_NORMAL_FALL&action=edit&redlink=1 "SMSG MOVE NORMAL FALL (page does not exist)")|0x0F3||
|[SMSG_MOVE_SET_HOVER](https://wowdev.wiki/index.php?title=SMSG_MOVE_SET_HOVER&action=edit&redlink=1 "SMSG MOVE SET HOVER (page does not exist)")|0x0F4||
|[SMSG_MOVE_UNSET_HOVER](https://wowdev.wiki/index.php?title=SMSG_MOVE_UNSET_HOVER&action=edit&redlink=1 "SMSG MOVE UNSET HOVER (page does not exist)")|0x0F5||
|[CMSG_MOVE_HOVER_ACK](https://wowdev.wiki/index.php?title=CMSG_MOVE_HOVER_ACK&action=edit&redlink=1 "CMSG MOVE HOVER ACK (page does not exist)")|0x0F6||
|[MSG_MOVE_HOVER](https://wowdev.wiki/index.php?title=MSG_MOVE_HOVER&action=edit&redlink=1 "MSG MOVE HOVER (page does not exist)")|0x0F7||
|[CMSG_TRIGGER_CINEMATIC_CHEAT](https://wowdev.wiki/index.php?title=CMSG_TRIGGER_CINEMATIC_CHEAT&action=edit&redlink=1 "CMSG TRIGGER CINEMATIC CHEAT (page does not exist)")|0x0F8||
|[CMSG_OPENING_CINEMATIC](https://wowdev.wiki/index.php?title=CMSG_OPENING_CINEMATIC&action=edit&redlink=1 "CMSG OPENING CINEMATIC (page does not exist)")|0x0F9||
|[SMSG_TRIGGER_CINEMATIC](https://wowdev.wiki/index.php?title=SMSG_TRIGGER_CINEMATIC&action=edit&redlink=1 "SMSG TRIGGER CINEMATIC (page does not exist)")|0x0FA||
|[CMSG_NEXT_CINEMATIC_CAMERA](https://wowdev.wiki/index.php?title=CMSG_NEXT_CINEMATIC_CAMERA&action=edit&redlink=1 "CMSG NEXT CINEMATIC CAMERA (page does not exist)")|0x0FB||
|[CMSG_COMPLETE_CINEMATIC](https://wowdev.wiki/index.php?title=CMSG_COMPLETE_CINEMATIC&action=edit&redlink=1 "CMSG COMPLETE CINEMATIC (page does not exist)")|0x0FC||
|[SMSG_TUTORIAL_FLAGS](https://wowdev.wiki/SMSG_TUTORIAL_FLAGS "SMSG TUTORIAL FLAGS")|0x0FD||
|[CMSG_TUTORIAL_FLAG](https://wowdev.wiki/index.php?title=CMSG_TUTORIAL_FLAG&action=edit&redlink=1 "CMSG TUTORIAL FLAG (page does not exist)")|0x0FE||
|[CMSG_TUTORIAL_CLEAR](https://wowdev.wiki/index.php?title=CMSG_TUTORIAL_CLEAR&action=edit&redlink=1 "CMSG TUTORIAL CLEAR (page does not exist)")|0x0FF||
|[CMSG_TUTORIAL_RESET](https://wowdev.wiki/index.php?title=CMSG_TUTORIAL_RESET&action=edit&redlink=1 "CMSG TUTORIAL RESET (page does not exist)")|0x100||
|[CMSG_STANDSTATECHANGE](https://wowdev.wiki/index.php?title=CMSG_STANDSTATECHANGE&action=edit&redlink=1 "CMSG STANDSTATECHANGE (page does not exist)")|0x101||
|[CMSG_EMOTE](https://wowdev.wiki/index.php?title=CMSG_EMOTE&action=edit&redlink=1 "CMSG EMOTE (page does not exist)")|0x102||
|[SMSG_EMOTE](https://wowdev.wiki/index.php?title=SMSG_EMOTE&action=edit&redlink=1 "SMSG EMOTE (page does not exist)")|0x103||
|[CMSG_TEXT_EMOTE](https://wowdev.wiki/index.php?title=CMSG_TEXT_EMOTE&action=edit&redlink=1 "CMSG TEXT EMOTE (page does not exist)")|0x104||
|[SMSG_TEXT_EMOTE](https://wowdev.wiki/index.php?title=SMSG_TEXT_EMOTE&action=edit&redlink=1 "SMSG TEXT EMOTE (page does not exist)")|0x105||
|[CMSG_AUTOEQUIP_GROUND_ITEM](https://wowdev.wiki/index.php?title=CMSG_AUTOEQUIP_GROUND_ITEM&action=edit&redlink=1 "CMSG AUTOEQUIP GROUND ITEM (page does not exist)")|0x106||
|[CMSG_AUTOSTORE_GROUND_ITEM](https://wowdev.wiki/index.php?title=CMSG_AUTOSTORE_GROUND_ITEM&action=edit&redlink=1 "CMSG AUTOSTORE GROUND ITEM (page does not exist)")|0x107||
|[CMSG_AUTOSTORE_LOOT_ITEM](https://wowdev.wiki/index.php?title=CMSG_AUTOSTORE_LOOT_ITEM&action=edit&redlink=1 "CMSG AUTOSTORE LOOT ITEM (page does not exist)")|0x108||
|[CMSG_STORE_LOOT_IN_SLOT](https://wowdev.wiki/index.php?title=CMSG_STORE_LOOT_IN_SLOT&action=edit&redlink=1 "CMSG STORE LOOT IN SLOT (page does not exist)")|0x109||
|[CMSG_AUTOEQUIP_ITEM](https://wowdev.wiki/index.php?title=CMSG_AUTOEQUIP_ITEM&action=edit&redlink=1 "CMSG AUTOEQUIP ITEM (page does not exist)")|0x10A||
|[CMSG_AUTOSTORE_BAG_ITEM](https://wowdev.wiki/index.php?title=CMSG_AUTOSTORE_BAG_ITEM&action=edit&redlink=1 "CMSG AUTOSTORE BAG ITEM (page does not exist)")|0x10B||
|[CMSG_SWAP_ITEM](https://wowdev.wiki/index.php?title=CMSG_SWAP_ITEM&action=edit&redlink=1 "CMSG SWAP ITEM (page does not exist)")|0x10C||
|[CMSG_SWAP_INV_ITEM](https://wowdev.wiki/index.php?title=CMSG_SWAP_INV_ITEM&action=edit&redlink=1 "CMSG SWAP INV ITEM (page does not exist)")|0x10D||
|[CMSG_SPLIT_ITEM](https://wowdev.wiki/index.php?title=CMSG_SPLIT_ITEM&action=edit&redlink=1 "CMSG SPLIT ITEM (page does not exist)")|0x10E||
|[CMSG_AUTOEQUIP_ITEM_SLOT](https://wowdev.wiki/index.php?title=CMSG_AUTOEQUIP_ITEM_SLOT&action=edit&redlink=1 "CMSG AUTOEQUIP ITEM SLOT (page does not exist)")|0x10F||
|[OBSOLETE_DROP_ITEM](https://wowdev.wiki/index.php?title=OBSOLETE_DROP_ITEM&action=edit&redlink=1 "OBSOLETE DROP ITEM (page does not exist)")|0x110||
|[CMSG_DESTROYITEM](https://wowdev.wiki/index.php?title=CMSG_DESTROYITEM&action=edit&redlink=1 "CMSG DESTROYITEM (page does not exist)")|0x111||
|[SMSG_INVENTORY_CHANGE_FAILURE](https://wowdev.wiki/index.php?title=SMSG_INVENTORY_CHANGE_FAILURE&action=edit&redlink=1 "SMSG INVENTORY CHANGE FAILURE (page does not exist)")|0x112||
|[SMSG_OPEN_CONTAINER](https://wowdev.wiki/index.php?title=SMSG_OPEN_CONTAINER&action=edit&redlink=1 "SMSG OPEN CONTAINER (page does not exist)")|0x113||
|[CMSG_INSPECT](https://wowdev.wiki/index.php?title=CMSG_INSPECT&action=edit&redlink=1 "CMSG INSPECT (page does not exist)")|0x114||
|[SMSG_INSPECT](https://wowdev.wiki/index.php?title=SMSG_INSPECT&action=edit&redlink=1 "SMSG INSPECT (page does not exist)")|0x115||
|[CMSG_INITIATE_TRADE](https://wowdev.wiki/index.php?title=CMSG_INITIATE_TRADE&action=edit&redlink=1 "CMSG INITIATE TRADE (page does not exist)")|0x116||
|[CMSG_BEGIN_TRADE](https://wowdev.wiki/index.php?title=CMSG_BEGIN_TRADE&action=edit&redlink=1 "CMSG BEGIN TRADE (page does not exist)")|0x117||
|[CMSG_BUSY_TRADE](https://wowdev.wiki/index.php?title=CMSG_BUSY_TRADE&action=edit&redlink=1 "CMSG BUSY TRADE (page does not exist)")|0x118||
|[CMSG_IGNORE_TRADE](https://wowdev.wiki/index.php?title=CMSG_IGNORE_TRADE&action=edit&redlink=1 "CMSG IGNORE TRADE (page does not exist)")|0x119||
|[CMSG_ACCEPT_TRADE](https://wowdev.wiki/index.php?title=CMSG_ACCEPT_TRADE&action=edit&redlink=1 "CMSG ACCEPT TRADE (page does not exist)")|0x11A||
|[CMSG_UNACCEPT_TRADE](https://wowdev.wiki/index.php?title=CMSG_UNACCEPT_TRADE&action=edit&redlink=1 "CMSG UNACCEPT TRADE (page does not exist)")|0x11B||
|[CMSG_CANCEL_TRADE](https://wowdev.wiki/index.php?title=CMSG_CANCEL_TRADE&action=edit&redlink=1 "CMSG CANCEL TRADE (page does not exist)")|0x11C||
|[CMSG_SET_TRADE_ITEM](https://wowdev.wiki/index.php?title=CMSG_SET_TRADE_ITEM&action=edit&redlink=1 "CMSG SET TRADE ITEM (page does not exist)")|0x11D||
|[CMSG_CLEAR_TRADE_ITEM](https://wowdev.wiki/index.php?title=CMSG_CLEAR_TRADE_ITEM&action=edit&redlink=1 "CMSG CLEAR TRADE ITEM (page does not exist)")|0x11E||
|[CMSG_SET_TRADE_GOLD](https://wowdev.wiki/index.php?title=CMSG_SET_TRADE_GOLD&action=edit&redlink=1 "CMSG SET TRADE GOLD (page does not exist)")|0x11F||
|[SMSG_TRADE_STATUS](https://wowdev.wiki/index.php?title=SMSG_TRADE_STATUS&action=edit&redlink=1 "SMSG TRADE STATUS (page does not exist)")|0x120||
|[SMSG_TRADE_STATUS_EXTENDED](https://wowdev.wiki/index.php?title=SMSG_TRADE_STATUS_EXTENDED&action=edit&redlink=1 "SMSG TRADE STATUS EXTENDED (page does not exist)")|0x121||
|[SMSG_INITIALIZE_FACTIONS](https://wowdev.wiki/index.php?title=SMSG_INITIALIZE_FACTIONS&action=edit&redlink=1 "SMSG INITIALIZE FACTIONS (page does not exist)")|0x122||
|[SMSG_SET_FACTION_VISIBLE](https://wowdev.wiki/index.php?title=SMSG_SET_FACTION_VISIBLE&action=edit&redlink=1 "SMSG SET FACTION VISIBLE (page does not exist)")|0x123||
|[SMSG_SET_FACTION_STANDING](https://wowdev.wiki/index.php?title=SMSG_SET_FACTION_STANDING&action=edit&redlink=1 "SMSG SET FACTION STANDING (page does not exist)")|0x124||
|[CMSG_SET_FACTION_ATWAR](https://wowdev.wiki/index.php?title=CMSG_SET_FACTION_ATWAR&action=edit&redlink=1 "CMSG SET FACTION ATWAR (page does not exist)")|0x125||
|[CMSG_SET_FACTION_CHEAT](https://wowdev.wiki/index.php?title=CMSG_SET_FACTION_CHEAT&action=edit&redlink=1 "CMSG SET FACTION CHEAT (page does not exist)")|0x126||
|[SMSG_SET_PROFICIENCY](https://wowdev.wiki/index.php?title=SMSG_SET_PROFICIENCY&action=edit&redlink=1 "SMSG SET PROFICIENCY (page does not exist)")|0x127||
|[CMSG_SET_ACTION_BUTTON](https://wowdev.wiki/index.php?title=CMSG_SET_ACTION_BUTTON&action=edit&redlink=1 "CMSG SET ACTION BUTTON (page does not exist)")|0x128||
|[SMSG_ACTION_BUTTONS](https://wowdev.wiki/index.php?title=SMSG_ACTION_BUTTONS&action=edit&redlink=1 "SMSG ACTION BUTTONS (page does not exist)")|0x129||
|[SMSG_INITIAL_SPELLS](https://wowdev.wiki/index.php?title=SMSG_INITIAL_SPELLS&action=edit&redlink=1 "SMSG INITIAL SPELLS (page does not exist)")|0x12A||
|[SMSG_LEARNED_SPELL](https://wowdev.wiki/index.php?title=SMSG_LEARNED_SPELL&action=edit&redlink=1 "SMSG LEARNED SPELL (page does not exist)")|0x12B||
|[SMSG_SUPERCEDED_SPELL](https://wowdev.wiki/index.php?title=SMSG_SUPERCEDED_SPELL&action=edit&redlink=1 "SMSG SUPERCEDED SPELL (page does not exist)")|0x12C||
|[CMSG_NEW_SPELL_SLOT](https://wowdev.wiki/index.php?title=CMSG_NEW_SPELL_SLOT&action=edit&redlink=1 "CMSG NEW SPELL SLOT (page does not exist)")|0x12D||
|[CMSG_CAST_SPELL](https://wowdev.wiki/index.php?title=CMSG_CAST_SPELL&action=edit&redlink=1 "CMSG CAST SPELL (page does not exist)")|0x12E||
|[CMSG_CANCEL_CAST](https://wowdev.wiki/index.php?title=CMSG_CANCEL_CAST&action=edit&redlink=1 "CMSG CANCEL CAST (page does not exist)")|0x12F||
|[SMSG_CAST_FAILED](https://wowdev.wiki/index.php?title=SMSG_CAST_FAILED&action=edit&redlink=1 "SMSG CAST FAILED (page does not exist)")|0x130||
|[SMSG_SPELL_START](https://wowdev.wiki/index.php?title=SMSG_SPELL_START&action=edit&redlink=1 "SMSG SPELL START (page does not exist)")|0x131||
|[SMSG_SPELL_GO](https://wowdev.wiki/index.php?title=SMSG_SPELL_GO&action=edit&redlink=1 "SMSG SPELL GO (page does not exist)")|0x132||
|[SMSG_SPELL_FAILURE](https://wowdev.wiki/index.php?title=SMSG_SPELL_FAILURE&action=edit&redlink=1 "SMSG SPELL FAILURE (page does not exist)")|0x133||
|[SMSG_SPELL_COOLDOWN](https://wowdev.wiki/index.php?title=SMSG_SPELL_COOLDOWN&action=edit&redlink=1 "SMSG SPELL COOLDOWN (page does not exist)")|0x134||
|[SMSG_COOLDOWN_EVENT](https://wowdev.wiki/index.php?title=SMSG_COOLDOWN_EVENT&action=edit&redlink=1 "SMSG COOLDOWN EVENT (page does not exist)")|0x135||
|[CMSG_CANCEL_AURA](https://wowdev.wiki/index.php?title=CMSG_CANCEL_AURA&action=edit&redlink=1 "CMSG CANCEL AURA (page does not exist)")|0x136||
|[SMSG_UPDATE_AURA_DURATION_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_UPDATE_AURA_DURATION_OBSOLETE&action=edit&redlink=1 "SMSG UPDATE AURA DURATION OBSOLETE (page does not exist)")|0x137||
|[SMSG_PET_CAST_FAILED](https://wowdev.wiki/index.php?title=SMSG_PET_CAST_FAILED&action=edit&redlink=1 "SMSG PET CAST FAILED (page does not exist)")|0x138||
|[MSG_CHANNEL_START](https://wowdev.wiki/index.php?title=MSG_CHANNEL_START&action=edit&redlink=1 "MSG CHANNEL START (page does not exist)")|0x139||
|[MSG_CHANNEL_UPDATE](https://wowdev.wiki/index.php?title=MSG_CHANNEL_UPDATE&action=edit&redlink=1 "MSG CHANNEL UPDATE (page does not exist)")|0x13A||
|[CMSG_CANCEL_CHANNELLING](https://wowdev.wiki/index.php?title=CMSG_CANCEL_CHANNELLING&action=edit&redlink=1 "CMSG CANCEL CHANNELLING (page does not exist)")|0x13B||
|[SMSG_AI_REACTION](https://wowdev.wiki/index.php?title=SMSG_AI_REACTION&action=edit&redlink=1 "SMSG AI REACTION (page does not exist)")|0x13C||
|[CMSG_SET_SELECTION](https://wowdev.wiki/CMSG_SET_SELECTION "CMSG SET SELECTION")|0x13D||
|[CMSG_SET_TARGET_OBSOLETE](https://wowdev.wiki/index.php?title=CMSG_SET_TARGET_OBSOLETE&action=edit&redlink=1 "CMSG SET TARGET OBSOLETE (page does not exist)")|0x13E||
|[CMSG_UNUSED](https://wowdev.wiki/index.php?title=CMSG_UNUSED&action=edit&redlink=1 "CMSG UNUSED (page does not exist)")|0x13F||
|[CMSG_UNUSED2](https://wowdev.wiki/index.php?title=CMSG_UNUSED2&action=edit&redlink=1 "CMSG UNUSED2 (page does not exist)")|0x140||
|[CMSG_ATTACKSWING](https://wowdev.wiki/index.php?title=CMSG_ATTACKSWING&action=edit&redlink=1 "CMSG ATTACKSWING (page does not exist)")|0x141||
|[CMSG_ATTACKSTOP](https://wowdev.wiki/index.php?title=CMSG_ATTACKSTOP&action=edit&redlink=1 "CMSG ATTACKSTOP (page does not exist)")|0x142||
|[SMSG_ATTACKSTART](https://wowdev.wiki/index.php?title=SMSG_ATTACKSTART&action=edit&redlink=1 "SMSG ATTACKSTART (page does not exist)")|0x143||
|[SMSG_ATTACKSTOP](https://wowdev.wiki/index.php?title=SMSG_ATTACKSTOP&action=edit&redlink=1 "SMSG ATTACKSTOP (page does not exist)")|0x144||
|[SMSG_ATTACKSWING_NOTINRANGE](https://wowdev.wiki/index.php?title=SMSG_ATTACKSWING_NOTINRANGE&action=edit&redlink=1 "SMSG ATTACKSWING NOTINRANGE (page does not exist)")|0x145||
|[SMSG_ATTACKSWING_BADFACING](https://wowdev.wiki/index.php?title=SMSG_ATTACKSWING_BADFACING&action=edit&redlink=1 "SMSG ATTACKSWING BADFACING (page does not exist)")|0x146||
|[SMSG_ATTACKSWING_NOTSTANDING](https://wowdev.wiki/index.php?title=SMSG_ATTACKSWING_NOTSTANDING&action=edit&redlink=1 "SMSG ATTACKSWING NOTSTANDING (page does not exist)")|0x147||
|[SMSG_ATTACKSWING_DEADTARGET](https://wowdev.wiki/index.php?title=SMSG_ATTACKSWING_DEADTARGET&action=edit&redlink=1 "SMSG ATTACKSWING DEADTARGET (page does not exist)")|0x148||
|[SMSG_ATTACKSWING_CANT_ATTACK](https://wowdev.wiki/index.php?title=SMSG_ATTACKSWING_CANT_ATTACK&action=edit&redlink=1 "SMSG ATTACKSWING CANT ATTACK (page does not exist)")|0x149||
|[SMSG_ATTACKERSTATEUPDATE](https://wowdev.wiki/index.php?title=SMSG_ATTACKERSTATEUPDATE&action=edit&redlink=1 "SMSG ATTACKERSTATEUPDATE (page does not exist)")|0x14A||
|[SMSG_VICTIMSTATEUPDATE_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_VICTIMSTATEUPDATE_OBSOLETE&action=edit&redlink=1 "SMSG VICTIMSTATEUPDATE OBSOLETE (page does not exist)")|0x14B||
|[SMSG_DAMAGE_DONE_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_DAMAGE_DONE_OBSOLETE&action=edit&redlink=1 "SMSG DAMAGE DONE OBSOLETE (page does not exist)")|0x14C||
|[SMSG_DAMAGE_TAKEN_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_DAMAGE_TAKEN_OBSOLETE&action=edit&redlink=1 "SMSG DAMAGE TAKEN OBSOLETE (page does not exist)")|0x14D||
|[SMSG_CANCEL_COMBAT](https://wowdev.wiki/index.php?title=SMSG_CANCEL_COMBAT&action=edit&redlink=1 "SMSG CANCEL COMBAT (page does not exist)")|0x14E||
|[SMSG_SPELLBREAKLOG](https://wowdev.wiki/index.php?title=SMSG_SPELLBREAKLOG&action=edit&redlink=1 "SMSG SPELLBREAKLOG (page does not exist)")|0x14F||
|[SMSG_SPELLHEALLOG](https://wowdev.wiki/index.php?title=SMSG_SPELLHEALLOG&action=edit&redlink=1 "SMSG SPELLHEALLOG (page does not exist)")|0x150||
|[SMSG_SPELLENERGIZELOG](https://wowdev.wiki/index.php?title=SMSG_SPELLENERGIZELOG&action=edit&redlink=1 "SMSG SPELLENERGIZELOG (page does not exist)")|0x151||
|[CMSG_SHEATHE_OBSOLETE](https://wowdev.wiki/index.php?title=CMSG_SHEATHE_OBSOLETE&action=edit&redlink=1 "CMSG SHEATHE OBSOLETE (page does not exist)")|0x152||
|[CMSG_SAVE_PLAYER](https://wowdev.wiki/index.php?title=CMSG_SAVE_PLAYER&action=edit&redlink=1 "CMSG SAVE PLAYER (page does not exist)")|0x153||
|[CMSG_SETDEATHBINDPOINT](https://wowdev.wiki/index.php?title=CMSG_SETDEATHBINDPOINT&action=edit&redlink=1 "CMSG SETDEATHBINDPOINT (page does not exist)")|0x154||
|[SMSG_BINDPOINTUPDATE](https://wowdev.wiki/index.php?title=SMSG_BINDPOINTUPDATE&action=edit&redlink=1 "SMSG BINDPOINTUPDATE (page does not exist)")|0x155||
|[CMSG_GETDEATHBINDZONE](https://wowdev.wiki/index.php?title=CMSG_GETDEATHBINDZONE&action=edit&redlink=1 "CMSG GETDEATHBINDZONE (page does not exist)")|0x156||
|[SMSG_BINDZONEREPLY](https://wowdev.wiki/index.php?title=SMSG_BINDZONEREPLY&action=edit&redlink=1 "SMSG BINDZONEREPLY (page does not exist)")|0x157||
|[SMSG_PLAYERBOUND](https://wowdev.wiki/index.php?title=SMSG_PLAYERBOUND&action=edit&redlink=1 "SMSG PLAYERBOUND (page does not exist)")|0x158||
|[SMSG_CLIENT_CONTROL_UPDATE](https://wowdev.wiki/index.php?title=SMSG_CLIENT_CONTROL_UPDATE&action=edit&redlink=1 "SMSG CLIENT CONTROL UPDATE (page does not exist)")|0x159||
|[CMSG_REPOP_REQUEST](https://wowdev.wiki/index.php?title=CMSG_REPOP_REQUEST&action=edit&redlink=1 "CMSG REPOP REQUEST (page does not exist)")|0x15A||
|[SMSG_RESURRECT_REQUEST](https://wowdev.wiki/index.php?title=SMSG_RESURRECT_REQUEST&action=edit&redlink=1 "SMSG RESURRECT REQUEST (page does not exist)")|0x15B||
|[CMSG_RESURRECT_RESPONSE](https://wowdev.wiki/index.php?title=CMSG_RESURRECT_RESPONSE&action=edit&redlink=1 "CMSG RESURRECT RESPONSE (page does not exist)")|0x15C||
|[CMSG_LOOT](https://wowdev.wiki/index.php?title=CMSG_LOOT&action=edit&redlink=1 "CMSG LOOT (page does not exist)")|0x15D||
|[CMSG_LOOT_MONEY](https://wowdev.wiki/index.php?title=CMSG_LOOT_MONEY&action=edit&redlink=1 "CMSG LOOT MONEY (page does not exist)")|0x15E||
|[CMSG_LOOT_RELEASE](https://wowdev.wiki/index.php?title=CMSG_LOOT_RELEASE&action=edit&redlink=1 "CMSG LOOT RELEASE (page does not exist)")|0x15F||
|[SMSG_LOOT_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_LOOT_RESPONSE&action=edit&redlink=1 "SMSG LOOT RESPONSE (page does not exist)")|0x160||
|[SMSG_LOOT_RELEASE_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_LOOT_RELEASE_RESPONSE&action=edit&redlink=1 "SMSG LOOT RELEASE RESPONSE (page does not exist)")|0x161||
|[SMSG_LOOT_REMOVED](https://wowdev.wiki/index.php?title=SMSG_LOOT_REMOVED&action=edit&redlink=1 "SMSG LOOT REMOVED (page does not exist)")|0x162||
|[SMSG_LOOT_MONEY_NOTIFY](https://wowdev.wiki/index.php?title=SMSG_LOOT_MONEY_NOTIFY&action=edit&redlink=1 "SMSG LOOT MONEY NOTIFY (page does not exist)")|0x163||
|[SMSG_LOOT_ITEM_NOTIFY](https://wowdev.wiki/index.php?title=SMSG_LOOT_ITEM_NOTIFY&action=edit&redlink=1 "SMSG LOOT ITEM NOTIFY (page does not exist)")|0x164||
|[SMSG_LOOT_CLEAR_MONEY](https://wowdev.wiki/index.php?title=SMSG_LOOT_CLEAR_MONEY&action=edit&redlink=1 "SMSG LOOT CLEAR MONEY (page does not exist)")|0x165||
|[SMSG_ITEM_PUSH_RESULT](https://wowdev.wiki/index.php?title=SMSG_ITEM_PUSH_RESULT&action=edit&redlink=1 "SMSG ITEM PUSH RESULT (page does not exist)")|0x166||
|[SMSG_DUEL_REQUESTED](https://wowdev.wiki/index.php?title=SMSG_DUEL_REQUESTED&action=edit&redlink=1 "SMSG DUEL REQUESTED (page does not exist)")|0x167||
|[SMSG_DUEL_OUTOFBOUNDS](https://wowdev.wiki/index.php?title=SMSG_DUEL_OUTOFBOUNDS&action=edit&redlink=1 "SMSG DUEL OUTOFBOUNDS (page does not exist)")|0x168||
|[SMSG_DUEL_INBOUNDS](https://wowdev.wiki/index.php?title=SMSG_DUEL_INBOUNDS&action=edit&redlink=1 "SMSG DUEL INBOUNDS (page does not exist)")|0x169||
|[SMSG_DUEL_COMPLETE](https://wowdev.wiki/index.php?title=SMSG_DUEL_COMPLETE&action=edit&redlink=1 "SMSG DUEL COMPLETE (page does not exist)")|0x16A||
|[SMSG_DUEL_WINNER](https://wowdev.wiki/index.php?title=SMSG_DUEL_WINNER&action=edit&redlink=1 "SMSG DUEL WINNER (page does not exist)")|0x16B||
|[CMSG_DUEL_ACCEPTED](https://wowdev.wiki/index.php?title=CMSG_DUEL_ACCEPTED&action=edit&redlink=1 "CMSG DUEL ACCEPTED (page does not exist)")|0x16C||
|[CMSG_DUEL_CANCELLED](https://wowdev.wiki/index.php?title=CMSG_DUEL_CANCELLED&action=edit&redlink=1 "CMSG DUEL CANCELLED (page does not exist)")|0x16D||
|[SMSG_MOUNTRESULT](https://wowdev.wiki/index.php?title=SMSG_MOUNTRESULT&action=edit&redlink=1 "SMSG MOUNTRESULT (page does not exist)")|0x16E||
|[SMSG_DISMOUNTRESULT](https://wowdev.wiki/index.php?title=SMSG_DISMOUNTRESULT&action=edit&redlink=1 "SMSG DISMOUNTRESULT (page does not exist)")|0x16F||
|[SMSG_PUREMOUNT_CANCELLED_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_PUREMOUNT_CANCELLED_OBSOLETE&action=edit&redlink=1 "SMSG PUREMOUNT CANCELLED OBSOLETE (page does not exist)")|0x170||
|[CMSG_MOUNTSPECIAL_ANIM](https://wowdev.wiki/index.php?title=CMSG_MOUNTSPECIAL_ANIM&action=edit&redlink=1 "CMSG MOUNTSPECIAL ANIM (page does not exist)")|0x171||
|[SMSG_MOUNTSPECIAL_ANIM](https://wowdev.wiki/index.php?title=SMSG_MOUNTSPECIAL_ANIM&action=edit&redlink=1 "SMSG MOUNTSPECIAL ANIM (page does not exist)")|0x172||
|[SMSG_PET_TAME_FAILURE](https://wowdev.wiki/index.php?title=SMSG_PET_TAME_FAILURE&action=edit&redlink=1 "SMSG PET TAME FAILURE (page does not exist)")|0x173||
|[CMSG_PET_SET_ACTION](https://wowdev.wiki/index.php?title=CMSG_PET_SET_ACTION&action=edit&redlink=1 "CMSG PET SET ACTION (page does not exist)")|0x174||
|[CMSG_PET_ACTION](https://wowdev.wiki/index.php?title=CMSG_PET_ACTION&action=edit&redlink=1 "CMSG PET ACTION (page does not exist)")|0x175||
|[CMSG_PET_ABANDON](https://wowdev.wiki/index.php?title=CMSG_PET_ABANDON&action=edit&redlink=1 "CMSG PET ABANDON (page does not exist)")|0x176||
|[CMSG_PET_RENAME](https://wowdev.wiki/index.php?title=CMSG_PET_RENAME&action=edit&redlink=1 "CMSG PET RENAME (page does not exist)")|0x177||
|[SMSG_PET_NAME_INVALID](https://wowdev.wiki/index.php?title=SMSG_PET_NAME_INVALID&action=edit&redlink=1 "SMSG PET NAME INVALID (page does not exist)")|0x178||
|[SMSG_PET_SPELLS](https://wowdev.wiki/index.php?title=SMSG_PET_SPELLS&action=edit&redlink=1 "SMSG PET SPELLS (page does not exist)")|0x179||
|[SMSG_PET_MODE](https://wowdev.wiki/index.php?title=SMSG_PET_MODE&action=edit&redlink=1 "SMSG PET MODE (page does not exist)")|0x17A||
|[CMSG_GOSSIP_HELLO](https://wowdev.wiki/index.php?title=CMSG_GOSSIP_HELLO&action=edit&redlink=1 "CMSG GOSSIP HELLO (page does not exist)")|0x17B||
|[CMSG_GOSSIP_SELECT_OPTION](https://wowdev.wiki/index.php?title=CMSG_GOSSIP_SELECT_OPTION&action=edit&redlink=1 "CMSG GOSSIP SELECT OPTION (page does not exist)")|0x17C||
|[SMSG_GOSSIP_MESSAGE](https://wowdev.wiki/index.php?title=SMSG_GOSSIP_MESSAGE&action=edit&redlink=1 "SMSG GOSSIP MESSAGE (page does not exist)")|0x17D||
|[SMSG_GOSSIP_COMPLETE](https://wowdev.wiki/index.php?title=SMSG_GOSSIP_COMPLETE&action=edit&redlink=1 "SMSG GOSSIP COMPLETE (page does not exist)")|0x17E||
|[CMSG_NPC_TEXT_QUERY](https://wowdev.wiki/index.php?title=CMSG_NPC_TEXT_QUERY&action=edit&redlink=1 "CMSG NPC TEXT QUERY (page does not exist)")|0x17F||
|[SMSG_NPC_TEXT_UPDATE](https://wowdev.wiki/index.php?title=SMSG_NPC_TEXT_UPDATE&action=edit&redlink=1 "SMSG NPC TEXT UPDATE (page does not exist)")|0x180||
|[SMSG_NPC_WONT_TALK](https://wowdev.wiki/index.php?title=SMSG_NPC_WONT_TALK&action=edit&redlink=1 "SMSG NPC WONT TALK (page does not exist)")|0x181||
|[CMSG_QUESTGIVER_STATUS_QUERY](https://wowdev.wiki/index.php?title=CMSG_QUESTGIVER_STATUS_QUERY&action=edit&redlink=1 "CMSG QUESTGIVER STATUS QUERY (page does not exist)")|0x182||
|[SMSG_QUESTGIVER_STATUS](https://wowdev.wiki/index.php?title=SMSG_QUESTGIVER_STATUS&action=edit&redlink=1 "SMSG QUESTGIVER STATUS (page does not exist)")|0x183||
|[CMSG_QUESTGIVER_HELLO](https://wowdev.wiki/index.php?title=CMSG_QUESTGIVER_HELLO&action=edit&redlink=1 "CMSG QUESTGIVER HELLO (page does not exist)")|0x184||
|[SMSG_QUESTGIVER_QUEST_LIST](https://wowdev.wiki/index.php?title=SMSG_QUESTGIVER_QUEST_LIST&action=edit&redlink=1 "SMSG QUESTGIVER QUEST LIST (page does not exist)")|0x185||
|[CMSG_QUESTGIVER_QUERY_QUEST](https://wowdev.wiki/index.php?title=CMSG_QUESTGIVER_QUERY_QUEST&action=edit&redlink=1 "CMSG QUESTGIVER QUERY QUEST (page does not exist)")|0x186||
|[CMSG_QUESTGIVER_QUEST_AUTOLAUNCH](https://wowdev.wiki/index.php?title=CMSG_QUESTGIVER_QUEST_AUTOLAUNCH&action=edit&redlink=1 "CMSG QUESTGIVER QUEST AUTOLAUNCH (page does not exist)")|0x187||
|[SMSG_QUESTGIVER_QUEST_DETAILS](https://wowdev.wiki/index.php?title=SMSG_QUESTGIVER_QUEST_DETAILS&action=edit&redlink=1 "SMSG QUESTGIVER QUEST DETAILS (page does not exist)")|0x188||
|[CMSG_QUESTGIVER_ACCEPT_QUEST](https://wowdev.wiki/index.php?title=CMSG_QUESTGIVER_ACCEPT_QUEST&action=edit&redlink=1 "CMSG QUESTGIVER ACCEPT QUEST (page does not exist)")|0x189||
|[CMSG_QUESTGIVER_COMPLETE_QUEST](https://wowdev.wiki/index.php?title=CMSG_QUESTGIVER_COMPLETE_QUEST&action=edit&redlink=1 "CMSG QUESTGIVER COMPLETE QUEST (page does not exist)")|0x18A||
|[SMSG_QUESTGIVER_REQUEST_ITEMS](https://wowdev.wiki/index.php?title=SMSG_QUESTGIVER_REQUEST_ITEMS&action=edit&redlink=1 "SMSG QUESTGIVER REQUEST ITEMS (page does not exist)")|0x18B||
|[CMSG_QUESTGIVER_REQUEST_REWARD](https://wowdev.wiki/index.php?title=CMSG_QUESTGIVER_REQUEST_REWARD&action=edit&redlink=1 "CMSG QUESTGIVER REQUEST REWARD (page does not exist)")|0x18C||
|[SMSG_QUESTGIVER_OFFER_REWARD](https://wowdev.wiki/index.php?title=SMSG_QUESTGIVER_OFFER_REWARD&action=edit&redlink=1 "SMSG QUESTGIVER OFFER REWARD (page does not exist)")|0x18D||
|[CMSG_QUESTGIVER_CHOOSE_REWARD](https://wowdev.wiki/index.php?title=CMSG_QUESTGIVER_CHOOSE_REWARD&action=edit&redlink=1 "CMSG QUESTGIVER CHOOSE REWARD (page does not exist)")|0x18E||
|[SMSG_QUESTGIVER_QUEST_INVALID](https://wowdev.wiki/index.php?title=SMSG_QUESTGIVER_QUEST_INVALID&action=edit&redlink=1 "SMSG QUESTGIVER QUEST INVALID (page does not exist)")|0x18F||
|[CMSG_QUESTGIVER_CANCEL](https://wowdev.wiki/index.php?title=CMSG_QUESTGIVER_CANCEL&action=edit&redlink=1 "CMSG QUESTGIVER CANCEL (page does not exist)")|0x190||
|[SMSG_QUESTGIVER_QUEST_COMPLETE](https://wowdev.wiki/index.php?title=SMSG_QUESTGIVER_QUEST_COMPLETE&action=edit&redlink=1 "SMSG QUESTGIVER QUEST COMPLETE (page does not exist)")|0x191||
|[SMSG_QUESTGIVER_QUEST_FAILED](https://wowdev.wiki/index.php?title=SMSG_QUESTGIVER_QUEST_FAILED&action=edit&redlink=1 "SMSG QUESTGIVER QUEST FAILED (page does not exist)")|0x192||
|[CMSG_QUESTLOG_SWAP_QUEST](https://wowdev.wiki/index.php?title=CMSG_QUESTLOG_SWAP_QUEST&action=edit&redlink=1 "CMSG QUESTLOG SWAP QUEST (page does not exist)")|0x193||
|[CMSG_QUESTLOG_REMOVE_QUEST](https://wowdev.wiki/index.php?title=CMSG_QUESTLOG_REMOVE_QUEST&action=edit&redlink=1 "CMSG QUESTLOG REMOVE QUEST (page does not exist)")|0x194||
|[SMSG_QUESTLOG_FULL](https://wowdev.wiki/index.php?title=SMSG_QUESTLOG_FULL&action=edit&redlink=1 "SMSG QUESTLOG FULL (page does not exist)")|0x195||
|[SMSG_QUESTUPDATE_FAILED](https://wowdev.wiki/index.php?title=SMSG_QUESTUPDATE_FAILED&action=edit&redlink=1 "SMSG QUESTUPDATE FAILED (page does not exist)")|0x196||
|[SMSG_QUESTUPDATE_FAILEDTIMER](https://wowdev.wiki/index.php?title=SMSG_QUESTUPDATE_FAILEDTIMER&action=edit&redlink=1 "SMSG QUESTUPDATE FAILEDTIMER (page does not exist)")|0x197||
|[SMSG_QUESTUPDATE_COMPLETE](https://wowdev.wiki/index.php?title=SMSG_QUESTUPDATE_COMPLETE&action=edit&redlink=1 "SMSG QUESTUPDATE COMPLETE (page does not exist)")|0x198||
|[SMSG_QUESTUPDATE_ADD_KILL](https://wowdev.wiki/index.php?title=SMSG_QUESTUPDATE_ADD_KILL&action=edit&redlink=1 "SMSG QUESTUPDATE ADD KILL (page does not exist)")|0x199||
|[SMSG_QUESTUPDATE_ADD_ITEM](https://wowdev.wiki/index.php?title=SMSG_QUESTUPDATE_ADD_ITEM&action=edit&redlink=1 "SMSG QUESTUPDATE ADD ITEM (page does not exist)")|0x19A||
|[CMSG_QUEST_CONFIRM_ACCEPT](https://wowdev.wiki/index.php?title=CMSG_QUEST_CONFIRM_ACCEPT&action=edit&redlink=1 "CMSG QUEST CONFIRM ACCEPT (page does not exist)")|0x19B||
|[SMSG_QUEST_CONFIRM_ACCEPT](https://wowdev.wiki/index.php?title=SMSG_QUEST_CONFIRM_ACCEPT&action=edit&redlink=1 "SMSG QUEST CONFIRM ACCEPT (page does not exist)")|0x19C||
|[CMSG_PUSHQUESTTOPARTY](https://wowdev.wiki/index.php?title=CMSG_PUSHQUESTTOPARTY&action=edit&redlink=1 "CMSG PUSHQUESTTOPARTY (page does not exist)")|0x19D||
|[CMSG_LIST_INVENTORY](https://wowdev.wiki/index.php?title=CMSG_LIST_INVENTORY&action=edit&redlink=1 "CMSG LIST INVENTORY (page does not exist)")|0x19E||
|[SMSG_LIST_INVENTORY](https://wowdev.wiki/index.php?title=SMSG_LIST_INVENTORY&action=edit&redlink=1 "SMSG LIST INVENTORY (page does not exist)")|0x19F||
|[CMSG_SELL_ITEM](https://wowdev.wiki/index.php?title=CMSG_SELL_ITEM&action=edit&redlink=1 "CMSG SELL ITEM (page does not exist)")|0x1A0||
|[SMSG_SELL_ITEM](https://wowdev.wiki/index.php?title=SMSG_SELL_ITEM&action=edit&redlink=1 "SMSG SELL ITEM (page does not exist)")|0x1A1||
|[CMSG_BUY_ITEM](https://wowdev.wiki/index.php?title=CMSG_BUY_ITEM&action=edit&redlink=1 "CMSG BUY ITEM (page does not exist)")|0x1A2||
|[CMSG_BUY_ITEM_IN_SLOT](https://wowdev.wiki/index.php?title=CMSG_BUY_ITEM_IN_SLOT&action=edit&redlink=1 "CMSG BUY ITEM IN SLOT (page does not exist)")|0x1A3||
|[SMSG_BUY_ITEM](https://wowdev.wiki/index.php?title=SMSG_BUY_ITEM&action=edit&redlink=1 "SMSG BUY ITEM (page does not exist)")|0x1A4||
|[SMSG_BUY_FAILED](https://wowdev.wiki/index.php?title=SMSG_BUY_FAILED&action=edit&redlink=1 "SMSG BUY FAILED (page does not exist)")|0x1A5||
|[CMSG_TAXICLEARALLNODES](https://wowdev.wiki/index.php?title=CMSG_TAXICLEARALLNODES&action=edit&redlink=1 "CMSG TAXICLEARALLNODES (page does not exist)")|0x1A6||
|[CMSG_TAXIENABLEALLNODES](https://wowdev.wiki/index.php?title=CMSG_TAXIENABLEALLNODES&action=edit&redlink=1 "CMSG TAXIENABLEALLNODES (page does not exist)")|0x1A7||
|[CMSG_TAXISHOWNODES](https://wowdev.wiki/index.php?title=CMSG_TAXISHOWNODES&action=edit&redlink=1 "CMSG TAXISHOWNODES (page does not exist)")|0x1A8||
|[SMSG_SHOWTAXINODES](https://wowdev.wiki/index.php?title=SMSG_SHOWTAXINODES&action=edit&redlink=1 "SMSG SHOWTAXINODES (page does not exist)")|0x1A9||
|[CMSG_TAXINODE_STATUS_QUERY](https://wowdev.wiki/index.php?title=CMSG_TAXINODE_STATUS_QUERY&action=edit&redlink=1 "CMSG TAXINODE STATUS QUERY (page does not exist)")|0x1AA||
|[SMSG_TAXINODE_STATUS](https://wowdev.wiki/index.php?title=SMSG_TAXINODE_STATUS&action=edit&redlink=1 "SMSG TAXINODE STATUS (page does not exist)")|0x1AB||
|[CMSG_TAXIQUERYAVAILABLENODES](https://wowdev.wiki/index.php?title=CMSG_TAXIQUERYAVAILABLENODES&action=edit&redlink=1 "CMSG TAXIQUERYAVAILABLENODES (page does not exist)")\| 0x1AC||
|[CMSG_ACTIVATETAXI](https://wowdev.wiki/index.php?title=CMSG_ACTIVATETAXI&action=edit&redlink=1 "CMSG ACTIVATETAXI (page does not exist)")|0x1AD||
|[SMSG_ACTIVATETAXIREPLY](https://wowdev.wiki/index.php?title=SMSG_ACTIVATETAXIREPLY&action=edit&redlink=1 "SMSG ACTIVATETAXIREPLY (page does not exist)")|0x1AE||
|[SMSG_NEW_TAXI_PATH](https://wowdev.wiki/index.php?title=SMSG_NEW_TAXI_PATH&action=edit&redlink=1 "SMSG NEW TAXI PATH (page does not exist)")|0x1AF||
|[CMSG_TRAINER_LIST](https://wowdev.wiki/index.php?title=CMSG_TRAINER_LIST&action=edit&redlink=1 "CMSG TRAINER LIST (page does not exist)")|0x1B0||
|[SMSG_TRAINER_LIST](https://wowdev.wiki/index.php?title=SMSG_TRAINER_LIST&action=edit&redlink=1 "SMSG TRAINER LIST (page does not exist)")|0x1B1||
|[CMSG_TRAINER_BUY_SPELL](https://wowdev.wiki/index.php?title=CMSG_TRAINER_BUY_SPELL&action=edit&redlink=1 "CMSG TRAINER BUY SPELL (page does not exist)")|0x1B2||
|[SMSG_TRAINER_BUY_SUCCEEDED](https://wowdev.wiki/index.php?title=SMSG_TRAINER_BUY_SUCCEEDED&action=edit&redlink=1 "SMSG TRAINER BUY SUCCEEDED (page does not exist)")|0x1B3||
|[SMSG_TRAINER_BUY_FAILED](https://wowdev.wiki/index.php?title=SMSG_TRAINER_BUY_FAILED&action=edit&redlink=1 "SMSG TRAINER BUY FAILED (page does not exist)")|0x1B4||
|[CMSG_BINDER_ACTIVATE](https://wowdev.wiki/index.php?title=CMSG_BINDER_ACTIVATE&action=edit&redlink=1 "CMSG BINDER ACTIVATE (page does not exist)")|0x1B5||
|[SMSG_PLAYERBINDERROR](https://wowdev.wiki/index.php?title=SMSG_PLAYERBINDERROR&action=edit&redlink=1 "SMSG PLAYERBINDERROR (page does not exist)")|0x1B6||
|[CMSG_BANKER_ACTIVATE](https://wowdev.wiki/index.php?title=CMSG_BANKER_ACTIVATE&action=edit&redlink=1 "CMSG BANKER ACTIVATE (page does not exist)")|0x1B7||
|[SMSG_SHOW_BANK](https://wowdev.wiki/index.php?title=SMSG_SHOW_BANK&action=edit&redlink=1 "SMSG SHOW BANK (page does not exist)")|0x1B8||
|[CMSG_BUY_BANK_SLOT](https://wowdev.wiki/index.php?title=CMSG_BUY_BANK_SLOT&action=edit&redlink=1 "CMSG BUY BANK SLOT (page does not exist)")|0x1B9||
|[SMSG_BUY_BANK_SLOT_RESULT](https://wowdev.wiki/index.php?title=SMSG_BUY_BANK_SLOT_RESULT&action=edit&redlink=1 "SMSG BUY BANK SLOT RESULT (page does not exist)")|0x1BA||
|[CMSG_PETITION_SHOWLIST](https://wowdev.wiki/index.php?title=CMSG_PETITION_SHOWLIST&action=edit&redlink=1 "CMSG PETITION SHOWLIST (page does not exist)")|0x1BB||
|[SMSG_PETITION_SHOWLIST](https://wowdev.wiki/index.php?title=SMSG_PETITION_SHOWLIST&action=edit&redlink=1 "SMSG PETITION SHOWLIST (page does not exist)")|0x1BC||
|[CMSG_PETITION_BUY](https://wowdev.wiki/index.php?title=CMSG_PETITION_BUY&action=edit&redlink=1 "CMSG PETITION BUY (page does not exist)")|0x1BD||
|[CMSG_PETITION_SHOW_SIGNATURES](https://wowdev.wiki/index.php?title=CMSG_PETITION_SHOW_SIGNATURES&action=edit&redlink=1 "CMSG PETITION SHOW SIGNATURES (page does not exist)")|0x1BE||
|[SMSG_PETITION_SHOW_SIGNATURES](https://wowdev.wiki/index.php?title=SMSG_PETITION_SHOW_SIGNATURES&action=edit&redlink=1 "SMSG PETITION SHOW SIGNATURES (page does not exist)")|0x1BF||
|[CMSG_PETITION_SIGN](https://wowdev.wiki/index.php?title=CMSG_PETITION_SIGN&action=edit&redlink=1 "CMSG PETITION SIGN (page does not exist)")|0x1C0||
|[SMSG_PETITION_SIGN_RESULTS](https://wowdev.wiki/index.php?title=SMSG_PETITION_SIGN_RESULTS&action=edit&redlink=1 "SMSG PETITION SIGN RESULTS (page does not exist)")|0x1C1||
|[MSG_PETITION_DECLINE](https://wowdev.wiki/index.php?title=MSG_PETITION_DECLINE&action=edit&redlink=1 "MSG PETITION DECLINE (page does not exist)")|0x1C2||
|[CMSG_OFFER_PETITION](https://wowdev.wiki/index.php?title=CMSG_OFFER_PETITION&action=edit&redlink=1 "CMSG OFFER PETITION (page does not exist)")|0x1C3||
|[CMSG_TURN_IN_PETITION](https://wowdev.wiki/index.php?title=CMSG_TURN_IN_PETITION&action=edit&redlink=1 "CMSG TURN IN PETITION (page does not exist)")|0x1C4||
|[SMSG_TURN_IN_PETITION_RESULTS](https://wowdev.wiki/index.php?title=SMSG_TURN_IN_PETITION_RESULTS&action=edit&redlink=1 "SMSG TURN IN PETITION RESULTS (page does not exist)")|0x1C5||
|[CMSG_PETITION_QUERY](https://wowdev.wiki/index.php?title=CMSG_PETITION_QUERY&action=edit&redlink=1 "CMSG PETITION QUERY (page does not exist)")|0x1C6||
|[SMSG_PETITION_QUERY_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_PETITION_QUERY_RESPONSE&action=edit&redlink=1 "SMSG PETITION QUERY RESPONSE (page does not exist)")|0x1C7||
|[SMSG_FISH_NOT_HOOKED](https://wowdev.wiki/index.php?title=SMSG_FISH_NOT_HOOKED&action=edit&redlink=1 "SMSG FISH NOT HOOKED (page does not exist)")|0x1C8||
|[SMSG_FISH_ESCAPED](https://wowdev.wiki/index.php?title=SMSG_FISH_ESCAPED&action=edit&redlink=1 "SMSG FISH ESCAPED (page does not exist)")|0x1C9||
|[CMSG_BUG](https://wowdev.wiki/index.php?title=CMSG_BUG&action=edit&redlink=1 "CMSG BUG (page does not exist)")|0x1CA||
|[SMSG_NOTIFICATION](https://wowdev.wiki/index.php?title=SMSG_NOTIFICATION&action=edit&redlink=1 "SMSG NOTIFICATION (page does not exist)")|0x1CB||
|[CMSG_PLAYED_TIME](https://wowdev.wiki/index.php?title=CMSG_PLAYED_TIME&action=edit&redlink=1 "CMSG PLAYED TIME (page does not exist)")|0x1CC||
|[SMSG_PLAYED_TIME](https://wowdev.wiki/index.php?title=SMSG_PLAYED_TIME&action=edit&redlink=1 "SMSG PLAYED TIME (page does not exist)")|0x1CD||
|[CMSG_QUERY_TIME](https://wowdev.wiki/index.php?title=CMSG_QUERY_TIME&action=edit&redlink=1 "CMSG QUERY TIME (page does not exist)")|0x1CE||
|[SMSG_QUERY_TIME_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_QUERY_TIME_RESPONSE&action=edit&redlink=1 "SMSG QUERY TIME RESPONSE (page does not exist)")|0x1CF||
|[SMSG_LOG_XPGAIN](https://wowdev.wiki/index.php?title=SMSG_LOG_XPGAIN&action=edit&redlink=1 "SMSG LOG XPGAIN (page does not exist)")|0x1D0||
|[SMSG_AURACASTLOG](https://wowdev.wiki/index.php?title=SMSG_AURACASTLOG&action=edit&redlink=1 "SMSG AURACASTLOG (page does not exist)")|0x1D1||
|[CMSG_RECLAIM_CORPSE](https://wowdev.wiki/index.php?title=CMSG_RECLAIM_CORPSE&action=edit&redlink=1 "CMSG RECLAIM CORPSE (page does not exist)")|0x1D2||
|[CMSG_WRAP_ITEM](https://wowdev.wiki/index.php?title=CMSG_WRAP_ITEM&action=edit&redlink=1 "CMSG WRAP ITEM (page does not exist)")|0x1D3||
|[SMSG_LEVELUP_INFO](https://wowdev.wiki/index.php?title=SMSG_LEVELUP_INFO&action=edit&redlink=1 "SMSG LEVELUP INFO (page does not exist)")|0x1D4||
|[MSG_MINIMAP_PING](https://wowdev.wiki/index.php?title=MSG_MINIMAP_PING&action=edit&redlink=1 "MSG MINIMAP PING (page does not exist)")|0x1D5||
|[SMSG_RESISTLOG](https://wowdev.wiki/index.php?title=SMSG_RESISTLOG&action=edit&redlink=1 "SMSG RESISTLOG (page does not exist)")|0x1D6||
|[SMSG_ENCHANTMENTLOG](https://wowdev.wiki/index.php?title=SMSG_ENCHANTMENTLOG&action=edit&redlink=1 "SMSG ENCHANTMENTLOG (page does not exist)")|0x1D7||
|[CMSG_SET_SKILL_CHEAT](https://wowdev.wiki/index.php?title=CMSG_SET_SKILL_CHEAT&action=edit&redlink=1 "CMSG SET SKILL CHEAT (page does not exist)")|0x1D8||
|[SMSG_START_MIRROR_TIMER](https://wowdev.wiki/index.php?title=SMSG_START_MIRROR_TIMER&action=edit&redlink=1 "SMSG START MIRROR TIMER (page does not exist)")|0x1D9||
|[SMSG_PAUSE_MIRROR_TIMER](https://wowdev.wiki/index.php?title=SMSG_PAUSE_MIRROR_TIMER&action=edit&redlink=1 "SMSG PAUSE MIRROR TIMER (page does not exist)")|0x1DA||
|[SMSG_STOP_MIRROR_TIMER](https://wowdev.wiki/index.php?title=SMSG_STOP_MIRROR_TIMER&action=edit&redlink=1 "SMSG STOP MIRROR TIMER (page does not exist)")|0x1DB||
|[CMSG_PING](https://wowdev.wiki/CMSG_PING "CMSG PING")|0x1DC||
|[SMSG_PONG](https://wowdev.wiki/SMSG_PONG "SMSG PONG")|0x1DD||
|[SMSG_CLEAR_COOLDOWN](https://wowdev.wiki/index.php?title=SMSG_CLEAR_COOLDOWN&action=edit&redlink=1 "SMSG CLEAR COOLDOWN (page does not exist)")|0x1DE||
|[SMSG_GAMEOBJECT_PAGETEXT](https://wowdev.wiki/index.php?title=SMSG_GAMEOBJECT_PAGETEXT&action=edit&redlink=1 "SMSG GAMEOBJECT PAGETEXT (page does not exist)")|0x1DF||
|[CMSG_SETSHEATHED](https://wowdev.wiki/index.php?title=CMSG_SETSHEATHED&action=edit&redlink=1 "CMSG SETSHEATHED (page does not exist)")|0x1E0||
|[SMSG_COOLDOWN_CHEAT](https://wowdev.wiki/index.php?title=SMSG_COOLDOWN_CHEAT&action=edit&redlink=1 "SMSG COOLDOWN CHEAT (page does not exist)")|0x1E1||
|[SMSG_SPELL_DELAYED](https://wowdev.wiki/index.php?title=SMSG_SPELL_DELAYED&action=edit&redlink=1 "SMSG SPELL DELAYED (page does not exist)")|0x1E2||
|[CMSG_PLAYER_MACRO_OBSOLETE](https://wowdev.wiki/index.php?title=CMSG_PLAYER_MACRO_OBSOLETE&action=edit&redlink=1 "CMSG PLAYER MACRO OBSOLETE (page does not exist)")|0x1E3||
|[SMSG_PLAYER_MACRO_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_PLAYER_MACRO_OBSOLETE&action=edit&redlink=1 "SMSG PLAYER MACRO OBSOLETE (page does not exist)")|0x1E4||
|[CMSG_GHOST](https://wowdev.wiki/index.php?title=CMSG_GHOST&action=edit&redlink=1 "CMSG GHOST (page does not exist)")|0x1E5||
|[CMSG_GM_INVIS](https://wowdev.wiki/index.php?title=CMSG_GM_INVIS&action=edit&redlink=1 "CMSG GM INVIS (page does not exist)")|0x1E6||
|[SMSG_INVALID_PROMOTION_CODE](https://wowdev.wiki/index.php?title=SMSG_INVALID_PROMOTION_CODE&action=edit&redlink=1 "SMSG INVALID PROMOTION CODE (page does not exist)")|0x1E7||
|[MSG_GM_BIND_OTHER](https://wowdev.wiki/index.php?title=MSG_GM_BIND_OTHER&action=edit&redlink=1 "MSG GM BIND OTHER (page does not exist)")|0x1E8||
|[MSG_GM_SUMMON](https://wowdev.wiki/index.php?title=MSG_GM_SUMMON&action=edit&redlink=1 "MSG GM SUMMON (page does not exist)")|0x1E9||
|[SMSG_ITEM_TIME_UPDATE](https://wowdev.wiki/index.php?title=SMSG_ITEM_TIME_UPDATE&action=edit&redlink=1 "SMSG ITEM TIME UPDATE (page does not exist)")|0x1EA||
|[SMSG_ITEM_ENCHANT_TIME_UPDATE](https://wowdev.wiki/index.php?title=SMSG_ITEM_ENCHANT_TIME_UPDATE&action=edit&redlink=1 "SMSG ITEM ENCHANT TIME UPDATE (page does not exist)")|0x1EB||
|[SMSG_AUTH_CHALLENGE](https://wowdev.wiki/SMSG_AUTH_CHALLENGE "SMSG AUTH CHALLENGE")|0x1EC||
|[CMSG_AUTH_SESSION](https://wowdev.wiki/CMSG_AUTH_SESSION "CMSG AUTH SESSION")|0x1ED||
|[SMSG_AUTH_RESPONSE](https://wowdev.wiki/SMSG_AUTH_RESPONSE "SMSG AUTH RESPONSE")|0x1EE||
|[MSG_GM_SHOWLABEL](https://wowdev.wiki/index.php?title=MSG_GM_SHOWLABEL&action=edit&redlink=1 "MSG GM SHOWLABEL (page does not exist)")|0x1EF||
|[CMSG_PET_CAST_SPELL](https://wowdev.wiki/index.php?title=CMSG_PET_CAST_SPELL&action=edit&redlink=1 "CMSG PET CAST SPELL (page does not exist)")|0x1F0||
|[MSG_SAVE_GUILD_EMBLEM](https://wowdev.wiki/index.php?title=MSG_SAVE_GUILD_EMBLEM&action=edit&redlink=1 "MSG SAVE GUILD EMBLEM (page does not exist)")|0x1F1||
|[MSG_TABARDVENDOR_ACTIVATE](https://wowdev.wiki/index.php?title=MSG_TABARDVENDOR_ACTIVATE&action=edit&redlink=1 "MSG TABARDVENDOR ACTIVATE (page does not exist)")|0x1F2||
|[SMSG_PLAY_SPELL_VISUAL](https://wowdev.wiki/index.php?title=SMSG_PLAY_SPELL_VISUAL&action=edit&redlink=1 "SMSG PLAY SPELL VISUAL (page does not exist)")|0x1F3||
|[CMSG_ZONEUPDATE](https://wowdev.wiki/index.php?title=CMSG_ZONEUPDATE&action=edit&redlink=1 "CMSG ZONEUPDATE (page does not exist)")|0x1F4||
|[SMSG_PARTYKILLLOG](https://wowdev.wiki/index.php?title=SMSG_PARTYKILLLOG&action=edit&redlink=1 "SMSG PARTYKILLLOG (page does not exist)")|0x1F5||
|[SMSG_COMPRESSED_UPDATE_OBJECT](https://wowdev.wiki/index.php?title=SMSG_COMPRESSED_UPDATE_OBJECT&action=edit&redlink=1 "SMSG COMPRESSED UPDATE OBJECT (page does not exist)")|0x1F6||
|[SMSG_PLAY_SPELL_IMPACT](https://wowdev.wiki/index.php?title=SMSG_PLAY_SPELL_IMPACT&action=edit&redlink=1 "SMSG PLAY SPELL IMPACT (page does not exist)")|0x1F7||
|[SMSG_EXPLORATION_EXPERIENCE](https://wowdev.wiki/index.php?title=SMSG_EXPLORATION_EXPERIENCE&action=edit&redlink=1 "SMSG EXPLORATION EXPERIENCE (page does not exist)")|0x1F8||
|[CMSG_GM_SET_SECURITY_GROUP](https://wowdev.wiki/index.php?title=CMSG_GM_SET_SECURITY_GROUP&action=edit&redlink=1 "CMSG GM SET SECURITY GROUP (page does not exist)")|0x1F9||
|[CMSG_GM_NUKE](https://wowdev.wiki/index.php?title=CMSG_GM_NUKE&action=edit&redlink=1 "CMSG GM NUKE (page does not exist)")|0x1FA|not used in client|
|[MSG_RANDOM_ROLL](https://wowdev.wiki/index.php?title=MSG_RANDOM_ROLL&action=edit&redlink=1 "MSG RANDOM ROLL (page does not exist)")|0x1FB||
|[SMSG_ENVIRONMENTALDAMAGELOG](https://wowdev.wiki/index.php?title=SMSG_ENVIRONMENTALDAMAGELOG&action=edit&redlink=1 "SMSG ENVIRONMENTALDAMAGELOG (page does not exist)")|0x1FC||
|[CMSG_RWHOIS_OBSOLETE](https://wowdev.wiki/index.php?title=CMSG_RWHOIS_OBSOLETE&action=edit&redlink=1 "CMSG RWHOIS OBSOLETE (page does not exist)")|0x1FD|not used in client|
|[SMSG_RWHOIS](https://wowdev.wiki/index.php?title=SMSG_RWHOIS&action=edit&redlink=1 "SMSG RWHOIS (page does not exist)")|0x1FE||
|[MSG_LOOKING_FOR_GROUP](https://wowdev.wiki/index.php?title=MSG_LOOKING_FOR_GROUP&action=edit&redlink=1 "MSG LOOKING FOR GROUP (page does not exist)")|0x1FF||
|[CMSG_SET_LOOKING_FOR_GROUP](https://wowdev.wiki/index.php?title=CMSG_SET_LOOKING_FOR_GROUP&action=edit&redlink=1 "CMSG SET LOOKING FOR GROUP (page does not exist)")|0x200||
|[CMSG_UNLEARN_SPELL](https://wowdev.wiki/index.php?title=CMSG_UNLEARN_SPELL&action=edit&redlink=1 "CMSG UNLEARN SPELL (page does not exist)")|0x201||
|[CMSG_UNLEARN_SKILL](https://wowdev.wiki/index.php?title=CMSG_UNLEARN_SKILL&action=edit&redlink=1 "CMSG UNLEARN SKILL (page does not exist)")|0x202||
|[SMSG_REMOVED_SPELL](https://wowdev.wiki/index.php?title=SMSG_REMOVED_SPELL&action=edit&redlink=1 "SMSG REMOVED SPELL (page does not exist)")|0x203||
|[CMSG_DECHARGE](https://wowdev.wiki/index.php?title=CMSG_DECHARGE&action=edit&redlink=1 "CMSG DECHARGE (page does not exist)")|0x204||
|[CMSG_GMTICKET_CREATE](https://wowdev.wiki/index.php?title=CMSG_GMTICKET_CREATE&action=edit&redlink=1 "CMSG GMTICKET CREATE (page does not exist)")|0x205||
|[SMSG_GMTICKET_CREATE](https://wowdev.wiki/index.php?title=SMSG_GMTICKET_CREATE&action=edit&redlink=1 "SMSG GMTICKET CREATE (page does not exist)")|0x206||
|[CMSG_GMTICKET_UPDATETEXT](https://wowdev.wiki/index.php?title=CMSG_GMTICKET_UPDATETEXT&action=edit&redlink=1 "CMSG GMTICKET UPDATETEXT (page does not exist)")|0x207||
|[SMSG_GMTICKET_UPDATETEXT](https://wowdev.wiki/index.php?title=SMSG_GMTICKET_UPDATETEXT&action=edit&redlink=1 "SMSG GMTICKET UPDATETEXT (page does not exist)")|0x208||
|[SMSG_ACCOUNT_DATA_TIMES](https://wowdev.wiki/index.php?title=SMSG_ACCOUNT_DATA_TIMES&action=edit&redlink=1 "SMSG ACCOUNT DATA TIMES (page does not exist)")|0x209||
|[CMSG_REQUEST_ACCOUNT_DATA](https://wowdev.wiki/index.php?title=CMSG_REQUEST_ACCOUNT_DATA&action=edit&redlink=1 "CMSG REQUEST ACCOUNT DATA (page does not exist)")|0x20A||
|[CMSG_UPDATE_ACCOUNT_DATA](https://wowdev.wiki/index.php?title=CMSG_UPDATE_ACCOUNT_DATA&action=edit&redlink=1 "CMSG UPDATE ACCOUNT DATA (page does not exist)")|0x20B||
|[SMSG_UPDATE_ACCOUNT_DATA](https://wowdev.wiki/index.php?title=SMSG_UPDATE_ACCOUNT_DATA&action=edit&redlink=1 "SMSG UPDATE ACCOUNT DATA (page does not exist)")|0x20C||
|[SMSG_CLEAR_FAR_SIGHT_IMMEDIATE](https://wowdev.wiki/index.php?title=SMSG_CLEAR_FAR_SIGHT_IMMEDIATE&action=edit&redlink=1 "SMSG CLEAR FAR SIGHT IMMEDIATE (page does not exist)")|0x20D||
|[SMSG_POWERGAINLOG_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_POWERGAINLOG_OBSOLETE&action=edit&redlink=1 "SMSG POWERGAINLOG OBSOLETE (page does not exist)")|0x20E||
|[CMSG_GM_TEACH](https://wowdev.wiki/index.php?title=CMSG_GM_TEACH&action=edit&redlink=1 "CMSG GM TEACH (page does not exist)")|0x20F||
|[CMSG_GM_CREATE_ITEM_TARGET](https://wowdev.wiki/index.php?title=CMSG_GM_CREATE_ITEM_TARGET&action=edit&redlink=1 "CMSG GM CREATE ITEM TARGET (page does not exist)")|0x210||
|[CMSG_GMTICKET_GETTICKET](https://wowdev.wiki/index.php?title=CMSG_GMTICKET_GETTICKET&action=edit&redlink=1 "CMSG GMTICKET GETTICKET (page does not exist)")|0x211||
|[SMSG_GMTICKET_GETTICKET](https://wowdev.wiki/index.php?title=SMSG_GMTICKET_GETTICKET&action=edit&redlink=1 "SMSG GMTICKET GETTICKET (page does not exist)")|0x212||
|[CMSG_UNLEARN_TALENTS](https://wowdev.wiki/index.php?title=CMSG_UNLEARN_TALENTS&action=edit&redlink=1 "CMSG UNLEARN TALENTS (page does not exist)")|0x213||
|[SMSG_GAMEOBJECT_SPAWN_ANIM_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_GAMEOBJECT_SPAWN_ANIM_OBSOLETE&action=edit&redlink=1 "SMSG GAMEOBJECT SPAWN ANIM OBSOLETE (page does not exist)")|0x214||
|[SMSG_GAMEOBJECT_DESPAWN_ANIM](https://wowdev.wiki/index.php?title=SMSG_GAMEOBJECT_DESPAWN_ANIM&action=edit&redlink=1 "SMSG GAMEOBJECT DESPAWN ANIM (page does not exist)")|0x215||
|[MSG_CORPSE_QUERY](https://wowdev.wiki/index.php?title=MSG_CORPSE_QUERY&action=edit&redlink=1 "MSG CORPSE QUERY (page does not exist)")|0x216||
|[CMSG_GMTICKET_DELETETICKET](https://wowdev.wiki/index.php?title=CMSG_GMTICKET_DELETETICKET&action=edit&redlink=1 "CMSG GMTICKET DELETETICKET (page does not exist)")|0x217||
|[SMSG_GMTICKET_DELETETICKET](https://wowdev.wiki/index.php?title=SMSG_GMTICKET_DELETETICKET&action=edit&redlink=1 "SMSG GMTICKET DELETETICKET (page does not exist)")|0x218||
|[SMSG_CHAT_WRONG_FACTION](https://wowdev.wiki/index.php?title=SMSG_CHAT_WRONG_FACTION&action=edit&redlink=1 "SMSG CHAT WRONG FACTION (page does not exist)")|0x219||
|[CMSG_GMTICKET_SYSTEMSTATUS](https://wowdev.wiki/index.php?title=CMSG_GMTICKET_SYSTEMSTATUS&action=edit&redlink=1 "CMSG GMTICKET SYSTEMSTATUS (page does not exist)")|0x21A||
|[SMSG_GMTICKET_SYSTEMSTATUS](https://wowdev.wiki/index.php?title=SMSG_GMTICKET_SYSTEMSTATUS&action=edit&redlink=1 "SMSG GMTICKET SYSTEMSTATUS (page does not exist)")|0x21B||
|[CMSG_SPIRIT_HEALER_ACTIVATE](https://wowdev.wiki/index.php?title=CMSG_SPIRIT_HEALER_ACTIVATE&action=edit&redlink=1 "CMSG SPIRIT HEALER ACTIVATE (page does not exist)")|0x21C||
|[CMSG_SET_STAT_CHEAT](https://wowdev.wiki/index.php?title=CMSG_SET_STAT_CHEAT&action=edit&redlink=1 "CMSG SET STAT CHEAT (page does not exist)")|0x21D||
|[SMSG_SET_REST_START_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_SET_REST_START_OBSOLETE&action=edit&redlink=1 "SMSG SET REST START OBSOLETE (page does not exist)")|0x21E||
|[CMSG_SKILL_BUY_STEP](https://wowdev.wiki/index.php?title=CMSG_SKILL_BUY_STEP&action=edit&redlink=1 "CMSG SKILL BUY STEP (page does not exist)")|0x21F||
|[CMSG_SKILL_BUY_RANK](https://wowdev.wiki/index.php?title=CMSG_SKILL_BUY_RANK&action=edit&redlink=1 "CMSG SKILL BUY RANK (page does not exist)")|0x220||
|[CMSG_XP_CHEAT](https://wowdev.wiki/index.php?title=CMSG_XP_CHEAT&action=edit&redlink=1 "CMSG XP CHEAT (page does not exist)")|0x221||
|[SMSG_SPIRIT_HEALER_CONFIRM](https://wowdev.wiki/index.php?title=SMSG_SPIRIT_HEALER_CONFIRM&action=edit&redlink=1 "SMSG SPIRIT HEALER CONFIRM (page does not exist)")|0x222||
|[CMSG_CHARACTER_POINT_CHEAT](https://wowdev.wiki/index.php?title=CMSG_CHARACTER_POINT_CHEAT&action=edit&redlink=1 "CMSG CHARACTER POINT CHEAT (page does not exist)")|0x223||
|[SMSG_GOSSIP_POI](https://wowdev.wiki/index.php?title=SMSG_GOSSIP_POI&action=edit&redlink=1 "SMSG GOSSIP POI (page does not exist)")|0x224||
|[CMSG_CHAT_IGNORED](https://wowdev.wiki/index.php?title=CMSG_CHAT_IGNORED&action=edit&redlink=1 "CMSG CHAT IGNORED (page does not exist)")|0x225||
|[CMSG_GM_VISION](https://wowdev.wiki/index.php?title=CMSG_GM_VISION&action=edit&redlink=1 "CMSG GM VISION (page does not exist)")|0x226||
|[CMSG_SERVER_COMMAND](https://wowdev.wiki/index.php?title=CMSG_SERVER_COMMAND&action=edit&redlink=1 "CMSG SERVER COMMAND (page does not exist)")|0x227||
|[CMSG_GM_SILENCE](https://wowdev.wiki/index.php?title=CMSG_GM_SILENCE&action=edit&redlink=1 "CMSG GM SILENCE (page does not exist)")|0x228||
|[CMSG_GM_REVEALTO](https://wowdev.wiki/index.php?title=CMSG_GM_REVEALTO&action=edit&redlink=1 "CMSG GM REVEALTO (page does not exist)")|0x229||
|[CMSG_GM_RESURRECT](https://wowdev.wiki/index.php?title=CMSG_GM_RESURRECT&action=edit&redlink=1 "CMSG GM RESURRECT (page does not exist)")|0x22A||
|[CMSG_GM_SUMMONMOB](https://wowdev.wiki/index.php?title=CMSG_GM_SUMMONMOB&action=edit&redlink=1 "CMSG GM SUMMONMOB (page does not exist)")|0x22B||
|[CMSG_GM_MOVECORPSE](https://wowdev.wiki/index.php?title=CMSG_GM_MOVECORPSE&action=edit&redlink=1 "CMSG GM MOVECORPSE (page does not exist)")|0x22C||
|[CMSG_GM_FREEZE](https://wowdev.wiki/index.php?title=CMSG_GM_FREEZE&action=edit&redlink=1 "CMSG GM FREEZE (page does not exist)")|0x22D||
|[CMSG_GM_UBERINVIS](https://wowdev.wiki/index.php?title=CMSG_GM_UBERINVIS&action=edit&redlink=1 "CMSG GM UBERINVIS (page does not exist)")|0x22E||
|[CMSG_GM_REQUEST_PLAYER_INFO](https://wowdev.wiki/index.php?title=CMSG_GM_REQUEST_PLAYER_INFO&action=edit&redlink=1 "CMSG GM REQUEST PLAYER INFO (page does not exist)")|0x22F||
|[SMSG_GM_PLAYER_INFO](https://wowdev.wiki/index.php?title=SMSG_GM_PLAYER_INFO&action=edit&redlink=1 "SMSG GM PLAYER INFO (page does not exist)")|0x230||
|[CMSG_GUILD_RANK](https://wowdev.wiki/index.php?title=CMSG_GUILD_RANK&action=edit&redlink=1 "CMSG GUILD RANK (page does not exist)")|0x231||
|[CMSG_GUILD_ADD_RANK](https://wowdev.wiki/index.php?title=CMSG_GUILD_ADD_RANK&action=edit&redlink=1 "CMSG GUILD ADD RANK (page does not exist)")|0x232||
|[CMSG_GUILD_DEL_RANK](https://wowdev.wiki/index.php?title=CMSG_GUILD_DEL_RANK&action=edit&redlink=1 "CMSG GUILD DEL RANK (page does not exist)")|0x233||
|[CMSG_GUILD_SET_PUBLIC_NOTE](https://wowdev.wiki/index.php?title=CMSG_GUILD_SET_PUBLIC_NOTE&action=edit&redlink=1 "CMSG GUILD SET PUBLIC NOTE (page does not exist)")|0x234||
|[CMSG_GUILD_SET_OFFICER_NOTE](https://wowdev.wiki/index.php?title=CMSG_GUILD_SET_OFFICER_NOTE&action=edit&redlink=1 "CMSG GUILD SET OFFICER NOTE (page does not exist)")|0x235||
|[SMSG_LOGIN_VERIFY_WORLD](https://wowdev.wiki/SMSG_LOGIN_VERIFY_WORLD "SMSG LOGIN VERIFY WORLD")|0x236||
|[CMSG_CLEAR_EXPLORATION](https://wowdev.wiki/index.php?title=CMSG_CLEAR_EXPLORATION&action=edit&redlink=1 "CMSG CLEAR EXPLORATION (page does not exist)")|0x237||
|[CMSG_SEND_MAIL](https://wowdev.wiki/index.php?title=CMSG_SEND_MAIL&action=edit&redlink=1 "CMSG SEND MAIL (page does not exist)")|0x238||
|[SMSG_SEND_MAIL_RESULT](https://wowdev.wiki/index.php?title=SMSG_SEND_MAIL_RESULT&action=edit&redlink=1 "SMSG SEND MAIL RESULT (page does not exist)")|0x239||
|[CMSG_GET_MAIL_LIST](https://wowdev.wiki/index.php?title=CMSG_GET_MAIL_LIST&action=edit&redlink=1 "CMSG GET MAIL LIST (page does not exist)")|0x23A||
|[SMSG_MAIL_LIST_RESULT](https://wowdev.wiki/index.php?title=SMSG_MAIL_LIST_RESULT&action=edit&redlink=1 "SMSG MAIL LIST RESULT (page does not exist)")|0x23B||
|[CMSG_BATTLEFIELD_LIST](https://wowdev.wiki/index.php?title=CMSG_BATTLEFIELD_LIST&action=edit&redlink=1 "CMSG BATTLEFIELD LIST (page does not exist)")|0x23C||
|[SMSG_BATTLEFIELD_LIST](https://wowdev.wiki/index.php?title=SMSG_BATTLEFIELD_LIST&action=edit&redlink=1 "SMSG BATTLEFIELD LIST (page does not exist)")|0x23D||
|[CMSG_BATTLEFIELD_JOIN](https://wowdev.wiki/index.php?title=CMSG_BATTLEFIELD_JOIN&action=edit&redlink=1 "CMSG BATTLEFIELD JOIN (page does not exist)")|0x23E||
|[SMSG_BATTLEFIELD_WIN_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_BATTLEFIELD_WIN_OBSOLETE&action=edit&redlink=1 "SMSG BATTLEFIELD WIN OBSOLETE (page does not exist)")|0x23F||
|[SMSG_BATTLEFIELD_LOSE_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_BATTLEFIELD_LOSE_OBSOLETE&action=edit&redlink=1 "SMSG BATTLEFIELD LOSE OBSOLETE (page does not exist)")|0x240||
|[CMSG_TAXICLEARNODE](https://wowdev.wiki/index.php?title=CMSG_TAXICLEARNODE&action=edit&redlink=1 "CMSG TAXICLEARNODE (page does not exist)")|0x241||
|[CMSG_TAXIENABLENODE](https://wowdev.wiki/index.php?title=CMSG_TAXIENABLENODE&action=edit&redlink=1 "CMSG TAXIENABLENODE (page does not exist)")|0x242||
|[CMSG_ITEM_TEXT_QUERY](https://wowdev.wiki/index.php?title=CMSG_ITEM_TEXT_QUERY&action=edit&redlink=1 "CMSG ITEM TEXT QUERY (page does not exist)")|0x243||
|[SMSG_ITEM_TEXT_QUERY_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_ITEM_TEXT_QUERY_RESPONSE&action=edit&redlink=1 "SMSG ITEM TEXT QUERY RESPONSE (page does not exist)")|0x244||
|[CMSG_MAIL_TAKE_MONEY](https://wowdev.wiki/index.php?title=CMSG_MAIL_TAKE_MONEY&action=edit&redlink=1 "CMSG MAIL TAKE MONEY (page does not exist)")|0x245||
|[CMSG_MAIL_TAKE_ITEM](https://wowdev.wiki/index.php?title=CMSG_MAIL_TAKE_ITEM&action=edit&redlink=1 "CMSG MAIL TAKE ITEM (page does not exist)")|0x246||
|[CMSG_MAIL_MARK_AS_READ](https://wowdev.wiki/index.php?title=CMSG_MAIL_MARK_AS_READ&action=edit&redlink=1 "CMSG MAIL MARK AS READ (page does not exist)")|0x247||
|[CMSG_MAIL_RETURN_TO_SENDER](https://wowdev.wiki/index.php?title=CMSG_MAIL_RETURN_TO_SENDER&action=edit&redlink=1 "CMSG MAIL RETURN TO SENDER (page does not exist)")|0x248||
|[CMSG_MAIL_DELETE](https://wowdev.wiki/index.php?title=CMSG_MAIL_DELETE&action=edit&redlink=1 "CMSG MAIL DELETE (page does not exist)")|0x249||
|[CMSG_MAIL_CREATE_TEXT_ITEM](https://wowdev.wiki/index.php?title=CMSG_MAIL_CREATE_TEXT_ITEM&action=edit&redlink=1 "CMSG MAIL CREATE TEXT ITEM (page does not exist)")|0x24A||
|[SMSG_SPELLLOGMISS](https://wowdev.wiki/index.php?title=SMSG_SPELLLOGMISS&action=edit&redlink=1 "SMSG SPELLLOGMISS (page does not exist)")|0x24B||
|[SMSG_SPELLLOGEXECUTE](https://wowdev.wiki/index.php?title=SMSG_SPELLLOGEXECUTE&action=edit&redlink=1 "SMSG SPELLLOGEXECUTE (page does not exist)")|0x24C||
|[SMSG_DEBUGAURAPROC](https://wowdev.wiki/index.php?title=SMSG_DEBUGAURAPROC&action=edit&redlink=1 "SMSG DEBUGAURAPROC (page does not exist)")|0x24D||
|[SMSG_PERIODICAURALOG](https://wowdev.wiki/index.php?title=SMSG_PERIODICAURALOG&action=edit&redlink=1 "SMSG PERIODICAURALOG (page does not exist)")|0x24E||
|[SMSG_SPELLDAMAGESHIELD](https://wowdev.wiki/index.php?title=SMSG_SPELLDAMAGESHIELD&action=edit&redlink=1 "SMSG SPELLDAMAGESHIELD (page does not exist)")|0x24F||
|[SMSG_SPELLNONMELEEDAMAGELOG](https://wowdev.wiki/index.php?title=SMSG_SPELLNONMELEEDAMAGELOG&action=edit&redlink=1 "SMSG SPELLNONMELEEDAMAGELOG (page does not exist)")|0x250||
|[CMSG_LEARN_TALENT](https://wowdev.wiki/index.php?title=CMSG_LEARN_TALENT&action=edit&redlink=1 "CMSG LEARN TALENT (page does not exist)")|0x251||
|[SMSG_RESURRECT_FAILED](https://wowdev.wiki/index.php?title=SMSG_RESURRECT_FAILED&action=edit&redlink=1 "SMSG RESURRECT FAILED (page does not exist)")|0x252||
|[CMSG_TOGGLE_PVP](https://wowdev.wiki/index.php?title=CMSG_TOGGLE_PVP&action=edit&redlink=1 "CMSG TOGGLE PVP (page does not exist)")|0x253||
|[SMSG_ZONE_UNDER_ATTACK](https://wowdev.wiki/index.php?title=SMSG_ZONE_UNDER_ATTACK&action=edit&redlink=1 "SMSG ZONE UNDER ATTACK (page does not exist)")|0x254||
|[MSG_AUCTION_HELLO](https://wowdev.wiki/index.php?title=MSG_AUCTION_HELLO&action=edit&redlink=1 "MSG AUCTION HELLO (page does not exist)")|0x255||
|[CMSG_AUCTION_SELL_ITEM](https://wowdev.wiki/index.php?title=CMSG_AUCTION_SELL_ITEM&action=edit&redlink=1 "CMSG AUCTION SELL ITEM (page does not exist)")|0x256||
|[CMSG_AUCTION_REMOVE_ITEM](https://wowdev.wiki/index.php?title=CMSG_AUCTION_REMOVE_ITEM&action=edit&redlink=1 "CMSG AUCTION REMOVE ITEM (page does not exist)")|0x257||
|[CMSG_AUCTION_LIST_ITEMS](https://wowdev.wiki/index.php?title=CMSG_AUCTION_LIST_ITEMS&action=edit&redlink=1 "CMSG AUCTION LIST ITEMS (page does not exist)")|0x258||
|[CMSG_AUCTION_LIST_OWNER_ITEMS](https://wowdev.wiki/index.php?title=CMSG_AUCTION_LIST_OWNER_ITEMS&action=edit&redlink=1 "CMSG AUCTION LIST OWNER ITEMS (page does not exist)")|0x259||
|[CMSG_AUCTION_PLACE_BID](https://wowdev.wiki/index.php?title=CMSG_AUCTION_PLACE_BID&action=edit&redlink=1 "CMSG AUCTION PLACE BID (page does not exist)")|0x25A||
|[SMSG_AUCTION_COMMAND_RESULT](https://wowdev.wiki/index.php?title=SMSG_AUCTION_COMMAND_RESULT&action=edit&redlink=1 "SMSG AUCTION COMMAND RESULT (page does not exist)")|0x25B||
|[SMSG_AUCTION_LIST_RESULT](https://wowdev.wiki/index.php?title=SMSG_AUCTION_LIST_RESULT&action=edit&redlink=1 "SMSG AUCTION LIST RESULT (page does not exist)")|0x25C||
|[SMSG_AUCTION_OWNER_LIST_RESULT](https://wowdev.wiki/index.php?title=SMSG_AUCTION_OWNER_LIST_RESULT&action=edit&redlink=1 "SMSG AUCTION OWNER LIST RESULT (page does not exist)")|0x25D||
|[SMSG_AUCTION_BIDDER_NOTIFICATION](https://wowdev.wiki/index.php?title=SMSG_AUCTION_BIDDER_NOTIFICATION&action=edit&redlink=1 "SMSG AUCTION BIDDER NOTIFICATION (page does not exist)")|0x25E||
|[SMSG_AUCTION_OWNER_NOTIFICATION](https://wowdev.wiki/index.php?title=SMSG_AUCTION_OWNER_NOTIFICATION&action=edit&redlink=1 "SMSG AUCTION OWNER NOTIFICATION (page does not exist)")|0x25F||
|[SMSG_PROCRESIST](https://wowdev.wiki/index.php?title=SMSG_PROCRESIST&action=edit&redlink=1 "SMSG PROCRESIST (page does not exist)")|0x260||
|[SMSG_STANDSTATE_CHANGE_FAILURE_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_STANDSTATE_CHANGE_FAILURE_OBSOLETE&action=edit&redlink=1 "SMSG STANDSTATE CHANGE FAILURE OBSOLETE (page does not exist)")|0x261||
|[SMSG_DISPEL_FAILED](https://wowdev.wiki/index.php?title=SMSG_DISPEL_FAILED&action=edit&redlink=1 "SMSG DISPEL FAILED (page does not exist)")|0x262||
|[SMSG_SPELLORDAMAGE_IMMUNE](https://wowdev.wiki/index.php?title=SMSG_SPELLORDAMAGE_IMMUNE&action=edit&redlink=1 "SMSG SPELLORDAMAGE IMMUNE (page does not exist)")|0x263||
|[CMSG_AUCTION_LIST_BIDDER_ITEMS](https://wowdev.wiki/index.php?title=CMSG_AUCTION_LIST_BIDDER_ITEMS&action=edit&redlink=1 "CMSG AUCTION LIST BIDDER ITEMS (page does not exist)")|0x264||
|[SMSG_AUCTION_BIDDER_LIST_RESULT](https://wowdev.wiki/index.php?title=SMSG_AUCTION_BIDDER_LIST_RESULT&action=edit&redlink=1 "SMSG AUCTION BIDDER LIST RESULT (page does not exist)")|0x265||
|[SMSG_SET_FLAT_SPELL_MODIFIER](https://wowdev.wiki/index.php?title=SMSG_SET_FLAT_SPELL_MODIFIER&action=edit&redlink=1 "SMSG SET FLAT SPELL MODIFIER (page does not exist)")|0x266||
|[SMSG_SET_PCT_SPELL_MODIFIER](https://wowdev.wiki/index.php?title=SMSG_SET_PCT_SPELL_MODIFIER&action=edit&redlink=1 "SMSG SET PCT SPELL MODIFIER (page does not exist)")|0x267||
|[CMSG_SET_AMMO](https://wowdev.wiki/index.php?title=CMSG_SET_AMMO&action=edit&redlink=1 "CMSG SET AMMO (page does not exist)")|0x268||
|[SMSG_CORPSE_RECLAIM_DELAY](https://wowdev.wiki/index.php?title=SMSG_CORPSE_RECLAIM_DELAY&action=edit&redlink=1 "SMSG CORPSE RECLAIM DELAY (page does not exist)")|0x269||
|[CMSG_SET_ACTIVE_MOVER](https://wowdev.wiki/CMSG_SET_ACTIVE_MOVER "CMSG SET ACTIVE MOVER")|0x26A||
|[CMSG_PET_CANCEL_AURA](https://wowdev.wiki/index.php?title=CMSG_PET_CANCEL_AURA&action=edit&redlink=1 "CMSG PET CANCEL AURA (page does not exist)")|0x26B||
|[CMSG_PLAYER_AI_CHEAT](https://wowdev.wiki/index.php?title=CMSG_PLAYER_AI_CHEAT&action=edit&redlink=1 "CMSG PLAYER AI CHEAT (page does not exist)")|0x26C||
|[CMSG_CANCEL_AUTO_REPEAT_SPELL](https://wowdev.wiki/index.php?title=CMSG_CANCEL_AUTO_REPEAT_SPELL&action=edit&redlink=1 "CMSG CANCEL AUTO REPEAT SPELL (page does not exist)")|0x26D||
|[MSG_GM_ACCOUNT_ONLINE](https://wowdev.wiki/index.php?title=MSG_GM_ACCOUNT_ONLINE&action=edit&redlink=1 "MSG GM ACCOUNT ONLINE (page does not exist)")|0x26E||
|[MSG_LIST_STABLED_PETS](https://wowdev.wiki/index.php?title=MSG_LIST_STABLED_PETS&action=edit&redlink=1 "MSG LIST STABLED PETS (page does not exist)")|0x26F||
|[CMSG_STABLE_PET](https://wowdev.wiki/index.php?title=CMSG_STABLE_PET&action=edit&redlink=1 "CMSG STABLE PET (page does not exist)")|0x270||
|[CMSG_UNSTABLE_PET](https://wowdev.wiki/index.php?title=CMSG_UNSTABLE_PET&action=edit&redlink=1 "CMSG UNSTABLE PET (page does not exist)")|0x271||
|[CMSG_BUY_STABLE_SLOT](https://wowdev.wiki/index.php?title=CMSG_BUY_STABLE_SLOT&action=edit&redlink=1 "CMSG BUY STABLE SLOT (page does not exist)")|0x272||
|[SMSG_STABLE_RESULT](https://wowdev.wiki/index.php?title=SMSG_STABLE_RESULT&action=edit&redlink=1 "SMSG STABLE RESULT (page does not exist)")|0x273||
|[CMSG_STABLE_REVIVE_PET](https://wowdev.wiki/index.php?title=CMSG_STABLE_REVIVE_PET&action=edit&redlink=1 "CMSG STABLE REVIVE PET (page does not exist)")|0x274||
|[CMSG_STABLE_SWAP_PET](https://wowdev.wiki/index.php?title=CMSG_STABLE_SWAP_PET&action=edit&redlink=1 "CMSG STABLE SWAP PET (page does not exist)")|0x275||
|[MSG_QUEST_PUSH_RESULT](https://wowdev.wiki/index.php?title=MSG_QUEST_PUSH_RESULT&action=edit&redlink=1 "MSG QUEST PUSH RESULT (page does not exist)")|0x276||
|[SMSG_PLAY_MUSIC](https://wowdev.wiki/index.php?title=SMSG_PLAY_MUSIC&action=edit&redlink=1 "SMSG PLAY MUSIC (page does not exist)")|0x277||
|[SMSG_PLAY_OBJECT_SOUND](https://wowdev.wiki/index.php?title=SMSG_PLAY_OBJECT_SOUND&action=edit&redlink=1 "SMSG PLAY OBJECT SOUND (page does not exist)")|0x278||
|[CMSG_REQUEST_PET_INFO](https://wowdev.wiki/index.php?title=CMSG_REQUEST_PET_INFO&action=edit&redlink=1 "CMSG REQUEST PET INFO (page does not exist)")|0x279||
|[CMSG_FAR_SIGHT](https://wowdev.wiki/index.php?title=CMSG_FAR_SIGHT&action=edit&redlink=1 "CMSG FAR SIGHT (page does not exist)")|0x27A||
|[SMSG_SPELLDISPELLOG](https://wowdev.wiki/index.php?title=SMSG_SPELLDISPELLOG&action=edit&redlink=1 "SMSG SPELLDISPELLOG (page does not exist)")|0x27B||
|[SMSG_DAMAGE_CALC_LOG](https://wowdev.wiki/index.php?title=SMSG_DAMAGE_CALC_LOG&action=edit&redlink=1 "SMSG DAMAGE CALC LOG (page does not exist)")|0x27C||
|[CMSG_ENABLE_DAMAGE_LOG](https://wowdev.wiki/index.php?title=CMSG_ENABLE_DAMAGE_LOG&action=edit&redlink=1 "CMSG ENABLE DAMAGE LOG (page does not exist)")|0x27D||
|[CMSG_GROUP_CHANGE_SUB_GROUP](https://wowdev.wiki/index.php?title=CMSG_GROUP_CHANGE_SUB_GROUP&action=edit&redlink=1 "CMSG GROUP CHANGE SUB GROUP (page does not exist)")|0x27E||
|[CMSG_REQUEST_PARTY_MEMBER_STATS](https://wowdev.wiki/index.php?title=CMSG_REQUEST_PARTY_MEMBER_STATS&action=edit&redlink=1 "CMSG REQUEST PARTY MEMBER STATS (page does not exist)")|0x27F||
|[CMSG_GROUP_SWAP_SUB_GROUP](https://wowdev.wiki/index.php?title=CMSG_GROUP_SWAP_SUB_GROUP&action=edit&redlink=1 "CMSG GROUP SWAP SUB GROUP (page does not exist)")|0x280||
|[CMSG_RESET_FACTION_CHEAT](https://wowdev.wiki/index.php?title=CMSG_RESET_FACTION_CHEAT&action=edit&redlink=1 "CMSG RESET FACTION CHEAT (page does not exist)")|0x281||
|[CMSG_AUTOSTORE_BANK_ITEM](https://wowdev.wiki/index.php?title=CMSG_AUTOSTORE_BANK_ITEM&action=edit&redlink=1 "CMSG AUTOSTORE BANK ITEM (page does not exist)")|0x282||
|[CMSG_AUTOBANK_ITEM](https://wowdev.wiki/index.php?title=CMSG_AUTOBANK_ITEM&action=edit&redlink=1 "CMSG AUTOBANK ITEM (page does not exist)")|0x283||
|[MSG_QUERY_NEXT_MAIL_TIME](https://wowdev.wiki/index.php?title=MSG_QUERY_NEXT_MAIL_TIME&action=edit&redlink=1 "MSG QUERY NEXT MAIL TIME (page does not exist)")|0x284||
|[SMSG_RECEIVED_MAIL](https://wowdev.wiki/index.php?title=SMSG_RECEIVED_MAIL&action=edit&redlink=1 "SMSG RECEIVED MAIL (page does not exist)")|0x285||
|[SMSG_RAID_GROUP_ONLY](https://wowdev.wiki/index.php?title=SMSG_RAID_GROUP_ONLY&action=edit&redlink=1 "SMSG RAID GROUP ONLY (page does not exist)")|0x286||
|[CMSG_SET_DURABILITY_CHEAT](https://wowdev.wiki/index.php?title=CMSG_SET_DURABILITY_CHEAT&action=edit&redlink=1 "CMSG SET DURABILITY CHEAT (page does not exist)")|0x287||
|[CMSG_SET_PVP_RANK_CHEAT](https://wowdev.wiki/index.php?title=CMSG_SET_PVP_RANK_CHEAT&action=edit&redlink=1 "CMSG SET PVP RANK CHEAT (page does not exist)")|0x288||
|[CMSG_ADD_PVP_MEDAL_CHEAT](https://wowdev.wiki/index.php?title=CMSG_ADD_PVP_MEDAL_CHEAT&action=edit&redlink=1 "CMSG ADD PVP MEDAL CHEAT (page does not exist)")|0x289||
|[CMSG_DEL_PVP_MEDAL_CHEAT](https://wowdev.wiki/index.php?title=CMSG_DEL_PVP_MEDAL_CHEAT&action=edit&redlink=1 "CMSG DEL PVP MEDAL CHEAT (page does not exist)")|0x28A||
|[CMSG_SET_PVP_TITLE](https://wowdev.wiki/index.php?title=CMSG_SET_PVP_TITLE&action=edit&redlink=1 "CMSG SET PVP TITLE (page does not exist)")|0x28B||
|[SMSG_PVP_CREDIT](https://wowdev.wiki/index.php?title=SMSG_PVP_CREDIT&action=edit&redlink=1 "SMSG PVP CREDIT (page does not exist)")|0x28C||
|[SMSG_AUCTION_REMOVED_NOTIFICATION](https://wowdev.wiki/index.php?title=SMSG_AUCTION_REMOVED_NOTIFICATION&action=edit&redlink=1 "SMSG AUCTION REMOVED NOTIFICATION (page does not exist)")|0x28D||
|[CMSG_GROUP_RAID_CONVERT](https://wowdev.wiki/index.php?title=CMSG_GROUP_RAID_CONVERT&action=edit&redlink=1 "CMSG GROUP RAID CONVERT (page does not exist)")|0x28E||
|[CMSG_GROUP_ASSISTANT_LEADER](https://wowdev.wiki/index.php?title=CMSG_GROUP_ASSISTANT_LEADER&action=edit&redlink=1 "CMSG GROUP ASSISTANT LEADER (page does not exist)")|0x28F||
|[CMSG_BUYBACK_ITEM](https://wowdev.wiki/index.php?title=CMSG_BUYBACK_ITEM&action=edit&redlink=1 "CMSG BUYBACK ITEM (page does not exist)")|0x290||
|[SMSG_SERVER_MESSAGE](https://wowdev.wiki/index.php?title=SMSG_SERVER_MESSAGE&action=edit&redlink=1 "SMSG SERVER MESSAGE (page does not exist)")|0x291||
|[CMSG_MEETINGSTONE_JOIN](https://wowdev.wiki/index.php?title=CMSG_MEETINGSTONE_JOIN&action=edit&redlink=1 "CMSG MEETINGSTONE JOIN (page does not exist)")|0x292||
|[CMSG_MEETINGSTONE_LEAVE](https://wowdev.wiki/index.php?title=CMSG_MEETINGSTONE_LEAVE&action=edit&redlink=1 "CMSG MEETINGSTONE LEAVE (page does not exist)")|0x293||
|[CMSG_MEETINGSTONE_CHEAT](https://wowdev.wiki/index.php?title=CMSG_MEETINGSTONE_CHEAT&action=edit&redlink=1 "CMSG MEETINGSTONE CHEAT (page does not exist)")|0x294||
|[SMSG_MEETINGSTONE_SETQUEUE](https://wowdev.wiki/index.php?title=SMSG_MEETINGSTONE_SETQUEUE&action=edit&redlink=1 "SMSG MEETINGSTONE SETQUEUE (page does not exist)")\||0x295||
|[CMSG_MEETINGSTONE_INFO](https://wowdev.wiki/index.php?title=CMSG_MEETINGSTONE_INFO&action=edit&redlink=1 "CMSG MEETINGSTONE INFO (page does not exist)")|0x296||
|[SMSG_MEETINGSTONE_COMPLETE](https://wowdev.wiki/index.php?title=SMSG_MEETINGSTONE_COMPLETE&action=edit&redlink=1 "SMSG MEETINGSTONE COMPLETE (page does not exist)")|0x297||
|[SMSG_MEETINGSTONE_IN_PROGRESS](https://wowdev.wiki/index.php?title=SMSG_MEETINGSTONE_IN_PROGRESS&action=edit&redlink=1 "SMSG MEETINGSTONE IN PROGRESS (page does not exist)")|0x298||
|[SMSG_MEETINGSTONE_MEMBER_ADDED](https://wowdev.wiki/index.php?title=SMSG_MEETINGSTONE_MEMBER_ADDED&action=edit&redlink=1 "SMSG MEETINGSTONE MEMBER ADDED (page does not exist)")|0x299||
|[CMSG_GMTICKETSYSTEM_TOGGLE](https://wowdev.wiki/index.php?title=CMSG_GMTICKETSYSTEM_TOGGLE&action=edit&redlink=1 "CMSG GMTICKETSYSTEM TOGGLE (page does not exist)")|0x29A||
|[CMSG_CANCEL_GROWTH_AURA](https://wowdev.wiki/index.php?title=CMSG_CANCEL_GROWTH_AURA&action=edit&redlink=1 "CMSG CANCEL GROWTH AURA (page does not exist)")|0x29B||
|[SMSG_CANCEL_AUTO_REPEAT](https://wowdev.wiki/index.php?title=SMSG_CANCEL_AUTO_REPEAT&action=edit&redlink=1 "SMSG CANCEL AUTO REPEAT (page does not exist)")|0x29C||
|[SMSG_STANDSTATE_UPDATE](https://wowdev.wiki/index.php?title=SMSG_STANDSTATE_UPDATE&action=edit&redlink=1 "SMSG STANDSTATE UPDATE (page does not exist)")|0x29D||
|[SMSG_LOOT_ALL_PASSED](https://wowdev.wiki/index.php?title=SMSG_LOOT_ALL_PASSED&action=edit&redlink=1 "SMSG LOOT ALL PASSED (page does not exist)")|0x29E||
|[SMSG_LOOT_ROLL_WON](https://wowdev.wiki/index.php?title=SMSG_LOOT_ROLL_WON&action=edit&redlink=1 "SMSG LOOT ROLL WON (page does not exist)")|0x29F||
|[CMSG_LOOT_ROLL](https://wowdev.wiki/index.php?title=CMSG_LOOT_ROLL&action=edit&redlink=1 "CMSG LOOT ROLL (page does not exist)")|0x2A0||
|[SMSG_LOOT_START_ROLL](https://wowdev.wiki/index.php?title=SMSG_LOOT_START_ROLL&action=edit&redlink=1 "SMSG LOOT START ROLL (page does not exist)")|0x2A1||
|[SMSG_LOOT_ROLL](https://wowdev.wiki/index.php?title=SMSG_LOOT_ROLL&action=edit&redlink=1 "SMSG LOOT ROLL (page does not exist)")|0x2A2||
|[CMSG_LOOT_MASTER_GIVE](https://wowdev.wiki/index.php?title=CMSG_LOOT_MASTER_GIVE&action=edit&redlink=1 "CMSG LOOT MASTER GIVE (page does not exist)")|0x2A3||
|[SMSG_LOOT_MASTER_LIST](https://wowdev.wiki/index.php?title=SMSG_LOOT_MASTER_LIST&action=edit&redlink=1 "SMSG LOOT MASTER LIST (page does not exist)")|0x2A4||
|[SMSG_SET_FORCED_REACTIONS](https://wowdev.wiki/index.php?title=SMSG_SET_FORCED_REACTIONS&action=edit&redlink=1 "SMSG SET FORCED REACTIONS (page does not exist)")|0x2A5||
|[SMSG_SPELL_FAILED_OTHER](https://wowdev.wiki/index.php?title=SMSG_SPELL_FAILED_OTHER&action=edit&redlink=1 "SMSG SPELL FAILED OTHER (page does not exist)")|0x2A6||
|[SMSG_GAMEOBJECT_RESET_STATE](https://wowdev.wiki/index.php?title=SMSG_GAMEOBJECT_RESET_STATE&action=edit&redlink=1 "SMSG GAMEOBJECT RESET STATE (page does not exist)")|0x2A7||
|[CMSG_REPAIR_ITEM](https://wowdev.wiki/index.php?title=CMSG_REPAIR_ITEM&action=edit&redlink=1 "CMSG REPAIR ITEM (page does not exist)")|0x2A8||
|[SMSG_CHAT_PLAYER_NOT_FOUND](https://wowdev.wiki/index.php?title=SMSG_CHAT_PLAYER_NOT_FOUND&action=edit&redlink=1 "SMSG CHAT PLAYER NOT FOUND (page does not exist)")|0x2A9||
|[MSG_TALENT_WIPE_CONFIRM](https://wowdev.wiki/index.php?title=MSG_TALENT_WIPE_CONFIRM&action=edit&redlink=1 "MSG TALENT WIPE CONFIRM (page does not exist)")|0x2AA||
|[SMSG_SUMMON_REQUEST](https://wowdev.wiki/index.php?title=SMSG_SUMMON_REQUEST&action=edit&redlink=1 "SMSG SUMMON REQUEST (page does not exist)")|0x2AB||
|[CMSG_SUMMON_RESPONSE](https://wowdev.wiki/index.php?title=CMSG_SUMMON_RESPONSE&action=edit&redlink=1 "CMSG SUMMON RESPONSE (page does not exist)")|0x2AC||
|[MSG_MOVE_TOGGLE_GRAVITY_CHEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_TOGGLE_GRAVITY_CHEAT&action=edit&redlink=1 "MSG MOVE TOGGLE GRAVITY CHEAT (page does not exist)")|0x2AD||
|[SMSG_MONSTER_MOVE_TRANSPORT](https://wowdev.wiki/index.php?title=SMSG_MONSTER_MOVE_TRANSPORT&action=edit&redlink=1 "SMSG MONSTER MOVE TRANSPORT (page does not exist)")|0x2AE||
|[SMSG_PET_BROKEN](https://wowdev.wiki/index.php?title=SMSG_PET_BROKEN&action=edit&redlink=1 "SMSG PET BROKEN (page does not exist)")|0x2AF||
|[MSG_MOVE_FEATHER_FALL](https://wowdev.wiki/index.php?title=MSG_MOVE_FEATHER_FALL&action=edit&redlink=1 "MSG MOVE FEATHER FALL (page does not exist)")|0x2B0||
|[MSG_MOVE_WATER_WALK](https://wowdev.wiki/index.php?title=MSG_MOVE_WATER_WALK&action=edit&redlink=1 "MSG MOVE WATER WALK (page does not exist)")|0x2B1||
|[CMSG_SERVER_BROADCAST](https://wowdev.wiki/index.php?title=CMSG_SERVER_BROADCAST&action=edit&redlink=1 "CMSG SERVER BROADCAST (page does not exist)")|0x2B2|not used in client|
|[CMSG_SELF_RES](https://wowdev.wiki/index.php?title=CMSG_SELF_RES&action=edit&redlink=1 "CMSG SELF RES (page does not exist)")|0x2B3||
|[SMSG_FEIGN_DEATH_RESISTED](https://wowdev.wiki/index.php?title=SMSG_FEIGN_DEATH_RESISTED&action=edit&redlink=1 "SMSG FEIGN DEATH RESISTED (page does not exist)")|0x2B4||
|[CMSG_RUN_SCRIPT](https://wowdev.wiki/index.php?title=CMSG_RUN_SCRIPT&action=edit&redlink=1 "CMSG RUN SCRIPT (page does not exist)")|0x2B5|not used in client|
|[SMSG_SCRIPT_MESSAGE](https://wowdev.wiki/index.php?title=SMSG_SCRIPT_MESSAGE&action=edit&redlink=1 "SMSG SCRIPT MESSAGE (page does not exist)")|0x2B6|not used in client|
|[SMSG_DUEL_COUNTDOWN](https://wowdev.wiki/index.php?title=SMSG_DUEL_COUNTDOWN&action=edit&redlink=1 "SMSG DUEL COUNTDOWN (page does not exist)")|0x2B7||
|[SMSG_AREA_TRIGGER_MESSAGE](https://wowdev.wiki/index.php?title=SMSG_AREA_TRIGGER_MESSAGE&action=edit&redlink=1 "SMSG AREA TRIGGER MESSAGE (page does not exist)")|0x2B8||
|[CMSG_TOGGLE_HELM](https://wowdev.wiki/index.php?title=CMSG_TOGGLE_HELM&action=edit&redlink=1 "CMSG TOGGLE HELM (page does not exist)")|0x2B9||
|[CMSG_TOGGLE_CLOAK](https://wowdev.wiki/index.php?title=CMSG_TOGGLE_CLOAK&action=edit&redlink=1 "CMSG TOGGLE CLOAK (page does not exist)")|0x2BA||
|[SMSG_MEETINGSTONE_JOINFAILED](https://wowdev.wiki/index.php?title=SMSG_MEETINGSTONE_JOINFAILED&action=edit&redlink=1 "SMSG MEETINGSTONE JOINFAILED (page does not exist)")|0x2BB||
|[SMSG_PLAYER_SKINNED](https://wowdev.wiki/index.php?title=SMSG_PLAYER_SKINNED&action=edit&redlink=1 "SMSG PLAYER SKINNED (page does not exist)")|0x2BC||
|[SMSG_DURABILITY_DAMAGE_DEATH](https://wowdev.wiki/index.php?title=SMSG_DURABILITY_DAMAGE_DEATH&action=edit&redlink=1 "SMSG DURABILITY DAMAGE DEATH (page does not exist)")|0x2BD||
|[CMSG_SET_EXPLORATION](https://wowdev.wiki/index.php?title=CMSG_SET_EXPLORATION&action=edit&redlink=1 "CMSG SET EXPLORATION (page does not exist)")|0x2BE||
|[CMSG_SET_ACTIONBAR_TOGGLES](https://wowdev.wiki/index.php?title=CMSG_SET_ACTIONBAR_TOGGLES&action=edit&redlink=1 "CMSG SET ACTIONBAR TOGGLES (page does not exist)")|0x2BF||
|[UMSG_DELETE_GUILD_CHARTER](https://wowdev.wiki/index.php?title=UMSG_DELETE_GUILD_CHARTER&action=edit&redlink=1 "UMSG DELETE GUILD CHARTER (page does not exist)")|0x2C0||
|[MSG_PETITION_RENAME](https://wowdev.wiki/index.php?title=MSG_PETITION_RENAME&action=edit&redlink=1 "MSG PETITION RENAME (page does not exist)")|0x2C1||
|[SMSG_INIT_WORLD_STATES](https://wowdev.wiki/index.php?title=SMSG_INIT_WORLD_STATES&action=edit&redlink=1 "SMSG INIT WORLD STATES (page does not exist)")|0x2C2||
|[SMSG_UPDATE_WORLD_STATE](https://wowdev.wiki/index.php?title=SMSG_UPDATE_WORLD_STATE&action=edit&redlink=1 "SMSG UPDATE WORLD STATE (page does not exist)")|0x2C3||
|[CMSG_ITEM_NAME_QUERY](https://wowdev.wiki/index.php?title=CMSG_ITEM_NAME_QUERY&action=edit&redlink=1 "CMSG ITEM NAME QUERY (page does not exist)")|0x2C4||
|[SMSG_ITEM_NAME_QUERY_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_ITEM_NAME_QUERY_RESPONSE&action=edit&redlink=1 "SMSG ITEM NAME QUERY RESPONSE (page does not exist)")|0x2C5||
|[SMSG_PET_ACTION_FEEDBACK](https://wowdev.wiki/index.php?title=SMSG_PET_ACTION_FEEDBACK&action=edit&redlink=1 "SMSG PET ACTION FEEDBACK (page does not exist)")|0x2C6||
|[CMSG_CHAR_RENAME](https://wowdev.wiki/CMSG_CHAR_RENAME "CMSG CHAR RENAME")|0x2C7||
|[SMSG_CHAR_RENAME](https://wowdev.wiki/SMSG_CHAR_RENAME "SMSG CHAR RENAME")|0x2C8||
|[CMSG_MOVE_SPLINE_DONE](https://wowdev.wiki/index.php?title=CMSG_MOVE_SPLINE_DONE&action=edit&redlink=1 "CMSG MOVE SPLINE DONE (page does not exist)")|0x2C9||
|[CMSG_MOVE_FALL_RESET](https://wowdev.wiki/index.php?title=CMSG_MOVE_FALL_RESET&action=edit&redlink=1 "CMSG MOVE FALL RESET (page does not exist)")|0x2CA||
|[SMSG_UPDATE_LAST_INSTANCE_CREATED](https://wowdev.wiki/index.php?title=SMSG_UPDATE_LAST_INSTANCE_CREATED&action=edit&redlink=1 "SMSG UPDATE LAST INSTANCE CREATED (page does not exist)")|0x2CB||
|[SMSG_RAID_INSTANCE_INFO](https://wowdev.wiki/index.php?title=SMSG_RAID_INSTANCE_INFO&action=edit&redlink=1 "SMSG RAID INSTANCE INFO (page does not exist)")|0x2CC||
|[CMSG_REQUEST_RAID_INFO](https://wowdev.wiki/index.php?title=CMSG_REQUEST_RAID_INFO&action=edit&redlink=1 "CMSG REQUEST RAID INFO (page does not exist)")|0x2CD||
|[CMSG_MOVE_TIME_SKIPPED](https://wowdev.wiki/index.php?title=CMSG_MOVE_TIME_SKIPPED&action=edit&redlink=1 "CMSG MOVE TIME SKIPPED (page does not exist)")|0x2CE||
|[CMSG_MOVE_FEATHER_FALL_ACK](https://wowdev.wiki/index.php?title=CMSG_MOVE_FEATHER_FALL_ACK&action=edit&redlink=1 "CMSG MOVE FEATHER FALL ACK (page does not exist)")|0x2CF||
|[CMSG_MOVE_WATER_WALK_ACK](https://wowdev.wiki/index.php?title=CMSG_MOVE_WATER_WALK_ACK&action=edit&redlink=1 "CMSG MOVE WATER WALK ACK (page does not exist)")|0x2D0||
|[CMSG_MOVE_NOT_ACTIVE_MOVER](https://wowdev.wiki/index.php?title=CMSG_MOVE_NOT_ACTIVE_MOVER&action=edit&redlink=1 "CMSG MOVE NOT ACTIVE MOVER (page does not exist)")|0x2D1||
|[SMSG_PLAY_SOUND](https://wowdev.wiki/index.php?title=SMSG_PLAY_SOUND&action=edit&redlink=1 "SMSG PLAY SOUND (page does not exist)")|0x2D2||
|[CMSG_BATTLEFIELD_STATUS](https://wowdev.wiki/index.php?title=CMSG_BATTLEFIELD_STATUS&action=edit&redlink=1 "CMSG BATTLEFIELD STATUS (page does not exist)")|0x2D3||
|[SMSG_BATTLEFIELD_STATUS](https://wowdev.wiki/index.php?title=SMSG_BATTLEFIELD_STATUS&action=edit&redlink=1 "SMSG BATTLEFIELD STATUS (page does not exist)")|0x2D4||
|[CMSG_BATTLEFIELD_PORT](https://wowdev.wiki/index.php?title=CMSG_BATTLEFIELD_PORT&action=edit&redlink=1 "CMSG BATTLEFIELD PORT (page does not exist)")|0x2D5||
|[MSG_INSPECT_HONOR_STATS](https://wowdev.wiki/index.php?title=MSG_INSPECT_HONOR_STATS&action=edit&redlink=1 "MSG INSPECT HONOR STATS (page does not exist)")|0x2D6||
|[CMSG_BATTLEMASTER_HELLO](https://wowdev.wiki/index.php?title=CMSG_BATTLEMASTER_HELLO&action=edit&redlink=1 "CMSG BATTLEMASTER HELLO (page does not exist)")|0x2D7||
|[CMSG_MOVE_START_SWIM_CHEAT](https://wowdev.wiki/index.php?title=CMSG_MOVE_START_SWIM_CHEAT&action=edit&redlink=1 "CMSG MOVE START SWIM CHEAT (page does not exist)")|0x2D8|not used in client|
|[CMSG_MOVE_STOP_SWIM_CHEAT](https://wowdev.wiki/index.php?title=CMSG_MOVE_STOP_SWIM_CHEAT&action=edit&redlink=1 "CMSG MOVE STOP SWIM CHEAT (page does not exist)")|0x2D9|not used in client|
|[SMSG_FORCE_WALK_SPEED_CHANGE](https://wowdev.wiki/index.php?title=SMSG_FORCE_WALK_SPEED_CHANGE&action=edit&redlink=1 "SMSG FORCE WALK SPEED CHANGE (page does not exist)")|0x2DA||
|[CMSG_FORCE_WALK_SPEED_CHANGE_ACK](https://wowdev.wiki/index.php?title=CMSG_FORCE_WALK_SPEED_CHANGE_ACK&action=edit&redlink=1 "CMSG FORCE WALK SPEED CHANGE ACK (page does not exist)")|0x2DB||
|[SMSG_FORCE_SWIM_BACK_SPEED_CHANGE](https://wowdev.wiki/index.php?title=SMSG_FORCE_SWIM_BACK_SPEED_CHANGE&action=edit&redlink=1 "SMSG FORCE SWIM BACK SPEED CHANGE (page does not exist)")|0x2DC||
|[CMSG_FORCE_SWIM_BACK_SPEED_CHANGE_ACK](https://wowdev.wiki/index.php?title=CMSG_FORCE_SWIM_BACK_SPEED_CHANGE_ACK&action=edit&redlink=1 "CMSG FORCE SWIM BACK SPEED CHANGE ACK (page does not exist)")|0x2DD||
|[SMSG_FORCE_TURN_RATE_CHANGE](https://wowdev.wiki/index.php?title=SMSG_FORCE_TURN_RATE_CHANGE&action=edit&redlink=1 "SMSG FORCE TURN RATE CHANGE (page does not exist)")|0x2DE||
|[CMSG_FORCE_TURN_RATE_CHANGE_ACK](https://wowdev.wiki/index.php?title=CMSG_FORCE_TURN_RATE_CHANGE_ACK&action=edit&redlink=1 "CMSG FORCE TURN RATE CHANGE ACK (page does not exist)")|0x2DF||
|[MSG_PVP_LOG_DATA](https://wowdev.wiki/index.php?title=MSG_PVP_LOG_DATA&action=edit&redlink=1 "MSG PVP LOG DATA (page does not exist)")|0x2E0||
|[CMSG_LEAVE_BATTLEFIELD](https://wowdev.wiki/index.php?title=CMSG_LEAVE_BATTLEFIELD&action=edit&redlink=1 "CMSG LEAVE BATTLEFIELD (page does not exist)")|0x2E1||
|[CMSG_AREA_SPIRIT_HEALER_QUERY](https://wowdev.wiki/index.php?title=CMSG_AREA_SPIRIT_HEALER_QUERY&action=edit&redlink=1 "CMSG AREA SPIRIT HEALER QUERY (page does not exist)")|0x2E2||
|[CMSG_AREA_SPIRIT_HEALER_QUEUE](https://wowdev.wiki/index.php?title=CMSG_AREA_SPIRIT_HEALER_QUEUE&action=edit&redlink=1 "CMSG AREA SPIRIT HEALER QUEUE (page does not exist)")|0x2E3||
|[SMSG_AREA_SPIRIT_HEALER_TIME](https://wowdev.wiki/index.php?title=SMSG_AREA_SPIRIT_HEALER_TIME&action=edit&redlink=1 "SMSG AREA SPIRIT HEALER TIME (page does not exist)")|0x2E4||
|[CMSG_GM_UNTEACH](https://wowdev.wiki/index.php?title=CMSG_GM_UNTEACH&action=edit&redlink=1 "CMSG GM UNTEACH (page does not exist)")|0x2E5|not used in client|
|[SMSG_WARDEN_DATA](https://wowdev.wiki/index.php?title=SMSG_WARDEN_DATA&action=edit&redlink=1 "SMSG WARDEN DATA (page does not exist)")|0x2E6||
|[CMSG_WARDEN_DATA](https://wowdev.wiki/index.php?title=CMSG_WARDEN_DATA&action=edit&redlink=1 "CMSG WARDEN DATA (page does not exist)")|0x2E7||
|[SMSG_GROUP_JOINED_BATTLEGROUND](https://wowdev.wiki/index.php?title=SMSG_GROUP_JOINED_BATTLEGROUND&action=edit&redlink=1 "SMSG GROUP JOINED BATTLEGROUND (page does not exist)")|0x2E8||
|[MSG_BATTLEGROUND_PLAYER_POSITIONS](https://wowdev.wiki/index.php?title=MSG_BATTLEGROUND_PLAYER_POSITIONS&action=edit&redlink=1 "MSG BATTLEGROUND PLAYER POSITIONS (page does not exist)")|0x2E9||
|[CMSG_PET_STOP_ATTACK](https://wowdev.wiki/index.php?title=CMSG_PET_STOP_ATTACK&action=edit&redlink=1 "CMSG PET STOP ATTACK (page does not exist)")|0x2EA||
|[SMSG_BINDER_CONFIRM](https://wowdev.wiki/index.php?title=SMSG_BINDER_CONFIRM&action=edit&redlink=1 "SMSG BINDER CONFIRM (page does not exist)")|0x2EB||
|[SMSG_BATTLEGROUND_PLAYER_JOINED](https://wowdev.wiki/index.php?title=SMSG_BATTLEGROUND_PLAYER_JOINED&action=edit&redlink=1 "SMSG BATTLEGROUND PLAYER JOINED (page does not exist)")|0x2EC||
|[SMSG_BATTLEGROUND_PLAYER_LEFT](https://wowdev.wiki/index.php?title=SMSG_BATTLEGROUND_PLAYER_LEFT&action=edit&redlink=1 "SMSG BATTLEGROUND PLAYER LEFT (page does not exist)")|0x2ED||
|[CMSG_BATTLEMASTER_JOIN](https://wowdev.wiki/index.php?title=CMSG_BATTLEMASTER_JOIN&action=edit&redlink=1 "CMSG BATTLEMASTER JOIN (page does not exist)")|0x2EE||
|[SMSG_ADDON_INFO](https://wowdev.wiki/index.php?title=SMSG_ADDON_INFO&action=edit&redlink=1 "SMSG ADDON INFO (page does not exist)")|0x2EF||
|[CMSG_PET_UNLEARN](https://wowdev.wiki/index.php?title=CMSG_PET_UNLEARN&action=edit&redlink=1 "CMSG PET UNLEARN (page does not exist)")|0x2F0||
|[SMSG_PET_UNLEARN_CONFIRM](https://wowdev.wiki/index.php?title=SMSG_PET_UNLEARN_CONFIRM&action=edit&redlink=1 "SMSG PET UNLEARN CONFIRM (page does not exist)")|0x2F1||
|[SMSG_PARTY_MEMBER_STATS_FULL](https://wowdev.wiki/index.php?title=SMSG_PARTY_MEMBER_STATS_FULL&action=edit&redlink=1 "SMSG PARTY MEMBER STATS FULL (page does not exist)")|0x2F2||
|[CMSG_PET_SPELL_AUTOCAST](https://wowdev.wiki/index.php?title=CMSG_PET_SPELL_AUTOCAST&action=edit&redlink=1 "CMSG PET SPELL AUTOCAST (page does not exist)")|0x2F3||
|[SMSG_WEATHER](https://wowdev.wiki/index.php?title=SMSG_WEATHER&action=edit&redlink=1 "SMSG WEATHER (page does not exist)")|0x2F4||
|[SMSG_PLAY_TIME_WARNING](https://wowdev.wiki/index.php?title=SMSG_PLAY_TIME_WARNING&action=edit&redlink=1 "SMSG PLAY TIME WARNING (page does not exist)")|0x2F5||
|[SMSG_MINIGAME_SETUP](https://wowdev.wiki/index.php?title=SMSG_MINIGAME_SETUP&action=edit&redlink=1 "SMSG MINIGAME SETUP (page does not exist)")|0x2F6||
|[SMSG_MINIGAME_STATE](https://wowdev.wiki/index.php?title=SMSG_MINIGAME_STATE&action=edit&redlink=1 "SMSG MINIGAME STATE (page does not exist)")|0x2F7||
|[CMSG_MINIGAME_MOVE](https://wowdev.wiki/index.php?title=CMSG_MINIGAME_MOVE&action=edit&redlink=1 "CMSG MINIGAME MOVE (page does not exist)")|0x2F8||
|[SMSG_MINIGAME_MOVE_FAILED](https://wowdev.wiki/index.php?title=SMSG_MINIGAME_MOVE_FAILED&action=edit&redlink=1 "SMSG MINIGAME MOVE FAILED (page does not exist)")|0x2F9|not used in client|
|[SMSG_RAID_INSTANCE_MESSAGE](https://wowdev.wiki/index.php?title=SMSG_RAID_INSTANCE_MESSAGE&action=edit&redlink=1 "SMSG RAID INSTANCE MESSAGE (page does not exist)")|0x2FA||
|[SMSG_COMPRESSED_MOVES](https://wowdev.wiki/index.php?title=SMSG_COMPRESSED_MOVES&action=edit&redlink=1 "SMSG COMPRESSED MOVES (page does not exist)")|0x2FB||
|[CMSG_GUILD_INFO_TEXT](https://wowdev.wiki/index.php?title=CMSG_GUILD_INFO_TEXT&action=edit&redlink=1 "CMSG GUILD INFO TEXT (page does not exist)")|0x2FC||
|[SMSG_CHAT_RESTRICTED](https://wowdev.wiki/index.php?title=SMSG_CHAT_RESTRICTED&action=edit&redlink=1 "SMSG CHAT RESTRICTED (page does not exist)")|0x2FD||
|[SMSG_SPLINE_SET_RUN_SPEED](https://wowdev.wiki/index.php?title=SMSG_SPLINE_SET_RUN_SPEED&action=edit&redlink=1 "SMSG SPLINE SET RUN SPEED (page does not exist)")|0x2FE||
|[SMSG_SPLINE_SET_RUN_BACK_SPEED](https://wowdev.wiki/index.php?title=SMSG_SPLINE_SET_RUN_BACK_SPEED&action=edit&redlink=1 "SMSG SPLINE SET RUN BACK SPEED (page does not exist)")|0x2FF||
|[SMSG_SPLINE_SET_SWIM_SPEED](https://wowdev.wiki/index.php?title=SMSG_SPLINE_SET_SWIM_SPEED&action=edit&redlink=1 "SMSG SPLINE SET SWIM SPEED (page does not exist)")|0x300||
|[SMSG_SPLINE_SET_WALK_SPEED](https://wowdev.wiki/index.php?title=SMSG_SPLINE_SET_WALK_SPEED&action=edit&redlink=1 "SMSG SPLINE SET WALK SPEED (page does not exist)")|0x301||
|[SMSG_SPLINE_SET_SWIM_BACK_SPEED](https://wowdev.wiki/index.php?title=SMSG_SPLINE_SET_SWIM_BACK_SPEED&action=edit&redlink=1 "SMSG SPLINE SET SWIM BACK SPEED (page does not exist)")|0x302||
|[SMSG_SPLINE_SET_TURN_RATE](https://wowdev.wiki/index.php?title=SMSG_SPLINE_SET_TURN_RATE&action=edit&redlink=1 "SMSG SPLINE SET TURN RATE (page does not exist)")|0x303||
|[SMSG_SPLINE_MOVE_UNROOT](https://wowdev.wiki/index.php?title=SMSG_SPLINE_MOVE_UNROOT&action=edit&redlink=1 "SMSG SPLINE MOVE UNROOT (page does not exist)")|0x304||
|[SMSG_SPLINE_MOVE_FEATHER_FALL](https://wowdev.wiki/index.php?title=SMSG_SPLINE_MOVE_FEATHER_FALL&action=edit&redlink=1 "SMSG SPLINE MOVE FEATHER FALL (page does not exist)")|0x305||
|[SMSG_SPLINE_MOVE_NORMAL_FALL](https://wowdev.wiki/index.php?title=SMSG_SPLINE_MOVE_NORMAL_FALL&action=edit&redlink=1 "SMSG SPLINE MOVE NORMAL FALL (page does not exist)")|0x306||
|[SMSG_SPLINE_MOVE_SET_HOVER](https://wowdev.wiki/index.php?title=SMSG_SPLINE_MOVE_SET_HOVER&action=edit&redlink=1 "SMSG SPLINE MOVE SET HOVER (page does not exist)")|0x307||
|[SMSG_SPLINE_MOVE_UNSET_HOVER](https://wowdev.wiki/index.php?title=SMSG_SPLINE_MOVE_UNSET_HOVER&action=edit&redlink=1 "SMSG SPLINE MOVE UNSET HOVER (page does not exist)")|0x308||
|[SMSG_SPLINE_MOVE_WATER_WALK](https://wowdev.wiki/index.php?title=SMSG_SPLINE_MOVE_WATER_WALK&action=edit&redlink=1 "SMSG SPLINE MOVE WATER WALK (page does not exist)")|0x309||
|[SMSG_SPLINE_MOVE_LAND_WALK](https://wowdev.wiki/index.php?title=SMSG_SPLINE_MOVE_LAND_WALK&action=edit&redlink=1 "SMSG SPLINE MOVE LAND WALK (page does not exist)")|0x30A||
|[SMSG_SPLINE_MOVE_START_SWIM](https://wowdev.wiki/index.php?title=SMSG_SPLINE_MOVE_START_SWIM&action=edit&redlink=1 "SMSG SPLINE MOVE START SWIM (page does not exist)")\||0x30B||
|[SMSG_SPLINE_MOVE_STOP_SWIM](https://wowdev.wiki/index.php?title=SMSG_SPLINE_MOVE_STOP_SWIM&action=edit&redlink=1 "SMSG SPLINE MOVE STOP SWIM (page does not exist)")|0x30C||
|[SMSG_SPLINE_MOVE_SET_RUN_MODE](https://wowdev.wiki/index.php?title=SMSG_SPLINE_MOVE_SET_RUN_MODE&action=edit&redlink=1 "SMSG SPLINE MOVE SET RUN MODE (page does not exist)")|0x30D||
|[SMSG_SPLINE_MOVE_SET_WALK_MODE](https://wowdev.wiki/index.php?title=SMSG_SPLINE_MOVE_SET_WALK_MODE&action=edit&redlink=1 "SMSG SPLINE MOVE SET WALK MODE (page does not exist)")|0x30E||
|[CMSG_GM_NUKE_ACCOUNT](https://wowdev.wiki/index.php?title=CMSG_GM_NUKE_ACCOUNT&action=edit&redlink=1 "CMSG GM NUKE ACCOUNT (page does not exist)")|0x30F||
|[MSG_GM_DESTROY_CORPSE](https://wowdev.wiki/index.php?title=MSG_GM_DESTROY_CORPSE&action=edit&redlink=1 "MSG GM DESTROY CORPSE (page does not exist)")|0x310||
|[CMSG_GM_DESTROY_ONLINE_CORPSE](https://wowdev.wiki/index.php?title=CMSG_GM_DESTROY_ONLINE_CORPSE&action=edit&redlink=1 "CMSG GM DESTROY ONLINE CORPSE (page does not exist)")|0x311||
|[CMSG_ACTIVATETAXIEXPRESS](https://wowdev.wiki/index.php?title=CMSG_ACTIVATETAXIEXPRESS&action=edit&redlink=1 "CMSG ACTIVATETAXIEXPRESS (page does not exist)")|0x312||
|[SMSG_SET_FACTION_ATWAR](https://wowdev.wiki/index.php?title=SMSG_SET_FACTION_ATWAR&action=edit&redlink=1 "SMSG SET FACTION ATWAR (page does not exist)")|0x313||
|[SMSG_GAMETIMEBIAS_SET](https://wowdev.wiki/index.php?title=SMSG_GAMETIMEBIAS_SET&action=edit&redlink=1 "SMSG GAMETIMEBIAS SET (page does not exist)")|0x314|not used in client|
|[CMSG_DEBUG_ACTIONS_START](https://wowdev.wiki/index.php?title=CMSG_DEBUG_ACTIONS_START&action=edit&redlink=1 "CMSG DEBUG ACTIONS START (page does not exist)")|0x315||
|[CMSG_DEBUG_ACTIONS_STOP](https://wowdev.wiki/index.php?title=CMSG_DEBUG_ACTIONS_STOP&action=edit&redlink=1 "CMSG DEBUG ACTIONS STOP (page does not exist)")|0x316||
|[CMSG_SET_FACTION_INACTIVE](https://wowdev.wiki/index.php?title=CMSG_SET_FACTION_INACTIVE&action=edit&redlink=1 "CMSG SET FACTION INACTIVE (page does not exist)")|0x317||
|[CMSG_SET_WATCHED_FACTION](https://wowdev.wiki/index.php?title=CMSG_SET_WATCHED_FACTION&action=edit&redlink=1 "CMSG SET WATCHED FACTION (page does not exist)")|0x318||
|[MSG_MOVE_TIME_SKIPPED](https://wowdev.wiki/index.php?title=MSG_MOVE_TIME_SKIPPED&action=edit&redlink=1 "MSG MOVE TIME SKIPPED (page does not exist)")|0x319||
|[SMSG_SPLINE_MOVE_ROOT](https://wowdev.wiki/index.php?title=SMSG_SPLINE_MOVE_ROOT&action=edit&redlink=1 "SMSG SPLINE MOVE ROOT (page does not exist)")|0x31A||
|[CMSG_SET_EXPLORATION_ALL](https://wowdev.wiki/index.php?title=CMSG_SET_EXPLORATION_ALL&action=edit&redlink=1 "CMSG SET EXPLORATION ALL (page does not exist)")|0x31B||
|[SMSG_INVALIDATE_PLAYER](https://wowdev.wiki/index.php?title=SMSG_INVALIDATE_PLAYER&action=edit&redlink=1 "SMSG INVALIDATE PLAYER (page does not exist)")|0x31C||
|[CMSG_RESET_INSTANCE](https://wowdev.wiki/index.php?title=CMSG_RESET_INSTANCE&action=edit&redlink=1 "CMSG RESET INSTANCE (page does not exist)")|0x31D||
|[SMSG_INSTANCE_RESET](https://wowdev.wiki/index.php?title=SMSG_INSTANCE_RESET&action=edit&redlink=1 "SMSG INSTANCE RESET (page does not exist)")|0x31E||
|[SMSG_INSTANCE_RESET_FAILED](https://wowdev.wiki/index.php?title=SMSG_INSTANCE_RESET_FAILED&action=edit&redlink=1 "SMSG INSTANCE RESET FAILED (page does not exist)")|0x31F||
|[SMSG_UPDATE_LAST_INSTANCE](https://wowdev.wiki/index.php?title=SMSG_UPDATE_LAST_INSTANCE&action=edit&redlink=1 "SMSG UPDATE LAST INSTANCE (page does not exist)")|0x320||
|[MSG_RAID_TARGET_UPDATE](https://wowdev.wiki/index.php?title=MSG_RAID_TARGET_UPDATE&action=edit&redlink=1 "MSG RAID TARGET UPDATE (page does not exist)")|0x321||
|[MSG_RAID_READY_CHECK](https://wowdev.wiki/index.php?title=MSG_RAID_READY_CHECK&action=edit&redlink=1 "MSG RAID READY CHECK (page does not exist)")|0x322||
|[CMSG_LUA_USAGE](https://wowdev.wiki/index.php?title=CMSG_LUA_USAGE&action=edit&redlink=1 "CMSG LUA USAGE (page does not exist)")|0x323|not used in client|
|[SMSG_PET_ACTION_SOUND](https://wowdev.wiki/index.php?title=SMSG_PET_ACTION_SOUND&action=edit&redlink=1 "SMSG PET ACTION SOUND (page does not exist)")|0x324||
|[SMSG_PET_DISMISS_SOUND](https://wowdev.wiki/index.php?title=SMSG_PET_DISMISS_SOUND&action=edit&redlink=1 "SMSG PET DISMISS SOUND (page does not exist)")|0x325||
|[SMSG_GHOSTEE_GONE](https://wowdev.wiki/index.php?title=SMSG_GHOSTEE_GONE&action=edit&redlink=1 "SMSG GHOSTEE GONE (page does not exist)")|0x326||
|[CMSG_GM_UPDATE_TICKET_STATUS](https://wowdev.wiki/index.php?title=CMSG_GM_UPDATE_TICKET_STATUS&action=edit&redlink=1 "CMSG GM UPDATE TICKET STATUS (page does not exist)")|0x327||
|[SMSG_GM_TICKET_STATUS_UPDATE](https://wowdev.wiki/index.php?title=SMSG_GM_TICKET_STATUS_UPDATE&action=edit&redlink=1 "SMSG GM TICKET STATUS UPDATE (page does not exist)")|0x328||
|[MSG_SET_DUNGEON_DIFFICULTY](https://wowdev.wiki/index.php?title=MSG_SET_DUNGEON_DIFFICULTY&action=edit&redlink=1 "MSG SET DUNGEON DIFFICULTY (page does not exist)")|0x329||
|[CMSG_GMSURVEY_SUBMIT](https://wowdev.wiki/index.php?title=CMSG_GMSURVEY_SUBMIT&action=edit&redlink=1 "CMSG GMSURVEY SUBMIT (page does not exist)")|0x32A||
|[SMSG_UPDATE_INSTANCE_OWNERSHIP](https://wowdev.wiki/index.php?title=SMSG_UPDATE_INSTANCE_OWNERSHIP&action=edit&redlink=1 "SMSG UPDATE INSTANCE OWNERSHIP (page does not exist)")|0x32B||
|[CMSG_IGNORE_KNOCKBACK_CHEAT](https://wowdev.wiki/index.php?title=CMSG_IGNORE_KNOCKBACK_CHEAT&action=edit&redlink=1 "CMSG IGNORE KNOCKBACK CHEAT (page does not exist)")|0x32C||
|[SMSG_CHAT_PLAYER_AMBIGUOUS](https://wowdev.wiki/index.php?title=SMSG_CHAT_PLAYER_AMBIGUOUS&action=edit&redlink=1 "SMSG CHAT PLAYER AMBIGUOUS (page does not exist)")|0x32D|not used in client|
|[MSG_DELAY_GHOST_TELEPORT](https://wowdev.wiki/index.php?title=MSG_DELAY_GHOST_TELEPORT&action=edit&redlink=1 "MSG DELAY GHOST TELEPORT (page does not exist)")|0x32E|not used in client|
|[SMSG_SPELLINSTAKILLLOG](https://wowdev.wiki/index.php?title=SMSG_SPELLINSTAKILLLOG&action=edit&redlink=1 "SMSG SPELLINSTAKILLLOG (page does not exist)")|0x32F||
|[SMSG_SPELL_UPDATE_CHAIN_TARGETS](https://wowdev.wiki/index.php?title=SMSG_SPELL_UPDATE_CHAIN_TARGETS&action=edit&redlink=1 "SMSG SPELL UPDATE CHAIN TARGETS (page does not exist)")|0x330||
|[CMSG_CHAT_FILTERED](https://wowdev.wiki/index.php?title=CMSG_CHAT_FILTERED&action=edit&redlink=1 "CMSG CHAT FILTERED (page does not exist)")|0x331||
|[SMSG_EXPECTED_SPAM_RECORDS](https://wowdev.wiki/index.php?title=SMSG_EXPECTED_SPAM_RECORDS&action=edit&redlink=1 "SMSG EXPECTED SPAM RECORDS (page does not exist)")|0x332||
|[SMSG_SPELLSTEALLOG](https://wowdev.wiki/index.php?title=SMSG_SPELLSTEALLOG&action=edit&redlink=1 "SMSG SPELLSTEALLOG (page does not exist)")|0x333||
|[CMSG_LOTTERY_QUERY_OBSOLETE](https://wowdev.wiki/index.php?title=CMSG_LOTTERY_QUERY_OBSOLETE&action=edit&redlink=1 "CMSG LOTTERY QUERY OBSOLETE (page does not exist)")|0x334|not used in client|
|[SMSG_LOTTERY_QUERY_RESULT_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_LOTTERY_QUERY_RESULT_OBSOLETE&action=edit&redlink=1 "SMSG LOTTERY QUERY RESULT OBSOLETE (page does not exist)")|0x335|not used in client|
|[CMSG_BUY_LOTTERY_TICKET_OBSOLETE](https://wowdev.wiki/index.php?title=CMSG_BUY_LOTTERY_TICKET_OBSOLETE&action=edit&redlink=1 "CMSG BUY LOTTERY TICKET OBSOLETE (page does not exist)")|0x336|not used in client|
|[SMSG_LOTTERY_RESULT_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_LOTTERY_RESULT_OBSOLETE&action=edit&redlink=1 "SMSG LOTTERY RESULT OBSOLETE (page does not exist)")|0x337|not used in client|
|[SMSG_CHARACTER_PROFILE](https://wowdev.wiki/index.php?title=SMSG_CHARACTER_PROFILE&action=edit&redlink=1 "SMSG CHARACTER PROFILE (page does not exist)")|0x338|not used in client|
|[SMSG_CHARACTER_PROFILE_REALM_CONNECTED](https://wowdev.wiki/index.php?title=SMSG_CHARACTER_PROFILE_REALM_CONNECTED&action=edit&redlink=1 "SMSG CHARACTER PROFILE REALM CONNECTED (page does not exist)")|0x339|not used in client|
|[SMSG_DEFENSE_MESSAGE](https://wowdev.wiki/index.php?title=SMSG_DEFENSE_MESSAGE&action=edit&redlink=1 "SMSG DEFENSE MESSAGE (page does not exist)")|0x33A||
|[SMSG_INSTANCE_DIFFICULTY](https://wowdev.wiki/index.php?title=SMSG_INSTANCE_DIFFICULTY&action=edit&redlink=1 "SMSG INSTANCE DIFFICULTY (page does not exist)")|0x33B||
|[MSG_GM_RESETINSTANCELIMIT](https://wowdev.wiki/index.php?title=MSG_GM_RESETINSTANCELIMIT&action=edit&redlink=1 "MSG GM RESETINSTANCELIMIT (page does not exist)")|0x33C|not used in client|
|[SMSG_MOTD](https://wowdev.wiki/index.php?title=SMSG_MOTD&action=edit&redlink=1 "SMSG MOTD (page does not exist)")|0x33D||
|[SMSG_MOVE_SET_FLIGHT_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_MOVE_SET_FLIGHT_OBSOLETE&action=edit&redlink=1 "SMSG MOVE SET FLIGHT OBSOLETE (page does not exist)")|0x33E|not used in client|
|[SMSG_MOVE_UNSET_FLIGHT_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_MOVE_UNSET_FLIGHT_OBSOLETE&action=edit&redlink=1 "SMSG MOVE UNSET FLIGHT OBSOLETE (page does not exist)")|0x33F|not used in client|
|[CMSG_MOVE_FLIGHT_ACK_OBSOLETE](https://wowdev.wiki/index.php?title=CMSG_MOVE_FLIGHT_ACK_OBSOLETE&action=edit&redlink=1 "CMSG MOVE FLIGHT ACK OBSOLETE (page does not exist)")|0x340|not used in client|
|[MSG_MOVE_START_SWIM_CHEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_START_SWIM_CHEAT&action=edit&redlink=1 "MSG MOVE START SWIM CHEAT (page does not exist)")|0x341||
|[MSG_MOVE_STOP_SWIM_CHEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_STOP_SWIM_CHEAT&action=edit&redlink=1 "MSG MOVE STOP SWIM CHEAT (page does not exist)")|0x342||
|[SMSG_MOVE_SET_CAN_FLY](https://wowdev.wiki/index.php?title=SMSG_MOVE_SET_CAN_FLY&action=edit&redlink=1 "SMSG MOVE SET CAN FLY (page does not exist)")|0x343||
|[SMSG_MOVE_UNSET_CAN_FLY](https://wowdev.wiki/index.php?title=SMSG_MOVE_UNSET_CAN_FLY&action=edit&redlink=1 "SMSG MOVE UNSET CAN FLY (page does not exist)")|0x344||
|[CMSG_MOVE_SET_CAN_FLY_ACK](https://wowdev.wiki/index.php?title=CMSG_MOVE_SET_CAN_FLY_ACK&action=edit&redlink=1 "CMSG MOVE SET CAN FLY ACK (page does not exist)")|0x345||
|[CMSG_MOVE_SET_FLY](https://wowdev.wiki/index.php?title=CMSG_MOVE_SET_FLY&action=edit&redlink=1 "CMSG MOVE SET FLY (page does not exist)")|0x346||
|[CMSG_SOCKET_GEMS](https://wowdev.wiki/index.php?title=CMSG_SOCKET_GEMS&action=edit&redlink=1 "CMSG SOCKET GEMS (page does not exist)")|0x347||
|[CMSG_ARENA_TEAM_CREATE](https://wowdev.wiki/index.php?title=CMSG_ARENA_TEAM_CREATE&action=edit&redlink=1 "CMSG ARENA TEAM CREATE (page does not exist)")|0x348||
|[SMSG_ARENA_TEAM_COMMAND_RESULT](https://wowdev.wiki/index.php?title=SMSG_ARENA_TEAM_COMMAND_RESULT&action=edit&redlink=1 "SMSG ARENA TEAM COMMAND RESULT (page does not exist)")|0x349||
|[UMSG_UPDATE_ARENA_TEAM_OBSOLETE](https://wowdev.wiki/index.php?title=UMSG_UPDATE_ARENA_TEAM_OBSOLETE&action=edit&redlink=1 "UMSG UPDATE ARENA TEAM OBSOLETE (page does not exist)")|0x34A||
|[CMSG_ARENA_TEAM_QUERY](https://wowdev.wiki/index.php?title=CMSG_ARENA_TEAM_QUERY&action=edit&redlink=1 "CMSG ARENA TEAM QUERY (page does not exist)")|0x34B||
|[SMSG_ARENA_TEAM_QUERY_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_ARENA_TEAM_QUERY_RESPONSE&action=edit&redlink=1 "SMSG ARENA TEAM QUERY RESPONSE (page does not exist)")|0x34C||
|[CMSG_ARENA_TEAM_ROSTER](https://wowdev.wiki/index.php?title=CMSG_ARENA_TEAM_ROSTER&action=edit&redlink=1 "CMSG ARENA TEAM ROSTER (page does not exist)")|0x34D||
|[SMSG_ARENA_TEAM_ROSTER](https://wowdev.wiki/index.php?title=SMSG_ARENA_TEAM_ROSTER&action=edit&redlink=1 "SMSG ARENA TEAM ROSTER (page does not exist)")|0x34E||
|[CMSG_ARENA_TEAM_INVITE](https://wowdev.wiki/index.php?title=CMSG_ARENA_TEAM_INVITE&action=edit&redlink=1 "CMSG ARENA TEAM INVITE (page does not exist)")|0x34F||
|[SMSG_ARENA_TEAM_INVITE](https://wowdev.wiki/index.php?title=SMSG_ARENA_TEAM_INVITE&action=edit&redlink=1 "SMSG ARENA TEAM INVITE (page does not exist)")|0x350||
|[CMSG_ARENA_TEAM_ACCEPT](https://wowdev.wiki/index.php?title=CMSG_ARENA_TEAM_ACCEPT&action=edit&redlink=1 "CMSG ARENA TEAM ACCEPT (page does not exist)")|0x351||
|[CMSG_ARENA_TEAM_DECLINE](https://wowdev.wiki/index.php?title=CMSG_ARENA_TEAM_DECLINE&action=edit&redlink=1 "CMSG ARENA TEAM DECLINE (page does not exist)")|0x352||
|[CMSG_ARENA_TEAM_LEAVE](https://wowdev.wiki/index.php?title=CMSG_ARENA_TEAM_LEAVE&action=edit&redlink=1 "CMSG ARENA TEAM LEAVE (page does not exist)")|0x353||
|[CMSG_ARENA_TEAM_REMOVE](https://wowdev.wiki/index.php?title=CMSG_ARENA_TEAM_REMOVE&action=edit&redlink=1 "CMSG ARENA TEAM REMOVE (page does not exist)")|0x354||
|[CMSG_ARENA_TEAM_DISBAND](https://wowdev.wiki/index.php?title=CMSG_ARENA_TEAM_DISBAND&action=edit&redlink=1 "CMSG ARENA TEAM DISBAND (page does not exist)")|0x355||
|[CMSG_ARENA_TEAM_LEADER](https://wowdev.wiki/index.php?title=CMSG_ARENA_TEAM_LEADER&action=edit&redlink=1 "CMSG ARENA TEAM LEADER (page does not exist)")|0x356||
|[SMSG_ARENA_TEAM_EVENT](https://wowdev.wiki/index.php?title=SMSG_ARENA_TEAM_EVENT&action=edit&redlink=1 "SMSG ARENA TEAM EVENT (page does not exist)")|0x357||
|[CMSG_BATTLEMASTER_JOIN_ARENA](https://wowdev.wiki/index.php?title=CMSG_BATTLEMASTER_JOIN_ARENA&action=edit&redlink=1 "CMSG BATTLEMASTER JOIN ARENA (page does not exist)")|0x358||
|[MSG_MOVE_START_ASCEND](https://wowdev.wiki/index.php?title=MSG_MOVE_START_ASCEND&action=edit&redlink=1 "MSG MOVE START ASCEND (page does not exist)")|0x359||
|[MSG_MOVE_STOP_ASCEND](https://wowdev.wiki/index.php?title=MSG_MOVE_STOP_ASCEND&action=edit&redlink=1 "MSG MOVE STOP ASCEND (page does not exist)")|0x35A||
|[SMSG_ARENA_TEAM_STATS](https://wowdev.wiki/index.php?title=SMSG_ARENA_TEAM_STATS&action=edit&redlink=1 "SMSG ARENA TEAM STATS (page does not exist)")|0x35B||
|[CMSG_LFG_SET_AUTOJOIN](https://wowdev.wiki/index.php?title=CMSG_LFG_SET_AUTOJOIN&action=edit&redlink=1 "CMSG LFG SET AUTOJOIN (page does not exist)")|0x35C||
|[CMSG_LFG_CLEAR_AUTOJOIN](https://wowdev.wiki/index.php?title=CMSG_LFG_CLEAR_AUTOJOIN&action=edit&redlink=1 "CMSG LFG CLEAR AUTOJOIN (page does not exist)")|0x35D||
|[CMSG_LFM_SET_AUTOFILL](https://wowdev.wiki/index.php?title=CMSG_LFM_SET_AUTOFILL&action=edit&redlink=1 "CMSG LFM SET AUTOFILL (page does not exist)")|0x35E||
|[CMSG_LFM_CLEAR_AUTOFILL](https://wowdev.wiki/index.php?title=CMSG_LFM_CLEAR_AUTOFILL&action=edit&redlink=1 "CMSG LFM CLEAR AUTOFILL (page does not exist)")|0x35F||
|[CMSG_ACCEPT_LFG_MATCH](https://wowdev.wiki/index.php?title=CMSG_ACCEPT_LFG_MATCH&action=edit&redlink=1 "CMSG ACCEPT LFG MATCH (page does not exist)")|0x360||
|[CMSG_DECLINE_LFG_MATCH](https://wowdev.wiki/index.php?title=CMSG_DECLINE_LFG_MATCH&action=edit&redlink=1 "CMSG DECLINE LFG MATCH (page does not exist)")|0x361||
|[CMSG_CANCEL_PENDING_LFG](https://wowdev.wiki/index.php?title=CMSG_CANCEL_PENDING_LFG&action=edit&redlink=1 "CMSG CANCEL PENDING LFG (page does not exist)")|0x362||
|[CMSG_CLEAR_LOOKING_FOR_GROUP](https://wowdev.wiki/index.php?title=CMSG_CLEAR_LOOKING_FOR_GROUP&action=edit&redlink=1 "CMSG CLEAR LOOKING FOR GROUP (page does not exist)")|0x363||
|[CMSG_CLEAR_LOOKING_FOR_MORE](https://wowdev.wiki/index.php?title=CMSG_CLEAR_LOOKING_FOR_MORE&action=edit&redlink=1 "CMSG CLEAR LOOKING FOR MORE (page does not exist)")|0x364||
|[CMSG_SET_LOOKING_FOR_MORE](https://wowdev.wiki/index.php?title=CMSG_SET_LOOKING_FOR_MORE&action=edit&redlink=1 "CMSG SET LOOKING FOR MORE (page does not exist)")|0x365||
|[CMSG_SET_LFG_COMMENT](https://wowdev.wiki/index.php?title=CMSG_SET_LFG_COMMENT&action=edit&redlink=1 "CMSG SET LFG COMMENT (page does not exist)")|0x366||
|[SMSG_LFG_TIMEDOUT](https://wowdev.wiki/index.php?title=SMSG_LFG_TIMEDOUT&action=edit&redlink=1 "SMSG LFG TIMEDOUT (page does not exist)")|0x367||
|[SMSG_LFG_OTHER_TIMEDOUT](https://wowdev.wiki/index.php?title=SMSG_LFG_OTHER_TIMEDOUT&action=edit&redlink=1 "SMSG LFG OTHER TIMEDOUT (page does not exist)")|0x368||
|[SMSG_LFG_AUTOJOIN_FAILED](https://wowdev.wiki/index.php?title=SMSG_LFG_AUTOJOIN_FAILED&action=edit&redlink=1 "SMSG LFG AUTOJOIN FAILED (page does not exist)")|0x369||
|[SMSG_LFG_AUTOJOIN_FAILED_NO_PLAYER](https://wowdev.wiki/index.php?title=SMSG_LFG_AUTOJOIN_FAILED_NO_PLAYER&action=edit&redlink=1 "SMSG LFG AUTOJOIN FAILED NO PLAYER (page does not exist)")|0x36A||
|[SMSG_LFG_LEADER_IS_LFM](https://wowdev.wiki/index.php?title=SMSG_LFG_LEADER_IS_LFM&action=edit&redlink=1 "SMSG LFG LEADER IS LFM (page does not exist)")|0x36B||
|[SMSG_LFG_UPDATE](https://wowdev.wiki/index.php?title=SMSG_LFG_UPDATE&action=edit&redlink=1 "SMSG LFG UPDATE (page does not exist)")|0x36C||
|[SMSG_LFG_UPDATE_LFM](https://wowdev.wiki/index.php?title=SMSG_LFG_UPDATE_LFM&action=edit&redlink=1 "SMSG LFG UPDATE LFM (page does not exist)")|0x36D||
|[SMSG_LFG_UPDATE_LFG](https://wowdev.wiki/index.php?title=SMSG_LFG_UPDATE_LFG&action=edit&redlink=1 "SMSG LFG UPDATE LFG (page does not exist)")|0x36E||
|[SMSG_LFG_UPDATE_QUEUED](https://wowdev.wiki/index.php?title=SMSG_LFG_UPDATE_QUEUED&action=edit&redlink=1 "SMSG LFG UPDATE QUEUED (page does not exist)")|0x36F||
|[SMSG_LFG_PENDING_INVITE](https://wowdev.wiki/index.php?title=SMSG_LFG_PENDING_INVITE&action=edit&redlink=1 "SMSG LFG PENDING INVITE (page does not exist)")|0x370||
|[SMSG_LFG_PENDING_MATCH](https://wowdev.wiki/index.php?title=SMSG_LFG_PENDING_MATCH&action=edit&redlink=1 "SMSG LFG PENDING MATCH (page does not exist)")|0x371||
|[SMSG_LFG_PENDING_MATCH_DONE](https://wowdev.wiki/index.php?title=SMSG_LFG_PENDING_MATCH_DONE&action=edit&redlink=1 "SMSG LFG PENDING MATCH DONE (page does not exist)")|0x372||
|[SMSG_TITLE_EARNED](https://wowdev.wiki/index.php?title=SMSG_TITLE_EARNED&action=edit&redlink=1 "SMSG TITLE EARNED (page does not exist)")|0x373||
|[CMSG_SET_TITLE](https://wowdev.wiki/index.php?title=CMSG_SET_TITLE&action=edit&redlink=1 "CMSG SET TITLE (page does not exist)")|0x374||
|[CMSG_CANCEL_MOUNT_AURA](https://wowdev.wiki/index.php?title=CMSG_CANCEL_MOUNT_AURA&action=edit&redlink=1 "CMSG CANCEL MOUNT AURA (page does not exist)")|0x375||
|[SMSG_ARENA_ERROR](https://wowdev.wiki/index.php?title=SMSG_ARENA_ERROR&action=edit&redlink=1 "SMSG ARENA ERROR (page does not exist)")|0x376||
|[MSG_INSPECT_ARENA_TEAMS](https://wowdev.wiki/index.php?title=MSG_INSPECT_ARENA_TEAMS&action=edit&redlink=1 "MSG INSPECT ARENA TEAMS (page does not exist)")|0x377||
|[SMSG_DEATH_RELEASE_LOC](https://wowdev.wiki/index.php?title=SMSG_DEATH_RELEASE_LOC&action=edit&redlink=1 "SMSG DEATH RELEASE LOC (page does not exist)")|0x378||
|[CMSG_CANCEL_TEMP_ENCHANTMENT](https://wowdev.wiki/index.php?title=CMSG_CANCEL_TEMP_ENCHANTMENT&action=edit&redlink=1 "CMSG CANCEL TEMP ENCHANTMENT (page does not exist)")|0x379||
|[SMSG_FORCED_DEATH_UPDATE](https://wowdev.wiki/index.php?title=SMSG_FORCED_DEATH_UPDATE&action=edit&redlink=1 "SMSG FORCED DEATH UPDATE (page does not exist)")|0x37A||
|[CMSG_CHEAT_SET_HONOR_CURRENCY](https://wowdev.wiki/index.php?title=CMSG_CHEAT_SET_HONOR_CURRENCY&action=edit&redlink=1 "CMSG CHEAT SET HONOR CURRENCY (page does not exist)")|0x37B||
|[CMSG_CHEAT_SET_ARENA_CURRENCY](https://wowdev.wiki/index.php?title=CMSG_CHEAT_SET_ARENA_CURRENCY&action=edit&redlink=1 "CMSG CHEAT SET ARENA CURRENCY (page does not exist)")|0x37C||
|[MSG_MOVE_SET_FLIGHT_SPEED_CHEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_FLIGHT_SPEED_CHEAT&action=edit&redlink=1 "MSG MOVE SET FLIGHT SPEED CHEAT (page does not exist)")|0x37D||
|[MSG_MOVE_SET_FLIGHT_SPEED](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_FLIGHT_SPEED&action=edit&redlink=1 "MSG MOVE SET FLIGHT SPEED (page does not exist)")|0x37E||
|[MSG_MOVE_SET_FLIGHT_BACK_SPEED_CHEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_FLIGHT_BACK_SPEED_CHEAT&action=edit&redlink=1 "MSG MOVE SET FLIGHT BACK SPEED CHEAT (page does not exist)")|0x37F||
|[MSG_MOVE_SET_FLIGHT_BACK_SPEED](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_FLIGHT_BACK_SPEED&action=edit&redlink=1 "MSG MOVE SET FLIGHT BACK SPEED (page does not exist)")|0x380||
|[SMSG_FORCE_FLIGHT_SPEED_CHANGE](https://wowdev.wiki/index.php?title=SMSG_FORCE_FLIGHT_SPEED_CHANGE&action=edit&redlink=1 "SMSG FORCE FLIGHT SPEED CHANGE (page does not exist)")|0x381||
|[CMSG_FORCE_FLIGHT_SPEED_CHANGE_ACK](https://wowdev.wiki/index.php?title=CMSG_FORCE_FLIGHT_SPEED_CHANGE_ACK&action=edit&redlink=1 "CMSG FORCE FLIGHT SPEED CHANGE ACK (page does not exist)")|0x382||
|[SMSG_FORCE_FLIGHT_BACK_SPEED_CHANGE](https://wowdev.wiki/index.php?title=SMSG_FORCE_FLIGHT_BACK_SPEED_CHANGE&action=edit&redlink=1 "SMSG FORCE FLIGHT BACK SPEED CHANGE (page does not exist)")|0x383||
|[CMSG_FORCE_FLIGHT_BACK_SPEED_CHANGE_ACK](https://wowdev.wiki/index.php?title=CMSG_FORCE_FLIGHT_BACK_SPEED_CHANGE_ACK&action=edit&redlink=1 "CMSG FORCE FLIGHT BACK SPEED CHANGE ACK (page does not exist)")|0x384||
|[SMSG_SPLINE_SET_FLIGHT_SPEED](https://wowdev.wiki/index.php?title=SMSG_SPLINE_SET_FLIGHT_SPEED&action=edit&redlink=1 "SMSG SPLINE SET FLIGHT SPEED (page does not exist)")|0x385||
|[SMSG_SPLINE_SET_FLIGHT_BACK_SPEED](https://wowdev.wiki/index.php?title=SMSG_SPLINE_SET_FLIGHT_BACK_SPEED&action=edit&redlink=1 "SMSG SPLINE SET FLIGHT BACK SPEED (page does not exist)")|0x386||
|[CMSG_MAELSTROM_INVALIDATE_CACHE](https://wowdev.wiki/index.php?title=CMSG_MAELSTROM_INVALIDATE_CACHE&action=edit&redlink=1 "CMSG MAELSTROM INVALIDATE CACHE (page does not exist)")|0x387||
|[SMSG_FLIGHT_SPLINE_SYNC](https://wowdev.wiki/index.php?title=SMSG_FLIGHT_SPLINE_SYNC&action=edit&redlink=1 "SMSG FLIGHT SPLINE SYNC (page does not exist)")|0x388||
|[CMSG_SET_TAXI_BENCHMARK_MODE](https://wowdev.wiki/index.php?title=CMSG_SET_TAXI_BENCHMARK_MODE&action=edit&redlink=1 "CMSG SET TAXI BENCHMARK MODE (page does not exist)")|0x389||
|[SMSG_JOINED_BATTLEGROUND_QUEUE](https://wowdev.wiki/index.php?title=SMSG_JOINED_BATTLEGROUND_QUEUE&action=edit&redlink=1 "SMSG JOINED BATTLEGROUND QUEUE (page does not exist)")|0x38A||
|[SMSG_REALM_SPLIT](https://wowdev.wiki/index.php?title=SMSG_REALM_SPLIT&action=edit&redlink=1 "SMSG REALM SPLIT (page does not exist)")|0x38B||
|[CMSG_REALM_SPLIT](https://wowdev.wiki/index.php?title=CMSG_REALM_SPLIT&action=edit&redlink=1 "CMSG REALM SPLIT (page does not exist)")|0x38C||
|[CMSG_MOVE_CHNG_TRANSPORT](https://wowdev.wiki/index.php?title=CMSG_MOVE_CHNG_TRANSPORT&action=edit&redlink=1 "CMSG MOVE CHNG TRANSPORT (page does not exist)")|0x38D||
|[MSG_PARTY_ASSIGNMENT](https://wowdev.wiki/index.php?title=MSG_PARTY_ASSIGNMENT&action=edit&redlink=1 "MSG PARTY ASSIGNMENT (page does not exist)")|0x38E||
|[SMSG_OFFER_PETITION_ERROR](https://wowdev.wiki/index.php?title=SMSG_OFFER_PETITION_ERROR&action=edit&redlink=1 "SMSG OFFER PETITION ERROR (page does not exist)")|0x38F||
|[SMSG_TIME_SYNC_REQ](https://wowdev.wiki/index.php?title=SMSG_TIME_SYNC_REQ&action=edit&redlink=1 "SMSG TIME SYNC REQ (page does not exist)")|0x390||
|[CMSG_TIME_SYNC_RESP](https://wowdev.wiki/index.php?title=CMSG_TIME_SYNC_RESP&action=edit&redlink=1 "CMSG TIME SYNC RESP (page does not exist)")|0x391||
|[CMSG_SEND_LOCAL_EVENT](https://wowdev.wiki/index.php?title=CMSG_SEND_LOCAL_EVENT&action=edit&redlink=1 "CMSG SEND LOCAL EVENT (page does not exist)")|0x392||
|[CMSG_SEND_GENERAL_TRIGGER](https://wowdev.wiki/index.php?title=CMSG_SEND_GENERAL_TRIGGER&action=edit&redlink=1 "CMSG SEND GENERAL TRIGGER (page does not exist)")|0x393||
|[CMSG_SEND_COMBAT_TRIGGER](https://wowdev.wiki/index.php?title=CMSG_SEND_COMBAT_TRIGGER&action=edit&redlink=1 "CMSG SEND COMBAT TRIGGER (page does not exist)")|0x394||
|[CMSG_MAELSTROM_GM_SENT_MAIL](https://wowdev.wiki/index.php?title=CMSG_MAELSTROM_GM_SENT_MAIL&action=edit&redlink=1 "CMSG MAELSTROM GM SENT MAIL (page does not exist)")|0x395||
|[SMSG_RESET_FAILED_NOTIFY](https://wowdev.wiki/index.php?title=SMSG_RESET_FAILED_NOTIFY&action=edit&redlink=1 "SMSG RESET FAILED NOTIFY (page does not exist)")|0x396||
|[SMSG_REAL_GROUP_UPDATE](https://wowdev.wiki/index.php?title=SMSG_REAL_GROUP_UPDATE&action=edit&redlink=1 "SMSG REAL GROUP UPDATE (page does not exist)")|0x397||
|[SMSG_LFG_DISABLED](https://wowdev.wiki/index.php?title=SMSG_LFG_DISABLED&action=edit&redlink=1 "SMSG LFG DISABLED (page does not exist)")|0x398||
|[CMSG_ACTIVE_PVP_CHEAT](https://wowdev.wiki/index.php?title=CMSG_ACTIVE_PVP_CHEAT&action=edit&redlink=1 "CMSG ACTIVE PVP CHEAT (page does not exist)")|0x399||
|[CMSG_CHEAT_DUMP_ITEMS_DEBUG_ONLY](https://wowdev.wiki/index.php?title=CMSG_CHEAT_DUMP_ITEMS_DEBUG_ONLY&action=edit&redlink=1 "CMSG CHEAT DUMP ITEMS DEBUG ONLY (page does not exist)")|0x39A||
|[SMSG_CHEAT_DUMP_ITEMS_DEBUG_ONLY_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_CHEAT_DUMP_ITEMS_DEBUG_ONLY_RESPONSE&action=edit&redlink=1 "SMSG CHEAT DUMP ITEMS DEBUG ONLY RESPONSE (page does not exist)")|0x39B||
|[SMSG_CHEAT_DUMP_ITEMS_DEBUG_ONLY_RESPONSE_WRITE_FILE](https://wowdev.wiki/index.php?title=SMSG_CHEAT_DUMP_ITEMS_DEBUG_ONLY_RESPONSE_WRITE_FILE&action=edit&redlink=1 "SMSG CHEAT DUMP ITEMS DEBUG ONLY RESPONSE WRITE FILE (page does not exist)")|0x39C||
|[SMSG_UPDATE_COMBO_POINTS](https://wowdev.wiki/index.php?title=SMSG_UPDATE_COMBO_POINTS&action=edit&redlink=1 "SMSG UPDATE COMBO POINTS (page does not exist)")|0x39D||
|[SMSG_VOICE_SESSION_ROSTER_UPDATE](https://wowdev.wiki/index.php?title=SMSG_VOICE_SESSION_ROSTER_UPDATE&action=edit&redlink=1 "SMSG VOICE SESSION ROSTER UPDATE (page does not exist)")|0x39E||
|[SMSG_VOICE_SESSION_LEAVE](https://wowdev.wiki/index.php?title=SMSG_VOICE_SESSION_LEAVE&action=edit&redlink=1 "SMSG VOICE SESSION LEAVE (page does not exist)")|0x39F||
|[SMSG_VOICE_SESSION_ADJUST_PRIORITY](https://wowdev.wiki/index.php?title=SMSG_VOICE_SESSION_ADJUST_PRIORITY&action=edit&redlink=1 "SMSG VOICE SESSION ADJUST PRIORITY (page does not exist)")|0x3A0||
|[CMSG_VOICE_SET_TALKER_MUTED_REQUEST](https://wowdev.wiki/index.php?title=CMSG_VOICE_SET_TALKER_MUTED_REQUEST&action=edit&redlink=1 "CMSG VOICE SET TALKER MUTED REQUEST (page does not exist)")|0x3A1||
|[SMSG_VOICE_SET_TALKER_MUTED](https://wowdev.wiki/index.php?title=SMSG_VOICE_SET_TALKER_MUTED&action=edit&redlink=1 "SMSG VOICE SET TALKER MUTED (page does not exist)")|0x3A2||
|[SMSG_INIT_EXTRA_AURA_INFO_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_INIT_EXTRA_AURA_INFO_OBSOLETE&action=edit&redlink=1 "SMSG INIT EXTRA AURA INFO OBSOLETE (page does not exist)")|0x3A3||
|[SMSG_SET_EXTRA_AURA_INFO_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_SET_EXTRA_AURA_INFO_OBSOLETE&action=edit&redlink=1 "SMSG SET EXTRA AURA INFO OBSOLETE (page does not exist)")|0x3A4||
|[SMSG_SET_EXTRA_AURA_INFO_NEED_UPDATE_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_SET_EXTRA_AURA_INFO_NEED_UPDATE_OBSOLETE&action=edit&redlink=1 "SMSG SET EXTRA AURA INFO NEED UPDATE OBSOLETE (page does not exist)")|0x3A5||
|[SMSG_CLEAR_EXTRA_AURA_INFO_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_CLEAR_EXTRA_AURA_INFO_OBSOLETE&action=edit&redlink=1 "SMSG CLEAR EXTRA AURA INFO OBSOLETE (page does not exist)")|0x3A6||
|[MSG_MOVE_START_DESCEND](https://wowdev.wiki/index.php?title=MSG_MOVE_START_DESCEND&action=edit&redlink=1 "MSG MOVE START DESCEND (page does not exist)")|0x3A7||
|[CMSG_IGNORE_REQUIREMENTS_CHEAT](https://wowdev.wiki/index.php?title=CMSG_IGNORE_REQUIREMENTS_CHEAT&action=edit&redlink=1 "CMSG IGNORE REQUIREMENTS CHEAT (page does not exist)")|0x3A8||
|[SMSG_IGNORE_REQUIREMENTS_CHEAT](https://wowdev.wiki/index.php?title=SMSG_IGNORE_REQUIREMENTS_CHEAT&action=edit&redlink=1 "SMSG IGNORE REQUIREMENTS CHEAT (page does not exist)")|0x3A9||
|[SMSG_SPELL_CHANCE_PROC_LOG](https://wowdev.wiki/index.php?title=SMSG_SPELL_CHANCE_PROC_LOG&action=edit&redlink=1 "SMSG SPELL CHANCE PROC LOG (page does not exist)")|0x3AA||
|[CMSG_MOVE_SET_RUN_SPEED](https://wowdev.wiki/index.php?title=CMSG_MOVE_SET_RUN_SPEED&action=edit&redlink=1 "CMSG MOVE SET RUN SPEED (page does not exist)")|0x3AB||
|[SMSG_DISMOUNT](https://wowdev.wiki/index.php?title=SMSG_DISMOUNT&action=edit&redlink=1 "SMSG DISMOUNT (page does not exist)")|0x3AC||
|[MSG_MOVE_UPDATE_CAN_FLY](https://wowdev.wiki/index.php?title=MSG_MOVE_UPDATE_CAN_FLY&action=edit&redlink=1 "MSG MOVE UPDATE CAN FLY (page does not exist)")|0x3AD||
|[MSG_RAID_READY_CHECK_CONFIRM](https://wowdev.wiki/index.php?title=MSG_RAID_READY_CHECK_CONFIRM&action=edit&redlink=1 "MSG RAID READY CHECK CONFIRM (page does not exist)")|0x3AE||
|[CMSG_VOICE_SESSION_ENABLE](https://wowdev.wiki/index.php?title=CMSG_VOICE_SESSION_ENABLE&action=edit&redlink=1 "CMSG VOICE SESSION ENABLE (page does not exist)")|0x3AF||
|[SMSG_VOICE_SESSION_ENABLE](https://wowdev.wiki/index.php?title=SMSG_VOICE_SESSION_ENABLE&action=edit&redlink=1 "SMSG VOICE SESSION ENABLE (page does not exist)")|0x3B0||
|[SMSG_VOICE_PARENTAL_CONTROLS](https://wowdev.wiki/index.php?title=SMSG_VOICE_PARENTAL_CONTROLS&action=edit&redlink=1 "SMSG VOICE PARENTAL CONTROLS (page does not exist)")|0x3B1||
|[CMSG_GM_WHISPER](https://wowdev.wiki/index.php?title=CMSG_GM_WHISPER&action=edit&redlink=1 "CMSG GM WHISPER (page does not exist)")|0x3B2||
|[SMSG_GM_MESSAGECHAT](https://wowdev.wiki/index.php?title=SMSG_GM_MESSAGECHAT&action=edit&redlink=1 "SMSG GM MESSAGECHAT (page does not exist)")|0x3B3||
|[MSG_GM_GEARRATING](https://wowdev.wiki/index.php?title=MSG_GM_GEARRATING&action=edit&redlink=1 "MSG GM GEARRATING (page does not exist)")|0x3B4||
|[CMSG_COMMENTATOR_ENABLE](https://wowdev.wiki/index.php?title=CMSG_COMMENTATOR_ENABLE&action=edit&redlink=1 "CMSG COMMENTATOR ENABLE (page does not exist)")|0x3B5||
|[SMSG_COMMENTATOR_STATE_CHANGED](https://wowdev.wiki/index.php?title=SMSG_COMMENTATOR_STATE_CHANGED&action=edit&redlink=1 "SMSG COMMENTATOR STATE CHANGED (page does not exist)")|0x3B6||
|[CMSG_COMMENTATOR_GET_MAP_INFO](https://wowdev.wiki/index.php?title=CMSG_COMMENTATOR_GET_MAP_INFO&action=edit&redlink=1 "CMSG COMMENTATOR GET MAP INFO (page does not exist)")|0x3B7||
|[SMSG_COMMENTATOR_MAP_INFO](https://wowdev.wiki/index.php?title=SMSG_COMMENTATOR_MAP_INFO&action=edit&redlink=1 "SMSG COMMENTATOR MAP INFO (page does not exist)")|0x3B8||
|[CMSG_COMMENTATOR_GET_PLAYER_INFO](https://wowdev.wiki/index.php?title=CMSG_COMMENTATOR_GET_PLAYER_INFO&action=edit&redlink=1 "CMSG COMMENTATOR GET PLAYER INFO (page does not exist)")|0x3B9||
|[SMSG_COMMENTATOR_GET_PLAYER_INFO](https://wowdev.wiki/index.php?title=SMSG_COMMENTATOR_GET_PLAYER_INFO&action=edit&redlink=1 "SMSG COMMENTATOR GET PLAYER INFO (page does not exist)")|0x3BA||
|[SMSG_COMMENTATOR_PLAYER_INFO](https://wowdev.wiki/index.php?title=SMSG_COMMENTATOR_PLAYER_INFO&action=edit&redlink=1 "SMSG COMMENTATOR PLAYER INFO (page does not exist)")|0x3BB||
|[CMSG_COMMENTATOR_ENTER_INSTANCE](https://wowdev.wiki/index.php?title=CMSG_COMMENTATOR_ENTER_INSTANCE&action=edit&redlink=1 "CMSG COMMENTATOR ENTER INSTANCE (page does not exist)")|0x3BC||
|[CMSG_COMMENTATOR_EXIT_INSTANCE](https://wowdev.wiki/index.php?title=CMSG_COMMENTATOR_EXIT_INSTANCE&action=edit&redlink=1 "CMSG COMMENTATOR EXIT INSTANCE (page does not exist)")|0x3BD||
|[CMSG_COMMENTATOR_INSTANCE_COMMAND](https://wowdev.wiki/index.php?title=CMSG_COMMENTATOR_INSTANCE_COMMAND&action=edit&redlink=1 "CMSG COMMENTATOR INSTANCE COMMAND (page does not exist)")|0x3BE||
|[SMSG_CLEAR_TARGET](https://wowdev.wiki/index.php?title=SMSG_CLEAR_TARGET&action=edit&redlink=1 "SMSG CLEAR TARGET (page does not exist)")|0x3BF||
|[CMSG_BOT_DETECTED](https://wowdev.wiki/index.php?title=CMSG_BOT_DETECTED&action=edit&redlink=1 "CMSG BOT DETECTED (page does not exist)")|0x3C0||
|[SMSG_CROSSED_INEBRIATION_THRESHOLD](https://wowdev.wiki/index.php?title=SMSG_CROSSED_INEBRIATION_THRESHOLD&action=edit&redlink=1 "SMSG CROSSED INEBRIATION THRESHOLD (page does not exist)")|0x3C1||
|[CMSG_CHEAT_PLAYER_LOGIN](https://wowdev.wiki/index.php?title=CMSG_CHEAT_PLAYER_LOGIN&action=edit&redlink=1 "CMSG CHEAT PLAYER LOGIN (page does not exist)")|0x3C2||
|[CMSG_CHEAT_PLAYER_LOOKUP](https://wowdev.wiki/index.php?title=CMSG_CHEAT_PLAYER_LOOKUP&action=edit&redlink=1 "CMSG CHEAT PLAYER LOOKUP (page does not exist)")|0x3C3||
|[SMSG_CHEAT_PLAYER_LOOKUP](https://wowdev.wiki/index.php?title=SMSG_CHEAT_PLAYER_LOOKUP&action=edit&redlink=1 "SMSG CHEAT PLAYER LOOKUP (page does not exist)")|0x3C4||
|[SMSG_KICK_REASON](https://wowdev.wiki/index.php?title=SMSG_KICK_REASON&action=edit&redlink=1 "SMSG KICK REASON (page does not exist)")|0x3C5||
|[MSG_RAID_READY_CHECK_FINISHED](https://wowdev.wiki/index.php?title=MSG_RAID_READY_CHECK_FINISHED&action=edit&redlink=1 "MSG RAID READY CHECK FINISHED (page does not exist)")|0x3C6||
|[CMSG_COMPLAIN](https://wowdev.wiki/index.php?title=CMSG_COMPLAIN&action=edit&redlink=1 "CMSG COMPLAIN (page does not exist)")|0x3C7||
|[SMSG_COMPLAIN_RESULT](https://wowdev.wiki/index.php?title=SMSG_COMPLAIN_RESULT&action=edit&redlink=1 "SMSG COMPLAIN RESULT (page does not exist)")|0x3C8||
|[SMSG_FEATURE_SYSTEM_STATUS](https://wowdev.wiki/index.php?title=SMSG_FEATURE_SYSTEM_STATUS&action=edit&redlink=1 "SMSG FEATURE SYSTEM STATUS (page does not exist)")|0x3C9||
|[CMSG_GM_SHOW_COMPLAINTS](https://wowdev.wiki/index.php?title=CMSG_GM_SHOW_COMPLAINTS&action=edit&redlink=1 "CMSG GM SHOW COMPLAINTS (page does not exist)")|0x3CA||
|[CMSG_GM_UNSQUELCH](https://wowdev.wiki/index.php?title=CMSG_GM_UNSQUELCH&action=edit&redlink=1 "CMSG GM UNSQUELCH (page does not exist)")|0x3CB||
|[CMSG_CHANNEL_SILENCE_VOICE](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_SILENCE_VOICE&action=edit&redlink=1 "CMSG CHANNEL SILENCE VOICE (page does not exist)")|0x3CC||
|[CMSG_CHANNEL_SILENCE_ALL](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_SILENCE_ALL&action=edit&redlink=1 "CMSG CHANNEL SILENCE ALL (page does not exist)")|0x3CD||
|[CMSG_CHANNEL_UNSILENCE_VOICE](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_UNSILENCE_VOICE&action=edit&redlink=1 "CMSG CHANNEL UNSILENCE VOICE (page does not exist)")|0x3CE||
|[CMSG_CHANNEL_UNSILENCE_ALL](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_UNSILENCE_ALL&action=edit&redlink=1 "CMSG CHANNEL UNSILENCE ALL (page does not exist)")|0x3CF||
|[CMSG_TARGET_CAST](https://wowdev.wiki/index.php?title=CMSG_TARGET_CAST&action=edit&redlink=1 "CMSG TARGET CAST (page does not exist)")|0x3D0||
|[CMSG_TARGET_SCRIPT_CAST](https://wowdev.wiki/index.php?title=CMSG_TARGET_SCRIPT_CAST&action=edit&redlink=1 "CMSG TARGET SCRIPT CAST (page does not exist)")|0x3D1||
|[CMSG_CHANNEL_DISPLAY_LIST](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_DISPLAY_LIST&action=edit&redlink=1 "CMSG CHANNEL DISPLAY LIST (page does not exist)")|0x3D2||
|[CMSG_SET_ACTIVE_VOICE_CHANNEL](https://wowdev.wiki/index.php?title=CMSG_SET_ACTIVE_VOICE_CHANNEL&action=edit&redlink=1 "CMSG SET ACTIVE VOICE CHANNEL (page does not exist)")|0x3D3||
|[CMSG_GET_CHANNEL_MEMBER_COUNT](https://wowdev.wiki/index.php?title=CMSG_GET_CHANNEL_MEMBER_COUNT&action=edit&redlink=1 "CMSG GET CHANNEL MEMBER COUNT (page does not exist)")|0x3D4||
|[SMSG_CHANNEL_MEMBER_COUNT](https://wowdev.wiki/index.php?title=SMSG_CHANNEL_MEMBER_COUNT&action=edit&redlink=1 "SMSG CHANNEL MEMBER COUNT (page does not exist)")|0x3D5||
|[CMSG_CHANNEL_VOICE_ON](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_VOICE_ON&action=edit&redlink=1 "CMSG CHANNEL VOICE ON (page does not exist)")|0x3D6||
|[CMSG_CHANNEL_VOICE_OFF](https://wowdev.wiki/index.php?title=CMSG_CHANNEL_VOICE_OFF&action=edit&redlink=1 "CMSG CHANNEL VOICE OFF (page does not exist)")|0x3D7||
|[CMSG_DEBUG_LIST_TARGETS](https://wowdev.wiki/index.php?title=CMSG_DEBUG_LIST_TARGETS&action=edit&redlink=1 "CMSG DEBUG LIST TARGETS (page does not exist)")|0x3D8||
|[SMSG_DEBUG_LIST_TARGETS](https://wowdev.wiki/index.php?title=SMSG_DEBUG_LIST_TARGETS&action=edit&redlink=1 "SMSG DEBUG LIST TARGETS (page does not exist)")|0x3D9||
|[SMSG_AVAILABLE_VOICE_CHANNEL](https://wowdev.wiki/index.php?title=SMSG_AVAILABLE_VOICE_CHANNEL&action=edit&redlink=1 "SMSG AVAILABLE VOICE CHANNEL (page does not exist)")|0x3DA||
|[CMSG_ADD_VOICE_IGNORE](https://wowdev.wiki/index.php?title=CMSG_ADD_VOICE_IGNORE&action=edit&redlink=1 "CMSG ADD VOICE IGNORE (page does not exist)")|0x3DB||
|[CMSG_DEL_VOICE_IGNORE](https://wowdev.wiki/index.php?title=CMSG_DEL_VOICE_IGNORE&action=edit&redlink=1 "CMSG DEL VOICE IGNORE (page does not exist)")|0x3DC||
|[CMSG_PARTY_SILENCE](https://wowdev.wiki/index.php?title=CMSG_PARTY_SILENCE&action=edit&redlink=1 "CMSG PARTY SILENCE (page does not exist)")|0x3DD||
|[CMSG_PARTY_UNSILENCE](https://wowdev.wiki/index.php?title=CMSG_PARTY_UNSILENCE&action=edit&redlink=1 "CMSG PARTY UNSILENCE (page does not exist)")|0x3DE||
|[MSG_NOTIFY_PARTY_SQUELCH](https://wowdev.wiki/index.php?title=MSG_NOTIFY_PARTY_SQUELCH&action=edit&redlink=1 "MSG NOTIFY PARTY SQUELCH (page does not exist)")|0x3DF||
|[SMSG_COMSAT_RECONNECT_TRY](https://wowdev.wiki/index.php?title=SMSG_COMSAT_RECONNECT_TRY&action=edit&redlink=1 "SMSG COMSAT RECONNECT TRY (page does not exist)")|0x3E0||
|[SMSG_COMSAT_DISCONNECT](https://wowdev.wiki/index.php?title=SMSG_COMSAT_DISCONNECT&action=edit&redlink=1 "SMSG COMSAT DISCONNECT (page does not exist)")|0x3E1||
|[SMSG_COMSAT_CONNECT_FAIL](https://wowdev.wiki/index.php?title=SMSG_COMSAT_CONNECT_FAIL&action=edit&redlink=1 "SMSG COMSAT CONNECT FAIL (page does not exist)")|0x3E2||
|[SMSG_VOICE_CHAT_STATUS](https://wowdev.wiki/index.php?title=SMSG_VOICE_CHAT_STATUS&action=edit&redlink=1 "SMSG VOICE CHAT STATUS (page does not exist)")|0x3E3||
|[CMSG_REPORT_PVP_AFK](https://wowdev.wiki/index.php?title=CMSG_REPORT_PVP_AFK&action=edit&redlink=1 "CMSG REPORT PVP AFK (page does not exist)")|0x3E4||
|[CMSG_REPORT_PVP_AFK_RESULT](https://wowdev.wiki/index.php?title=CMSG_REPORT_PVP_AFK_RESULT&action=edit&redlink=1 "CMSG REPORT PVP AFK RESULT (page does not exist)")|0x3E5||
|[CMSG_GUILD_BANKER_ACTIVATE](https://wowdev.wiki/index.php?title=CMSG_GUILD_BANKER_ACTIVATE&action=edit&redlink=1 "CMSG GUILD BANKER ACTIVATE (page does not exist)")|0x3E6||
|[CMSG_GUILD_BANK_QUERY_TAB](https://wowdev.wiki/index.php?title=CMSG_GUILD_BANK_QUERY_TAB&action=edit&redlink=1 "CMSG GUILD BANK QUERY TAB (page does not exist)")|0x3E7||
|[SMSG_GUILD_BANK_LIST](https://wowdev.wiki/index.php?title=SMSG_GUILD_BANK_LIST&action=edit&redlink=1 "SMSG GUILD BANK LIST (page does not exist)")|0x3E8||
|[CMSG_GUILD_BANK_SWAP_ITEMS](https://wowdev.wiki/index.php?title=CMSG_GUILD_BANK_SWAP_ITEMS&action=edit&redlink=1 "CMSG GUILD BANK SWAP ITEMS (page does not exist)")|0x3E9||
|[CMSG_GUILD_BANK_BUY_TAB](https://wowdev.wiki/index.php?title=CMSG_GUILD_BANK_BUY_TAB&action=edit&redlink=1 "CMSG GUILD BANK BUY TAB (page does not exist)")|0x3EA||
|[CMSG_GUILD_BANK_UPDATE_TAB](https://wowdev.wiki/index.php?title=CMSG_GUILD_BANK_UPDATE_TAB&action=edit&redlink=1 "CMSG GUILD BANK UPDATE TAB (page does not exist)")|0x3EB||
|[CMSG_GUILD_BANK_DEPOSIT_MONEY](https://wowdev.wiki/index.php?title=CMSG_GUILD_BANK_DEPOSIT_MONEY&action=edit&redlink=1 "CMSG GUILD BANK DEPOSIT MONEY (page does not exist)")|0x3EC||
|[CMSG_GUILD_BANK_WITHDRAW_MONEY](https://wowdev.wiki/index.php?title=CMSG_GUILD_BANK_WITHDRAW_MONEY&action=edit&redlink=1 "CMSG GUILD BANK WITHDRAW MONEY (page does not exist)")|0x3ED||
|[MSG_GUILD_BANK_LOG_QUERY](https://wowdev.wiki/index.php?title=MSG_GUILD_BANK_LOG_QUERY&action=edit&redlink=1 "MSG GUILD BANK LOG QUERY (page does not exist)")|0x3EE||
|[CMSG_SET_CHANNEL_WATCH](https://wowdev.wiki/index.php?title=CMSG_SET_CHANNEL_WATCH&action=edit&redlink=1 "CMSG SET CHANNEL WATCH (page does not exist)")|0x3EF||
|[SMSG_USERLIST_ADD](https://wowdev.wiki/index.php?title=SMSG_USERLIST_ADD&action=edit&redlink=1 "SMSG USERLIST ADD (page does not exist)")|0x3F0||
|[SMSG_USERLIST_REMOVE](https://wowdev.wiki/index.php?title=SMSG_USERLIST_REMOVE&action=edit&redlink=1 "SMSG USERLIST REMOVE (page does not exist)")|0x3F1||
|[SMSG_USERLIST_UPDATE](https://wowdev.wiki/index.php?title=SMSG_USERLIST_UPDATE&action=edit&redlink=1 "SMSG USERLIST UPDATE (page does not exist)")|0x3F2||
|[CMSG_CLEAR_CHANNEL_WATCH](https://wowdev.wiki/index.php?title=CMSG_CLEAR_CHANNEL_WATCH&action=edit&redlink=1 "CMSG CLEAR CHANNEL WATCH (page does not exist)")|0x3F3||
|[SMSG_INSPECT_TALENT](https://wowdev.wiki/index.php?title=SMSG_INSPECT_TALENT&action=edit&redlink=1 "SMSG INSPECT TALENT (page does not exist)")|0x3F4||
|[SMSG_GOGOGO_OBSOLETE](https://wowdev.wiki/index.php?title=SMSG_GOGOGO_OBSOLETE&action=edit&redlink=1 "SMSG GOGOGO OBSOLETE (page does not exist)")|0x3F5||
|[SMSG_ECHO_PARTY_SQUELCH](https://wowdev.wiki/index.php?title=SMSG_ECHO_PARTY_SQUELCH&action=edit&redlink=1 "SMSG ECHO PARTY SQUELCH (page does not exist)")|0x3F6||
|[CMSG_SET_TITLE_SUFFIX](https://wowdev.wiki/index.php?title=CMSG_SET_TITLE_SUFFIX&action=edit&redlink=1 "CMSG SET TITLE SUFFIX (page does not exist)")|0x3F7||
|[CMSG_SPELLCLICK](https://wowdev.wiki/index.php?title=CMSG_SPELLCLICK&action=edit&redlink=1 "CMSG SPELLCLICK (page does not exist)")|0x3F8||
|[SMSG_LOOT_LIST](https://wowdev.wiki/index.php?title=SMSG_LOOT_LIST&action=edit&redlink=1 "SMSG LOOT LIST (page does not exist)")|0x3F9||
|[CMSG_GM_CHARACTER_RESTORE](https://wowdev.wiki/index.php?title=CMSG_GM_CHARACTER_RESTORE&action=edit&redlink=1 "CMSG GM CHARACTER RESTORE (page does not exist)")|0x3FA||
|[CMSG_GM_CHARACTER_SAVE](https://wowdev.wiki/index.php?title=CMSG_GM_CHARACTER_SAVE&action=edit&redlink=1 "CMSG GM CHARACTER SAVE (page does not exist)")|0x3FB||
|[SMSG_VOICESESSION_FULL](https://wowdev.wiki/index.php?title=SMSG_VOICESESSION_FULL&action=edit&redlink=1 "SMSG VOICESESSION FULL (page does not exist)")|0x3FC||
|[MSG_GUILD_PERMISSIONS](https://wowdev.wiki/index.php?title=MSG_GUILD_PERMISSIONS&action=edit&redlink=1 "MSG GUILD PERMISSIONS (page does not exist)")|0x3FD||
|[MSG_GUILD_BANK_MONEY_WITHDRAWN](https://wowdev.wiki/index.php?title=MSG_GUILD_BANK_MONEY_WITHDRAWN&action=edit&redlink=1 "MSG GUILD BANK MONEY WITHDRAWN (page does not exist)")|0x3FE||
|[MSG_GUILD_EVENT_LOG_QUERY](https://wowdev.wiki/index.php?title=MSG_GUILD_EVENT_LOG_QUERY&action=edit&redlink=1 "MSG GUILD EVENT LOG QUERY (page does not exist)")|0x3FF||
|[CMSG_MAELSTROM_RENAME_GUILD](https://wowdev.wiki/index.php?title=CMSG_MAELSTROM_RENAME_GUILD&action=edit&redlink=1 "CMSG MAELSTROM RENAME GUILD (page does not exist)")|0x400||
|[CMSG_GET_MIRRORIMAGE_DATA](https://wowdev.wiki/index.php?title=CMSG_GET_MIRRORIMAGE_DATA&action=edit&redlink=1 "CMSG GET MIRRORIMAGE DATA (page does not exist)")|0x401||
|[SMSG_MIRRORIMAGE_DATA](https://wowdev.wiki/index.php?title=SMSG_MIRRORIMAGE_DATA&action=edit&redlink=1 "SMSG MIRRORIMAGE DATA (page does not exist)")|0x402||
|[SMSG_FORCE_DISPLAY_UPDATE](https://wowdev.wiki/index.php?title=SMSG_FORCE_DISPLAY_UPDATE&action=edit&redlink=1 "SMSG FORCE DISPLAY UPDATE (page does not exist)")|0x403||
|[SMSG_SPELL_CHANCE_RESIST_PUSHBACK](https://wowdev.wiki/index.php?title=SMSG_SPELL_CHANCE_RESIST_PUSHBACK&action=edit&redlink=1 "SMSG SPELL CHANCE RESIST PUSHBACK (page does not exist)")|0x404||
|[CMSG_IGNORE_DIMINISHING_RETURNS_CHEAT](https://wowdev.wiki/index.php?title=CMSG_IGNORE_DIMINISHING_RETURNS_CHEAT&action=edit&redlink=1 "CMSG IGNORE DIMINISHING RETURNS CHEAT (page does not exist)")|0x405||
|[SMSG_IGNORE_DIMINISHING_RETURNS_CHEAT](https://wowdev.wiki/index.php?title=SMSG_IGNORE_DIMINISHING_RETURNS_CHEAT&action=edit&redlink=1 "SMSG IGNORE DIMINISHING RETURNS CHEAT (page does not exist)")|0x406||
|[CMSG_KEEP_ALIVE](https://wowdev.wiki/index.php?title=CMSG_KEEP_ALIVE&action=edit&redlink=1 "CMSG KEEP ALIVE (page does not exist)")|0x407||
|[SMSG_RAID_READY_CHECK_ERROR](https://wowdev.wiki/index.php?title=SMSG_RAID_READY_CHECK_ERROR&action=edit&redlink=1 "SMSG RAID READY CHECK ERROR (page does not exist)")|0x408||
|[CMSG_OPT_OUT_OF_LOOT](https://wowdev.wiki/index.php?title=CMSG_OPT_OUT_OF_LOOT&action=edit&redlink=1 "CMSG OPT OUT OF LOOT (page does not exist)")|0x409||
|[MSG_QUERY_GUILD_BANK_TEXT](https://wowdev.wiki/index.php?title=MSG_QUERY_GUILD_BANK_TEXT&action=edit&redlink=1 "MSG QUERY GUILD BANK TEXT (page does not exist)")|0x40A||
|[CMSG_SET_GUILD_BANK_TEXT](https://wowdev.wiki/index.php?title=CMSG_SET_GUILD_BANK_TEXT&action=edit&redlink=1 "CMSG SET GUILD BANK TEXT (page does not exist)")|0x40B||
|[CMSG_SET_GRANTABLE_LEVELS](https://wowdev.wiki/index.php?title=CMSG_SET_GRANTABLE_LEVELS&action=edit&redlink=1 "CMSG SET GRANTABLE LEVELS (page does not exist)")|0x40C||
|[CMSG_GRANT_LEVEL](https://wowdev.wiki/index.php?title=CMSG_GRANT_LEVEL&action=edit&redlink=1 "CMSG GRANT LEVEL (page does not exist)")|0x40D||
|[CMSG_REFER_A_FRIEND](https://wowdev.wiki/index.php?title=CMSG_REFER_A_FRIEND&action=edit&redlink=1 "CMSG REFER A FRIEND (page does not exist)")|0x40E||
|[MSG_GM_CHANGE_ARENA_RATING](https://wowdev.wiki/index.php?title=MSG_GM_CHANGE_ARENA_RATING&action=edit&redlink=1 "MSG GM CHANGE ARENA RATING (page does not exist)")|0x40F||
|[CMSG_DECLINE_CHANNEL_INVITE](https://wowdev.wiki/index.php?title=CMSG_DECLINE_CHANNEL_INVITE&action=edit&redlink=1 "CMSG DECLINE CHANNEL INVITE (page does not exist)")|0x410||
|[CMSG_GROUPACTION_THROTTLED](https://wowdev.wiki/index.php?title=CMSG_GROUPACTION_THROTTLED&action=edit&redlink=1 "CMSG GROUPACTION THROTTLED (page does not exist)")|0x411||
|[SMSG_OVERRIDE_LIGHT](https://wowdev.wiki/index.php?title=SMSG_OVERRIDE_LIGHT&action=edit&redlink=1 "SMSG OVERRIDE LIGHT (page does not exist)")|0x412||
|[SMSG_TOTEM_CREATED](https://wowdev.wiki/index.php?title=SMSG_TOTEM_CREATED&action=edit&redlink=1 "SMSG TOTEM CREATED (page does not exist)")|0x413||
|[CMSG_TOTEM_DESTROYED](https://wowdev.wiki/index.php?title=CMSG_TOTEM_DESTROYED&action=edit&redlink=1 "CMSG TOTEM DESTROYED (page does not exist)")|0x414||
|[CMSG_EXPIRE_RAID_INSTANCE](https://wowdev.wiki/index.php?title=CMSG_EXPIRE_RAID_INSTANCE&action=edit&redlink=1 "CMSG EXPIRE RAID INSTANCE (page does not exist)")|0x415||
|[CMSG_NO_SPELL_VARIANCE](https://wowdev.wiki/index.php?title=CMSG_NO_SPELL_VARIANCE&action=edit&redlink=1 "CMSG NO SPELL VARIANCE (page does not exist)")|0x416||
|[CMSG_QUESTGIVER_STATUS_MULTIPLE_QUERY](https://wowdev.wiki/index.php?title=CMSG_QUESTGIVER_STATUS_MULTIPLE_QUERY&action=edit&redlink=1 "CMSG QUESTGIVER STATUS MULTIPLE QUERY (page does not exist)")|0x417||
|[SMSG_QUESTGIVER_STATUS_MULTIPLE](https://wowdev.wiki/index.php?title=SMSG_QUESTGIVER_STATUS_MULTIPLE&action=edit&redlink=1 "SMSG QUESTGIVER STATUS MULTIPLE (page does not exist)")|0x418||
|[CMSG_SET_PLAYER_DECLINED_NAMES](https://wowdev.wiki/index.php?title=CMSG_SET_PLAYER_DECLINED_NAMES&action=edit&redlink=1 "CMSG SET PLAYER DECLINED NAMES (page does not exist)")|0x419||
|[SMSG_SET_PLAYER_DECLINED_NAMES_RESULT](https://wowdev.wiki/index.php?title=SMSG_SET_PLAYER_DECLINED_NAMES_RESULT&action=edit&redlink=1 "SMSG SET PLAYER DECLINED NAMES RESULT (page does not exist)")|0x41A||
|[CMSG_QUERY_SERVER_BUCK_DATA](https://wowdev.wiki/index.php?title=CMSG_QUERY_SERVER_BUCK_DATA&action=edit&redlink=1 "CMSG QUERY SERVER BUCK DATA (page does not exist)")|0x41B||
|[CMSG_CLEAR_SERVER_BUCK_DATA](https://wowdev.wiki/index.php?title=CMSG_CLEAR_SERVER_BUCK_DATA&action=edit&redlink=1 "CMSG CLEAR SERVER BUCK DATA (page does not exist)")|0x41C||
|[SMSG_SERVER_BUCK_DATA](https://wowdev.wiki/index.php?title=SMSG_SERVER_BUCK_DATA&action=edit&redlink=1 "SMSG SERVER BUCK DATA (page does not exist)")|0x41D||
|[SMSG_SEND_UNLEARN_SPELLS](https://wowdev.wiki/index.php?title=SMSG_SEND_UNLEARN_SPELLS&action=edit&redlink=1 "SMSG SEND UNLEARN SPELLS (page does not exist)")|0x41E||
|[SMSG_PROPOSE_LEVEL_GRANT](https://wowdev.wiki/index.php?title=SMSG_PROPOSE_LEVEL_GRANT&action=edit&redlink=1 "SMSG PROPOSE LEVEL GRANT (page does not exist)")|0x41F||
|[CMSG_ACCEPT_LEVEL_GRANT](https://wowdev.wiki/index.php?title=CMSG_ACCEPT_LEVEL_GRANT&action=edit&redlink=1 "CMSG ACCEPT LEVEL GRANT (page does not exist)")|0x420||
|[SMSG_REFER_A_FRIEND_FAILURE](https://wowdev.wiki/index.php?title=SMSG_REFER_A_FRIEND_FAILURE&action=edit&redlink=1 "SMSG REFER A FRIEND FAILURE (page does not exist)")|0x421||
|[SMSG_SPLINE_MOVE_SET_FLYING](https://wowdev.wiki/index.php?title=SMSG_SPLINE_MOVE_SET_FLYING&action=edit&redlink=1 "SMSG SPLINE MOVE SET FLYING (page does not exist)")|0x422||
|[SMSG_SPLINE_MOVE_UNSET_FLYING](https://wowdev.wiki/index.php?title=SMSG_SPLINE_MOVE_UNSET_FLYING&action=edit&redlink=1 "SMSG SPLINE MOVE UNSET FLYING (page does not exist)")|0x423||
|[SMSG_SUMMON_CANCEL](https://wowdev.wiki/index.php?title=SMSG_SUMMON_CANCEL&action=edit&redlink=1 "SMSG SUMMON CANCEL (page does not exist)")|0x424||
|[CMSG_CHANGE_PERSONAL_ARENA_RATING](https://wowdev.wiki/index.php?title=CMSG_CHANGE_PERSONAL_ARENA_RATING&action=edit&redlink=1 "CMSG CHANGE PERSONAL ARENA RATING (page does not exist)")|0x425||
|[CMSG_ALTER_APPEARANCE](https://wowdev.wiki/index.php?title=CMSG_ALTER_APPEARANCE&action=edit&redlink=1 "CMSG ALTER APPEARANCE (page does not exist)")|0x426||
|[SMSG_ENABLE_BARBER_SHOP](https://wowdev.wiki/index.php?title=SMSG_ENABLE_BARBER_SHOP&action=edit&redlink=1 "SMSG ENABLE BARBER SHOP (page does not exist)")|0x427||
|[SMSG_BARBER_SHOP_RESULT](https://wowdev.wiki/index.php?title=SMSG_BARBER_SHOP_RESULT&action=edit&redlink=1 "SMSG BARBER SHOP RESULT (page does not exist)")|0x428||
|[CMSG_CALENDAR_GET_CALENDAR](https://wowdev.wiki/index.php?title=CMSG_CALENDAR_GET_CALENDAR&action=edit&redlink=1 "CMSG CALENDAR GET CALENDAR (page does not exist)")|0x429||
|[CMSG_CALENDAR_GET_EVENT](https://wowdev.wiki/index.php?title=CMSG_CALENDAR_GET_EVENT&action=edit&redlink=1 "CMSG CALENDAR GET EVENT (page does not exist)")|0x42A||
|[CMSG_CALENDAR_GUILD_FILTER](https://wowdev.wiki/index.php?title=CMSG_CALENDAR_GUILD_FILTER&action=edit&redlink=1 "CMSG CALENDAR GUILD FILTER (page does not exist)")|0x42B||
|[CMSG_CALENDAR_ARENA_TEAM](https://wowdev.wiki/index.php?title=CMSG_CALENDAR_ARENA_TEAM&action=edit&redlink=1 "CMSG CALENDAR ARENA TEAM (page does not exist)")|0x42C||
|[CMSG_CALENDAR_ADD_EVENT](https://wowdev.wiki/index.php?title=CMSG_CALENDAR_ADD_EVENT&action=edit&redlink=1 "CMSG CALENDAR ADD EVENT (page does not exist)")|0x42D||
|[CMSG_CALENDAR_UPDATE_EVENT](https://wowdev.wiki/index.php?title=CMSG_CALENDAR_UPDATE_EVENT&action=edit&redlink=1 "CMSG CALENDAR UPDATE EVENT (page does not exist)")|0x42E||
|[CMSG_CALENDAR_REMOVE_EVENT](https://wowdev.wiki/index.php?title=CMSG_CALENDAR_REMOVE_EVENT&action=edit&redlink=1 "CMSG CALENDAR REMOVE EVENT (page does not exist)")|0x42F||
|[CMSG_CALENDAR_COPY_EVENT](https://wowdev.wiki/index.php?title=CMSG_CALENDAR_COPY_EVENT&action=edit&redlink=1 "CMSG CALENDAR COPY EVENT (page does not exist)")|0x430||
|[CMSG_CALENDAR_EVENT_INVITE](https://wowdev.wiki/index.php?title=CMSG_CALENDAR_EVENT_INVITE&action=edit&redlink=1 "CMSG CALENDAR EVENT INVITE (page does not exist)")|0x431||
|[CMSG_CALENDAR_EVENT_RSVP](https://wowdev.wiki/index.php?title=CMSG_CALENDAR_EVENT_RSVP&action=edit&redlink=1 "CMSG CALENDAR EVENT RSVP (page does not exist)")|0x432||
|[CMSG_CALENDAR_EVENT_REMOVE_INVITE](https://wowdev.wiki/index.php?title=CMSG_CALENDAR_EVENT_REMOVE_INVITE&action=edit&redlink=1 "CMSG CALENDAR EVENT REMOVE INVITE (page does not exist)")|0x433||
|[CMSG_CALENDAR_EVENT_STATUS](https://wowdev.wiki/index.php?title=CMSG_CALENDAR_EVENT_STATUS&action=edit&redlink=1 "CMSG CALENDAR EVENT STATUS (page does not exist)")|0x434||
|[CMSG_CALENDAR_EVENT_MODERATOR_STATUS](https://wowdev.wiki/index.php?title=CMSG_CALENDAR_EVENT_MODERATOR_STATUS&action=edit&redlink=1 "CMSG CALENDAR EVENT MODERATOR STATUS (page does not exist)")|0x435||
|[SMSG_CALENDAR_SEND_CALENDAR](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_SEND_CALENDAR&action=edit&redlink=1 "SMSG CALENDAR SEND CALENDAR (page does not exist)")|0x436||
|[SMSG_CALENDAR_SEND_EVENT](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_SEND_EVENT&action=edit&redlink=1 "SMSG CALENDAR SEND EVENT (page does not exist)")|0x437||
|[SMSG_CALENDAR_FILTER_GUILD](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_FILTER_GUILD&action=edit&redlink=1 "SMSG CALENDAR FILTER GUILD (page does not exist)")|0x438||
|[SMSG_CALENDAR_ARENA_TEAM](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_ARENA_TEAM&action=edit&redlink=1 "SMSG CALENDAR ARENA TEAM (page does not exist)")|0x439||
|[SMSG_CALENDAR_EVENT_INVITE](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_EVENT_INVITE&action=edit&redlink=1 "SMSG CALENDAR EVENT INVITE (page does not exist)")|0x43A||
|[SMSG_CALENDAR_EVENT_INVITE_REMOVED](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_EVENT_INVITE_REMOVED&action=edit&redlink=1 "SMSG CALENDAR EVENT INVITE REMOVED (page does not exist)")|0x43B||
|[SMSG_CALENDAR_EVENT_STATUS](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_EVENT_STATUS&action=edit&redlink=1 "SMSG CALENDAR EVENT STATUS (page does not exist)")|0x43C||
|[SMSG_CALENDAR_COMMAND_RESULT](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_COMMAND_RESULT&action=edit&redlink=1 "SMSG CALENDAR COMMAND RESULT (page does not exist)")|0x43D||
|[SMSG_CALENDAR_RAID_LOCKOUT_ADDED](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_RAID_LOCKOUT_ADDED&action=edit&redlink=1 "SMSG CALENDAR RAID LOCKOUT ADDED (page does not exist)")|0x43E||
|[SMSG_CALENDAR_RAID_LOCKOUT_REMOVED](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_RAID_LOCKOUT_REMOVED&action=edit&redlink=1 "SMSG CALENDAR RAID LOCKOUT REMOVED (page does not exist)")|0x43F||
|[SMSG_CALENDAR_EVENT_INVITE_ALERT](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_EVENT_INVITE_ALERT&action=edit&redlink=1 "SMSG CALENDAR EVENT INVITE ALERT (page does not exist)")|0x440||
|[SMSG_CALENDAR_EVENT_INVITE_REMOVED_ALERT](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_EVENT_INVITE_REMOVED_ALERT&action=edit&redlink=1 "SMSG CALENDAR EVENT INVITE REMOVED ALERT (page does not exist)")|0x441||
|[SMSG_CALENDAR_EVENT_INVITE_STATUS_ALERT](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_EVENT_INVITE_STATUS_ALERT&action=edit&redlink=1 "SMSG CALENDAR EVENT INVITE STATUS ALERT (page does not exist)")|0x442||
|[SMSG_CALENDAR_EVENT_REMOVED_ALERT](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_EVENT_REMOVED_ALERT&action=edit&redlink=1 "SMSG CALENDAR EVENT REMOVED ALERT (page does not exist)")|0x443||
|[SMSG_CALENDAR_EVENT_UPDATED_ALERT](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_EVENT_UPDATED_ALERT&action=edit&redlink=1 "SMSG CALENDAR EVENT UPDATED ALERT (page does not exist)")|0x444||
|[SMSG_CALENDAR_EVENT_MODERATOR_STATUS_ALERT](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_EVENT_MODERATOR_STATUS_ALERT&action=edit&redlink=1 "SMSG CALENDAR EVENT MODERATOR STATUS ALERT (page does not exist)")|0x445||
|[CMSG_CALENDAR_COMPLAIN](https://wowdev.wiki/index.php?title=CMSG_CALENDAR_COMPLAIN&action=edit&redlink=1 "CMSG CALENDAR COMPLAIN (page does not exist)")|0x446||
|[SMSG_CALENDAR_EVENT_RESERVED_2](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_EVENT_RESERVED_2&action=edit&redlink=1 "SMSG CALENDAR EVENT RESERVED 2 (page does not exist)")|0x447||
|[SMSG_CALENDAR_EVENT_RESERVED_3](https://wowdev.wiki/index.php?title=SMSG_CALENDAR_EVENT_RESERVED_3&action=edit&redlink=1 "SMSG CALENDAR EVENT RESERVED 3 (page does not exist)")|0x448||
|[CMSG_SAVE_DANCE](https://wowdev.wiki/index.php?title=CMSG_SAVE_DANCE&action=edit&redlink=1 "CMSG SAVE DANCE (page does not exist)")|0x449||
|[SMSG_NOTIFY_DANCE](https://wowdev.wiki/index.php?title=SMSG_NOTIFY_DANCE&action=edit&redlink=1 "SMSG NOTIFY DANCE (page does not exist)")|0x44A||
|[CMSG_PLAY_DANCE](https://wowdev.wiki/index.php?title=CMSG_PLAY_DANCE&action=edit&redlink=1 "CMSG PLAY DANCE (page does not exist)")|0x44B||
|[SMSG_PLAY_DANCE](https://wowdev.wiki/index.php?title=SMSG_PLAY_DANCE&action=edit&redlink=1 "SMSG PLAY DANCE (page does not exist)")|0x44C||
|[CMSG_LOAD_DANCES](https://wowdev.wiki/index.php?title=CMSG_LOAD_DANCES&action=edit&redlink=1 "CMSG LOAD DANCES (page does not exist)")|0x44D||
|[CMSG_STOP_DANCE](https://wowdev.wiki/index.php?title=CMSG_STOP_DANCE&action=edit&redlink=1 "CMSG STOP DANCE (page does not exist)")|0x44E||
|[SMSG_STOP_DANCE](https://wowdev.wiki/index.php?title=SMSG_STOP_DANCE&action=edit&redlink=1 "SMSG STOP DANCE (page does not exist)")|0x44F||
|[CMSG_SYNC_DANCE](https://wowdev.wiki/index.php?title=CMSG_SYNC_DANCE&action=edit&redlink=1 "CMSG SYNC DANCE (page does not exist)")|0x450||
|[CMSG_DANCE_QUERY](https://wowdev.wiki/index.php?title=CMSG_DANCE_QUERY&action=edit&redlink=1 "CMSG DANCE QUERY (page does not exist)")|0x451||
|[SMSG_DANCE_QUERY_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_DANCE_QUERY_RESPONSE&action=edit&redlink=1 "SMSG DANCE QUERY RESPONSE (page does not exist)")|0x452||
|[SMSG_INVALIDATE_DANCE](https://wowdev.wiki/index.php?title=SMSG_INVALIDATE_DANCE&action=edit&redlink=1 "SMSG INVALIDATE DANCE (page does not exist)")|0x453||
|[CMSG_DELETE_DANCE](https://wowdev.wiki/index.php?title=CMSG_DELETE_DANCE&action=edit&redlink=1 "CMSG DELETE DANCE (page does not exist)")|0x454||
|[SMSG_LEARNED_DANCE_MOVES](https://wowdev.wiki/index.php?title=SMSG_LEARNED_DANCE_MOVES&action=edit&redlink=1 "SMSG LEARNED DANCE MOVES (page does not exist)")|0x455||
|[CMSG_LEARN_DANCE_MOVE](https://wowdev.wiki/index.php?title=CMSG_LEARN_DANCE_MOVE&action=edit&redlink=1 "CMSG LEARN DANCE MOVE (page does not exist)")|0x456||
|[CMSG_UNLEARN_DANCE_MOVE](https://wowdev.wiki/index.php?title=CMSG_UNLEARN_DANCE_MOVE&action=edit&redlink=1 "CMSG UNLEARN DANCE MOVE (page does not exist)")|0x457||
|[CMSG_SET_RUNE_COUNT](https://wowdev.wiki/index.php?title=CMSG_SET_RUNE_COUNT&action=edit&redlink=1 "CMSG SET RUNE COUNT (page does not exist)")|0x458||
|[CMSG_SET_RUNE_COOLDOWN](https://wowdev.wiki/index.php?title=CMSG_SET_RUNE_COOLDOWN&action=edit&redlink=1 "CMSG SET RUNE COOLDOWN (page does not exist)")|0x459||
|[MSG_MOVE_SET_PITCH_RATE_CHEAT](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_PITCH_RATE_CHEAT&action=edit&redlink=1 "MSG MOVE SET PITCH RATE CHEAT (page does not exist)")|0x45A||
|[MSG_MOVE_SET_PITCH_RATE](https://wowdev.wiki/index.php?title=MSG_MOVE_SET_PITCH_RATE&action=edit&redlink=1 "MSG MOVE SET PITCH RATE (page does not exist)")|0x45B||
|[SMSG_FORCE_PITCH_RATE_CHANG](https://wowdev.wiki/index.php?title=SMSG_FORCE_PITCH_RATE_CHANG&action=edit&redlink=1 "SMSG FORCE PITCH RATE CHANG (page does not exist)")\||0x45C||
|[CMSG_FORCE_PITCH_RATE_CHANGE_ACK](https://wowdev.wiki/index.php?title=CMSG_FORCE_PITCH_RATE_CHANGE_ACK&action=edit&redlink=1 "CMSG FORCE PITCH RATE CHANGE ACK (page does not exist)")|0x45D||
|[SMSG_SPLINE_SET_PITCH_RATE](https://wowdev.wiki/index.php?title=SMSG_SPLINE_SET_PITCH_RATE&action=edit&redlink=1 "SMSG SPLINE SET PITCH RATE (page does not exist)")|0x45E||
|[SMSG_MOVE_ABANDON_TRANSPORT](https://wowdev.wiki/index.php?title=SMSG_MOVE_ABANDON_TRANSPORT&action=edit&redlink=1 "SMSG MOVE ABANDON TRANSPORT (page does not exist)")|0x45F||
|[MSG_MOVE_ABANDON_TRANSPORT](https://wowdev.wiki/index.php?title=MSG_MOVE_ABANDON_TRANSPORT&action=edit&redlink=1 "MSG MOVE ABANDON TRANSPORT (page does not exist)")|0x460||
|[CMSG_MOVE_ABANDON_TRANSPORT_ACK](https://wowdev.wiki/index.php?title=CMSG_MOVE_ABANDON_TRANSPORT_ACK&action=edit&redlink=1 "CMSG MOVE ABANDON TRANSPORT ACK (page does not exist)")|0x461||
|[CMSG_UPDATE_MISSILE_TRAJECTORY](https://wowdev.wiki/index.php?title=CMSG_UPDATE_MISSILE_TRAJECTORY&action=edit&redlink=1 "CMSG UPDATE MISSILE TRAJECTORY (page does not exist)")|0x462||
|[SMSG_UPDATE_ACCOUNT_DATA_COMPLETE](https://wowdev.wiki/index.php?title=SMSG_UPDATE_ACCOUNT_DATA_COMPLETE&action=edit&redlink=1 "SMSG UPDATE ACCOUNT DATA COMPLETE (page does not exist)")|0x463||
|[SMSG_TRIGGER_MOVIE](https://wowdev.wiki/index.php?title=SMSG_TRIGGER_MOVIE&action=edit&redlink=1 "SMSG TRIGGER MOVIE (page does not exist)")|0x464||
|[CMSG_COMPLETE_MOVIE](https://wowdev.wiki/index.php?title=CMSG_COMPLETE_MOVIE&action=edit&redlink=1 "CMSG COMPLETE MOVIE (page does not exist)")|0x465||
|[CMSG_SET_GLYPH_SLOT](https://wowdev.wiki/index.php?title=CMSG_SET_GLYPH_SLOT&action=edit&redlink=1 "CMSG SET GLYPH SLOT (page does not exist)")|0x466||
|[CMSG_SET_GLYPH](https://wowdev.wiki/index.php?title=CMSG_SET_GLYPH&action=edit&redlink=1 "CMSG SET GLYPH (page does not exist)")|0x467||
|[SMSG_ACHIEVEMENT_EARNED](https://wowdev.wiki/index.php?title=SMSG_ACHIEVEMENT_EARNED&action=edit&redlink=1 "SMSG ACHIEVEMENT EARNED (page does not exist)")|0x468||
|[SMSG_DYNAMIC_DROP_ROLL_RESULT](https://wowdev.wiki/index.php?title=SMSG_DYNAMIC_DROP_ROLL_RESULT&action=edit&redlink=1 "SMSG DYNAMIC DROP ROLL RESULT (page does not exist)")|0x469||
|[SMSG_CRITERIA_UPDATE](https://wowdev.wiki/index.php?title=SMSG_CRITERIA_UPDATE&action=edit&redlink=1 "SMSG CRITERIA UPDATE (page does not exist)")|0x46A||
|[CMSG_QUERY_INSPECT_ACHIEVEMENTS](https://wowdev.wiki/index.php?title=CMSG_QUERY_INSPECT_ACHIEVEMENTS&action=edit&redlink=1 "CMSG QUERY INSPECT ACHIEVEMENTS (page does not exist)")|0x46B||
|[SMSG_RESPOND_INSPECT_ACHIEVEMENTS](https://wowdev.wiki/index.php?title=SMSG_RESPOND_INSPECT_ACHIEVEMENTS&action=edit&redlink=1 "SMSG RESPOND INSPECT ACHIEVEMENTS (page does not exist)")|0x46C||
|[CMSG_DISMISS_CONTROLLED_VEHICLE](https://wowdev.wiki/index.php?title=CMSG_DISMISS_CONTROLLED_VEHICLE&action=edit&redlink=1 "CMSG DISMISS CONTROLLED VEHICLE (page does not exist)")|0x46D||
|[CMSG_COMPLETE_ACHIEVEMENT_CHEAT](https://wowdev.wiki/index.php?title=CMSG_COMPLETE_ACHIEVEMENT_CHEAT&action=edit&redlink=1 "CMSG COMPLETE ACHIEVEMENT CHEAT (page does not exist)")|0x46E||
|[SMSG_QUESTUPDATE_ADD_PVP_KILL](https://wowdev.wiki/index.php?title=SMSG_QUESTUPDATE_ADD_PVP_KILL&action=edit&redlink=1 "SMSG QUESTUPDATE ADD PVP KILL (page does not exist)")|0x46F||
|[CMSG_SET_CRITERIA_CHEAT](https://wowdev.wiki/index.php?title=CMSG_SET_CRITERIA_CHEAT&action=edit&redlink=1 "CMSG SET CRITERIA CHEAT (page does not exist)")|0x470||
|[SMSG_GROUP_SWAP_FAILED](https://wowdev.wiki/index.php?title=SMSG_GROUP_SWAP_FAILED&action=edit&redlink=1 "SMSG GROUP SWAP FAILED (page does not exist)")|0x471||
|[CMSG_UNITANIMTIER_CHEAT](https://wowdev.wiki/index.php?title=CMSG_UNITANIMTIER_CHEAT&action=edit&redlink=1 "CMSG UNITANIMTIER CHEAT (page does not exist)")|0x472||
|[CMSG_CHAR_CUSTOMIZE](https://wowdev.wiki/index.php?title=CMSG_CHAR_CUSTOMIZE&action=edit&redlink=1 "CMSG CHAR CUSTOMIZE (page does not exist)")|0x473||
|[SMSG_CHAR_CUSTOMIZE](https://wowdev.wiki/index.php?title=SMSG_CHAR_CUSTOMIZE&action=edit&redlink=1 "SMSG CHAR CUSTOMIZE (page does not exist)")|0x474||
|[SMSG_PET_RENAMEABLE](https://wowdev.wiki/index.php?title=SMSG_PET_RENAMEABLE&action=edit&redlink=1 "SMSG PET RENAMEABLE (page does not exist)")|0x475||
|[CMSG_REQUEST_VEHICLE_EXIT](https://wowdev.wiki/index.php?title=CMSG_REQUEST_VEHICLE_EXIT&action=edit&redlink=1 "CMSG REQUEST VEHICLE EXIT (page does not exist)")|0x476||
|[CMSG_REQUEST_VEHICLE_PREV_SEAT](https://wowdev.wiki/index.php?title=CMSG_REQUEST_VEHICLE_PREV_SEAT&action=edit&redlink=1 "CMSG REQUEST VEHICLE PREV SEAT (page does not exist)")|0x477||
|[CMSG_REQUEST_VEHICLE_NEXT_SEAT](https://wowdev.wiki/index.php?title=CMSG_REQUEST_VEHICLE_NEXT_SEAT&action=edit&redlink=1 "CMSG REQUEST VEHICLE NEXT SEAT (page does not exist)")|0x478||
|[CMSG_REQUEST_VEHICLE_SWITCH_SEAT](https://wowdev.wiki/index.php?title=CMSG_REQUEST_VEHICLE_SWITCH_SEAT&action=edit&redlink=1 "CMSG REQUEST VEHICLE SWITCH SEAT (page does not exist)")|0x479||
|[CMSG_PET_LEARN_TALENT](https://wowdev.wiki/index.php?title=CMSG_PET_LEARN_TALENT&action=edit&redlink=1 "CMSG PET LEARN TALENT (page does not exist)")|0x47A||
|[CMSG_PET_UNLEARN_TALENTS](https://wowdev.wiki/index.php?title=CMSG_PET_UNLEARN_TALENTS&action=edit&redlink=1 "CMSG PET UNLEARN TALENTS (page does not exist)")|0x47B||
|[SMSG_SET_PHASE_SHIFT](https://wowdev.wiki/index.php?title=SMSG_SET_PHASE_SHIFT&action=edit&redlink=1 "SMSG SET PHASE SHIFT (page does not exist)")|0x47C||
|[SMSG_ALL_ACHIEVEMENT_DATA](https://wowdev.wiki/index.php?title=SMSG_ALL_ACHIEVEMENT_DATA&action=edit&redlink=1 "SMSG ALL ACHIEVEMENT DATA (page does not exist)")|0x47D||
|[CMSG_FORCE_SAY_CHEAT](https://wowdev.wiki/index.php?title=CMSG_FORCE_SAY_CHEAT&action=edit&redlink=1 "CMSG FORCE SAY CHEAT (page does not exist)")|0x47E|not used in client|
|[SMSG_HEALTH_UPDATE](https://wowdev.wiki/index.php?title=SMSG_HEALTH_UPDATE&action=edit&redlink=1 "SMSG HEALTH UPDATE (page does not exist)")|0x47F||
|[SMSG_POWER_UPDATE](https://wowdev.wiki/index.php?title=SMSG_POWER_UPDATE&action=edit&redlink=1 "SMSG POWER UPDATE (page does not exist)")|0x480||
|[CMSG_GAMEOBJ_REPORT_USE](https://wowdev.wiki/index.php?title=CMSG_GAMEOBJ_REPORT_USE&action=edit&redlink=1 "CMSG GAMEOBJ REPORT USE (page does not exist)")|0x481||
|[SMSG_HIGHEST_THREAT_UPDATE](https://wowdev.wiki/index.php?title=SMSG_HIGHEST_THREAT_UPDATE&action=edit&redlink=1 "SMSG HIGHEST THREAT UPDATE (page does not exist)")|0x482||
|[SMSG_THREAT_UPDATE](https://wowdev.wiki/index.php?title=SMSG_THREAT_UPDATE&action=edit&redlink=1 "SMSG THREAT UPDATE (page does not exist)")|0x483||
|[SMSG_THREAT_REMOVE](https://wowdev.wiki/index.php?title=SMSG_THREAT_REMOVE&action=edit&redlink=1 "SMSG THREAT REMOVE (page does not exist)")|0x484||
|[SMSG_THREAT_CLEAR](https://wowdev.wiki/index.php?title=SMSG_THREAT_CLEAR&action=edit&redlink=1 "SMSG THREAT CLEAR (page does not exist)")|0x485||
|[SMSG_CONVERT_RUNE](https://wowdev.wiki/index.php?title=SMSG_CONVERT_RUNE&action=edit&redlink=1 "SMSG CONVERT RUNE (page does not exist)")|0x486||
|[SMSG_RESYNC_RUNES](https://wowdev.wiki/index.php?title=SMSG_RESYNC_RUNES&action=edit&redlink=1 "SMSG RESYNC RUNES (page does not exist)")|0x487||
|[SMSG_ADD_RUNE_POWER](https://wowdev.wiki/index.php?title=SMSG_ADD_RUNE_POWER&action=edit&redlink=1 "SMSG ADD RUNE POWER (page does not exist)")|0x488|uint32 amounth|
|[CMSG_START_QUEST](https://wowdev.wiki/index.php?title=CMSG_START_QUEST&action=edit&redlink=1 "CMSG START QUEST (page does not exist)")|0x489||
|[CMSG_REMOVE_GLYPH](https://wowdev.wiki/index.php?title=CMSG_REMOVE_GLYPH&action=edit&redlink=1 "CMSG REMOVE GLYPH (page does not exist)")|0x48A||
|[CMSG_DUMP_OBJECTS](https://wowdev.wiki/index.php?title=CMSG_DUMP_OBJECTS&action=edit&redlink=1 "CMSG DUMP OBJECTS (page does not exist)")|0x48B||
|[SMSG_DUMP_OBJECTS_DATA](https://wowdev.wiki/index.php?title=SMSG_DUMP_OBJECTS_DATA&action=edit&redlink=1 "SMSG DUMP OBJECTS DATA (page does not exist)")|0x48C||
|[CMSG_DISMISS_CRITTER](https://wowdev.wiki/index.php?title=CMSG_DISMISS_CRITTER&action=edit&redlink=1 "CMSG DISMISS CRITTER (page does not exist)")|0x48D||
|[SMSG_NOTIFY_DEST_LOC_SPELL_CAST](https://wowdev.wiki/index.php?title=SMSG_NOTIFY_DEST_LOC_SPELL_CAST&action=edit&redlink=1 "SMSG NOTIFY DEST LOC SPELL CAST (page does not exist)")|0x48E||
|[CMSG_AUCTION_LIST_PENDING_SALES](https://wowdev.wiki/index.php?title=CMSG_AUCTION_LIST_PENDING_SALES&action=edit&redlink=1 "CMSG AUCTION LIST PENDING SALES (page does not exist)")|0x48F||
|[SMSG_AUCTION_LIST_PENDING_SALES](https://wowdev.wiki/index.php?title=SMSG_AUCTION_LIST_PENDING_SALES&action=edit&redlink=1 "SMSG AUCTION LIST PENDING SALES (page does not exist)")|0x490||
|[SMSG_MODIFY_COOLDOWN](https://wowdev.wiki/index.php?title=SMSG_MODIFY_COOLDOWN&action=edit&redlink=1 "SMSG MODIFY COOLDOWN (page does not exist)")|0x491||
|[SMSG_PET_UPDATE_COMBO_POINTS](https://wowdev.wiki/index.php?title=SMSG_PET_UPDATE_COMBO_POINTS&action=edit&redlink=1 "SMSG PET UPDATE COMBO POINTS (page does not exist)")|0x492||
|[CMSG_ENABLETAXI](https://wowdev.wiki/index.php?title=CMSG_ENABLETAXI&action=edit&redlink=1 "CMSG ENABLETAXI (page does not exist)")|0x493||
|[SMSG_PRE_RESURRECT](https://wowdev.wiki/index.php?title=SMSG_PRE_RESURRECT&action=edit&redlink=1 "SMSG PRE RESURRECT (page does not exist)")|0x494||
|[SMSG_AURA_UPDATE_ALL](https://wowdev.wiki/index.php?title=SMSG_AURA_UPDATE_ALL&action=edit&redlink=1 "SMSG AURA UPDATE ALL (page does not exist)")|0x495||
|[SMSG_AURA_UPDATE](https://wowdev.wiki/index.php?title=SMSG_AURA_UPDATE&action=edit&redlink=1 "SMSG AURA UPDATE (page does not exist)")|0x496||
|[CMSG_FLOOD_GRACE_CHEAT](https://wowdev.wiki/index.php?title=CMSG_FLOOD_GRACE_CHEAT&action=edit&redlink=1 "CMSG FLOOD GRACE CHEAT (page does not exist)")|0x497|not used in client|
|[SMSG_SERVER_FIRST_ACHIEVEMENT](https://wowdev.wiki/index.php?title=SMSG_SERVER_FIRST_ACHIEVEMENT&action=edit&redlink=1 "SMSG SERVER FIRST ACHIEVEMENT (page does not exist)")|0x498||
|[SMSG_PET_LEARNED_SPELL](https://wowdev.wiki/index.php?title=SMSG_PET_LEARNED_SPELL&action=edit&redlink=1 "SMSG PET LEARNED SPELL (page does not exist)")|0x499|uint16 spellid 'Your pet learned spell: %s'|
|[SMSG_PET_UNLEARNED_SPELL](https://wowdev.wiki/index.php?title=SMSG_PET_UNLEARNED_SPELL&action=edit&redlink=1 "SMSG PET UNLEARNED SPELL (page does not exist)")|0x49A|uint16 spellid 'Your pet unlearned %s'|
|[CMSG_CHANGE_SEATS_ON_CONTROLLED_VEHICLE](https://wowdev.wiki/index.php?title=CMSG_CHANGE_SEATS_ON_CONTROLLED_VEHICLE&action=edit&redlink=1 "CMSG CHANGE SEATS ON CONTROLLED VEHICLE (page does not exist)")|0x49B|not used in client|
|[CMSG_HEARTH_AND_RESURRECT](https://wowdev.wiki/index.php?title=CMSG_HEARTH_AND_RESURRECT&action=edit&redlink=1 "CMSG HEARTH AND RESURRECT (page does not exist)")|0x49C|lua: HearthAndResurrectFromArea empty|
|[SMSG_CONTROL_VEHICLE](https://wowdev.wiki/index.php?title=SMSG_CONTROL_VEHICLE&action=edit&redlink=1 "SMSG CONTROL VEHICLE (page does not exist)")|0x49D|empty|
|[SMSG_CRITERIA_DELETED](https://wowdev.wiki/index.php?title=SMSG_CRITERIA_DELETED&action=edit&redlink=1 "SMSG CRITERIA DELETED (page does not exist)")|0x49E|uint32|
|[SMSG_ACHIEVEMENT_DELETED](https://wowdev.wiki/index.php?title=SMSG_ACHIEVEMENT_DELETED&action=edit&redlink=1 "SMSG ACHIEVEMENT DELETED (page does not exist)")|0x49F|uint32|
|[CMSG_SERVER_INFO_QUERY](https://wowdev.wiki/index.php?title=CMSG_SERVER_INFO_QUERY&action=edit&redlink=1 "CMSG SERVER INFO QUERY (page does not exist)")|0x4A0|not used in client|
|[SMSG_SERVER_INFO_RESPONSE](https://wowdev.wiki/index.php?title=SMSG_SERVER_INFO_RESPONSE&action=edit&redlink=1 "SMSG SERVER INFO RESPONSE (page does not exist)")|0x4A1|not used in client|
|[CMSG_CHECK_LOGIN_CRITERIA](https://wowdev.wiki/index.php?title=CMSG_CHECK_LOGIN_CRITERIA&action=edit&redlink=1 "CMSG CHECK LOGIN CRITERIA (page does not exist)")|0x4A2|not used in client|
|[SMSG_SERVER_BUCK_DATA_START](https://wowdev.wiki/index.php?title=SMSG_SERVER_BUCK_DATA_START&action=edit&redlink=1 "SMSG SERVER BUCK DATA START (page does not exist)")|0x4A3|not used in client|
|[CMSG_QUERY_VEHICLE_STATUS](https://wowdev.wiki/index.php?title=CMSG_QUERY_VEHICLE_STATUS&action=edit&redlink=1 "CMSG QUERY VEHICLE STATUS (page does not exist)")|0x4A4|not used in client|
|[SMSG_PET_GUIDS](https://wowdev.wiki/index.php?title=SMSG_PET_GUIDS&action=edit&redlink=1 "SMSG PET GUIDS (page does not exist)")|0x4A5||
|[SMSG_CLIENTCACHE_VERSION](https://wowdev.wiki/index.php?title=SMSG_CLIENTCACHE_VERSION&action=edit&redlink=1 "SMSG CLIENTCACHE VERSION (page does not exist)")|0x4A6||
|[NUM_MSG_TYPES](https://wowdev.wiki/index.php?title=NUM_MSG_TYPES&action=edit&redlink=1 "NUM MSG TYPES (page does not exist)")|0x4A7|

Adaptet from Hearthstone/Opcodes.h