_Sync'd to version from 21 February 2016._

In this block several data about the player's and its target's infomation is hold.

**by Karliky on 12th July. 09, 11:04** 3.1.3 definition

```
**Offset	Type	Description**
0x00	int64	player ID - 8 bytes integer 
0x79C	float	x
0x798	float	y
0x7A0	float	z
0x8	int32	health (+ 0x17*4)
0x7A8	float	Rotation (/ (3.14159265358979 / 180))
```

**by vsloathe on 12th Sep. 07, 15:40**

```
**Offset	Type	Description**
0x00	int64	player ID - 8 bytes integer 
0x10	float	x
0x14	float	y
0x18	float	z
0x1C	float	horizontal direction (0 ... 2*PI) 
0x20	float	vertical direction (-PI/2 ... PI/2) 
0x30	pointer	(4 bytes address, pointer to another structure) +0x58 health - int32 
0x30	pointer	+0x5C mana - int32
0x40	int64	target ID
0x58	int32	health
0x5C	int32	mana
```

# Player Structure

   ```cpp
struct Player
   {
       /*0x0000*/ QWORD ObjectFieldGuid;
       /*0x0008*/ unsigned int ObjectFieldType;
       /*0x000c*/ unsigned int ObjectFieldEntry;
       /*0x0010*/ float ObjectFieldScaleX;
       /*0x0014*/ unsigned int ObjectFieldPadding;
       /*0x0018*/ QWORD UnitFieldCharm;
       /*0x0020*/ QWORD UnitFieldSummon;
       /*0x0028*/ QWORD UnitFieldCharmedby;
       /*0x0030*/ QWORD UnitFieldSummonedby;
       /*0x0038*/ QWORD UnitFieldCreatedby;
       /*0x0040*/ QWORD UnitFieldTarget;
       /*0x0048*/ QWORD UnitFieldPersuaded;
       /*0x0050*/ QWORD UnitFieldChannelObject;
       /*0x0058*/ unsigned int UnitFieldHealth;
       /*0x005c*/ unsigned int UnitFieldPower1;
       /*0x0060*/ unsigned int UnitFieldPower2;
       /*0x0064*/ unsigned int UnitFieldPower3;
       /*0x0068*/ unsigned int UnitFieldPower4;
       /*0x006c*/ unsigned int UnitFieldPower5;
       /*0x0070*/ unsigned int UnitFieldMaxhealth;
       /*0x0074*/ unsigned int UnitFieldMaxpower1;
       /*0x0078*/ unsigned int UnitFieldMaxpower2;
       /*0x007c*/ unsigned int UnitFieldMaxpower3;
       /*0x0080*/ unsigned int UnitFieldMaxpower4;
       /*0x0084*/ unsigned int UnitFieldMaxpower5;
       /*0x0088*/ unsigned int UnitFieldLevel;
       /*0x008c*/ unsigned int UnitFieldFactiontemplate;
       /*0x0090*/ char UnitFieldBytes0[4];
       /*0x0094*/ unsigned int UnitVirtualItemSlotDisplay[3];
       /*0x00a0*/ char UnitVirtualItemInfo[24];
       /*0x00b8*/ unsigned int UnitFieldFlags;
       /*0x00bc*/ unsigned int UnitFieldFlags2;
       /*0x00c0*/ unsigned int UnitFieldAura[56];
       /*0x01a0*/ char UnitFieldAuraflags[56];
       /*0x01d8*/ char UnitFieldAuralevels[56];
       /*0x0210*/ char UnitFieldAuraapplications[56];
       /*0x0248*/ unsigned int UnitFieldAurastate;
       /*0x024c*/ unsigned int UnitFieldBaseattacktime[2];
       /*0x0254*/ unsigned int UnitFieldRangedattacktime;
       /*0x0258*/ float UnitFieldBoundingradius;
       /*0x025c*/ float UnitFieldCombatreach;
       /*0x0260*/ unsigned int UnitFieldDisplayid;
       /*0x0264*/ unsigned int UnitFieldNativedisplayid;
       /*0x0268*/ unsigned int UnitFieldMountdisplayid;
       /*0x026c*/ float UnitFieldMindamage;
       /*0x0270*/ float UnitFieldMaxdamage;
       /*0x0274*/ float UnitFieldMinoffhanddamage;
       /*0x0278*/ float UnitFieldMaxoffhanddamage;
       /*0x027c*/ char UnitFieldBytes1[4];
       /*0x0280*/ unsigned int UnitFieldPetnumber;
       /*0x0284*/ unsigned int UnitFieldPetNameTimestamp;
       /*0x0288*/ unsigned int UnitFieldPetexperience;
       /*0x028c*/ unsigned int UnitFieldPetnextlevelexp;
       /*0x0290*/ unsigned int UnitDynamicFlags;
       /*0x0294*/ unsigned int UnitChannelSpell;
       /*0x0298*/ float UnitModCastSpeed;
       /*0x029c*/ unsigned int UnitCreatedBySpell;
       /*0x02a0*/ unsigned int UnitNpcFlags;
       /*0x02a4*/ unsigned int UnitNpcEmotestate;
       /*0x02a8*/ int UnitTrainingPoints;
       /*0x02ac*/ unsigned int UnitFieldStat0;
       /*0x02b0*/ unsigned int UnitFieldStat1;
       /*0x02b4*/ unsigned int UnitFieldStat2;
       /*0x02b8*/ unsigned int UnitFieldStat3;
       /*0x02bc*/ unsigned int UnitFieldStat4;
       /*0x02c0*/ unsigned int UnitFieldPosstat0;
       /*0x02c4*/ unsigned int UnitFieldPosstat1;
       /*0x02c8*/ unsigned int UnitFieldPosstat2;
       /*0x02cc*/ unsigned int UnitFieldPosstat3;
       /*0x02d0*/ unsigned int UnitFieldPosstat4;
       /*0x02d4*/ unsigned int UnitFieldNegstat0;
       /*0x02d8*/ unsigned int UnitFieldNegstat1;
       /*0x02dc*/ unsigned int UnitFieldNegstat2;
       /*0x02e0*/ unsigned int UnitFieldNegstat3;
       /*0x02e4*/ unsigned int UnitFieldNegstat4;
       /*0x02e8*/ unsigned int UnitFieldResistances[7];
       /*0x0304*/ unsigned int UnitFieldResistancebuffmodspositive[7];
       /*0x0320*/ unsigned int UnitFieldResistancebuffmodsnegative[7];
       /*0x033c*/ unsigned int UnitFieldBaseMana;
       /*0x0340*/ unsigned int UnitFieldBaseHealth;
       /*0x0344*/ char UnitFieldBytes2[4];
       /*0x0348*/ unsigned int UnitFieldAttackPower;
       /*0x034c*/ int UnitFieldAttackPowerMods;
       /*0x0350*/ float UnitFieldAttackPowerMultiplier;
       /*0x0354*/ unsigned int UnitFieldRangedAttackPower;
       /*0x0358*/ int UnitFieldRangedAttackPowerMods;
       /*0x035c*/ float UnitFieldRangedAttackPowerMultiplier;
       /*0x0360*/ float UnitFieldMinrangeddamage;
       /*0x0364*/ float UnitFieldMaxrangeddamage;
       /*0x0368*/ unsigned int UnitFieldPowerCostModifier[7];
       /*0x0384*/ float UnitFieldPowerCostMultiplier[7];
       /*0x0388*/ QWORD PlayerDuelArbiter;
       /*0x0390*/ unsigned int PlayerFlags;
       /*0x0394*/ unsigned int PlayerGuildid;
       /*0x0398*/ unsigned int PlayerGuildrank;
       /*0x039c*/ char PlayerBytes[4];
       /*0x03a0*/ char PlayerBytes2[4];
       /*0x03a4*/ char PlayerBytes3[4];
       /*0x03a8*/ unsigned int PlayerDuelTeam;
       /*0x03ac*/ unsigned int PlayerGuildTimestamp;
       /*0x03b0*/ unsigned int PlayerQuestLog11;
       /*0x03b4*/ unsigned int PlayerQuestLog12[2];
       /*0x03bc*/ unsigned int PlayerQuestLog21;
       /*0x03c0*/ unsigned int PlayerQuestLog22[2];
       /*0x03c8*/ unsigned int PlayerQuestLog31;
       /*0x03cc*/ unsigned int PlayerQuestLog32[2];
       /*0x03d4*/ unsigned int PlayerQuestLog41;
       /*0x03d8*/ unsigned int PlayerQuestLog42[2];
       /*0x03e0*/ unsigned int PlayerQuestLog51;
       /*0x03e4*/ unsigned int PlayerQuestLog52[2];
       /*0x03ec*/ unsigned int PlayerQuestLog61;
       /*0x03f0*/ unsigned int PlayerQuestLog62[2];
       /*0x03f8*/ unsigned int PlayerQuestLog71;
       /*0x03fc*/ unsigned int PlayerQuestLog72[2];
       /*0x0404*/ unsigned int PlayerQuestLog81;
       /*0x0408*/ unsigned int PlayerQuestLog82[2];
       /*0x0410*/ unsigned int PlayerQuestLog91;
       /*0x0414*/ unsigned int PlayerQuestLog92[2];
       /*0x041c*/ unsigned int PlayerQuestLog101;
       /*0x0420*/ unsigned int PlayerQuestLog102[2];
       /*0x0428*/ unsigned int PlayerQuestLog111;
       /*0x042c*/ unsigned int PlayerQuestLog112[2];
       /*0x0434*/ unsigned int PlayerQuestLog121;
       /*0x0438*/ unsigned int PlayerQuestLog122[2];
       /*0x0440*/ unsigned int PlayerQuestLog131;
       /*0x0444*/ unsigned int PlayerQuestLog132[2];
       /*0x044c*/ unsigned int PlayerQuestLog141;
       /*0x0450*/ unsigned int PlayerQuestLog142[2];
       /*0x0458*/ unsigned int PlayerQuestLog151;
       /*0x045c*/ unsigned int PlayerQuestLog152[2];
       /*0x0464*/ unsigned int PlayerQuestLog161;
       /*0x0468*/ unsigned int PlayerQuestLog162[2];
       /*0x0470*/ unsigned int PlayerQuestLog171;
       /*0x0474*/ unsigned int PlayerQuestLog172[2];
       /*0x047c*/ unsigned int PlayerQuestLog181;
       /*0x0480*/ unsigned int PlayerQuestLog182[2];
       /*0x0488*/ unsigned int PlayerQuestLog191;
       /*0x048c*/ unsigned int PlayerQuestLog192[2];
       /*0x0494*/ unsigned int PlayerQuestLog201;
       /*0x0498*/ unsigned int PlayerQuestLog202[2];
       /*0x04a0*/ unsigned int PlayerQuestLog211;
       /*0x04a4*/ unsigned int PlayerQuestLog212[2];
       /*0x04ac*/ unsigned int PlayerQuestLog221;
       /*0x04b0*/ unsigned int PlayerQuestLog222[2];
       /*0x04b8*/ unsigned int PlayerQuestLog231;
       /*0x04bc*/ unsigned int PlayerQuestLog232[2];
       /*0x04c4*/ unsigned int PlayerQuestLog241;
       /*0x04c8*/ unsigned int PlayerQuestLog242[2];
       /*0x04d0*/ unsigned int PlayerQuestLog251;
       /*0x04d4*/ unsigned int PlayerQuestLog252[2];
       /*0x04dc*/ QWORD PlayerVisibleItem1Creator;
       /*0x04e4*/ unsigned int PlayerVisibleItem10[12];
       /*0x0514*/ int PlayerVisibleItem1Properties;
       /*0x0518*/ unsigned int PlayerVisibleItem1Pad;
       /*0x051c*/ QWORD PlayerVisibleItem2Creator;
       /*0x0524*/ unsigned int PlayerVisibleItem20[12];
       /*0x0554*/ int PlayerVisibleItem2Properties;
       /*0x0558*/ unsigned int PlayerVisibleItem2Pad;
       /*0x055c*/ QWORD PlayerVisibleItem3Creator;
       /*0x0564*/ unsigned int PlayerVisibleItem30[12];
       /*0x0594*/ int PlayerVisibleItem3Properties;
       /*0x0598*/ unsigned int PlayerVisibleItem3Pad;
       /*0x059c*/ QWORD PlayerVisibleItem4Creator;
       /*0x05a4*/ unsigned int PlayerVisibleItem40[12];
       /*0x05d4*/ int PlayerVisibleItem4Properties;
       /*0x05d8*/ unsigned int PlayerVisibleItem4Pad;
       /*0x05dc*/ QWORD PlayerVisibleItem5Creator;
       /*0x05e4*/ unsigned int PlayerVisibleItem50[12];
       /*0x0614*/ int PlayerVisibleItem5Properties;
       /*0x0618*/ unsigned int PlayerVisibleItem5Pad;
       /*0x061c*/ QWORD PlayerVisibleItem6Creator;
       /*0x0624*/ unsigned int PlayerVisibleItem60[12];
       /*0x0654*/ int PlayerVisibleItem6Properties;
       /*0x0658*/ unsigned int PlayerVisibleItem6Pad;
       /*0x065c*/ QWORD PlayerVisibleItem7Creator;
       /*0x0664*/ unsigned int PlayerVisibleItem70[12];
       /*0x0694*/ int PlayerVisibleItem7Properties;
       /*0x0698*/ unsigned int PlayerVisibleItem7Pad;
       /*0x069c*/ QWORD PlayerVisibleItem8Creator;
       /*0x06a4*/ unsigned int PlayerVisibleItem80[12];
       /*0x06d4*/ int PlayerVisibleItem8Properties;
       /*0x06d8*/ unsigned int PlayerVisibleItem8Pad;
       /*0x06dc*/ QWORD PlayerVisibleItem9Creator;
       /*0x06e4*/ unsigned int PlayerVisibleItem90[12];
       /*0x0714*/ int PlayerVisibleItem9Properties;
       /*0x0718*/ unsigned int PlayerVisibleItem9Pad;
       /*0x071c*/ QWORD PlayerVisibleItem10Creator;
       /*0x0724*/ unsigned int PlayerVisibleItem100[12];
       /*0x0754*/ int PlayerVisibleItem10Properties;
       /*0x0758*/ unsigned int PlayerVisibleItem10Pad;
       /*0x075c*/ QWORD PlayerVisibleItem11Creator;
       /*0x0764*/ unsigned int PlayerVisibleItem110[12];
       /*0x0794*/ int PlayerVisibleItem11Properties;
       /*0x0798*/ unsigned int PlayerVisibleItem11Pad;
       /*0x079c*/ QWORD PlayerVisibleItem12Creator;
       /*0x07a4*/ unsigned int PlayerVisibleItem120[12];
       /*0x07d4*/ int PlayerVisibleItem12Properties;
       /*0x07d8*/ unsigned int PlayerVisibleItem12Pad;
       /*0x07dc*/ QWORD PlayerVisibleItem13Creator;
       /*0x07e4*/ unsigned int PlayerVisibleItem130[12];
       /*0x0814*/ int PlayerVisibleItem13Properties;
       /*0x0818*/ unsigned int PlayerVisibleItem13Pad;
       /*0x081c*/ QWORD PlayerVisibleItem14Creator;
       /*0x0824*/ unsigned int PlayerVisibleItem140[12];
       /*0x0854*/ int PlayerVisibleItem14Properties;
       /*0x0858*/ unsigned int PlayerVisibleItem14Pad;
       /*0x085c*/ QWORD PlayerVisibleItem15Creator;
       /*0x0864*/ unsigned int PlayerVisibleItem150[12];
       /*0x0894*/ int PlayerVisibleItem15Properties;
       /*0x0898*/ unsigned int PlayerVisibleItem15Pad;
       /*0x089c*/ QWORD PlayerVisibleItem16Creator;
       /*0x08a4*/ unsigned int PlayerVisibleItem160[12];
       /*0x08d4*/ int PlayerVisibleItem16Properties;
       /*0x08d8*/ unsigned int PlayerVisibleItem16Pad;
       /*0x08dc*/ QWORD PlayerVisibleItem17Creator;
       /*0x08e4*/ unsigned int PlayerVisibleItem170[12];
       /*0x0914*/ int PlayerVisibleItem17Properties;
       /*0x0918*/ unsigned int PlayerVisibleItem17Pad;
       /*0x091c*/ QWORD PlayerVisibleItem18Creator;
       /*0x0924*/ unsigned int PlayerVisibleItem180[12];
       /*0x0954*/ int PlayerVisibleItem18Properties;
       /*0x0958*/ unsigned int PlayerVisibleItem18Pad;
       /*0x095c*/ QWORD PlayerVisibleItem19Creator;
       /*0x0964*/ unsigned int PlayerVisibleItem190[12];
       /*0x0994*/ int PlayerVisibleItem19Properties;
       /*0x0998*/ unsigned int PlayerVisibleItem19Pad;
       /*0x099c*/ unsigned int PlayerChosenTitle;
       /*0x09a0*/ QWORD PlayerFieldInvSlotHead[23];
       /*0x0a58*/ QWORD PlayerFieldPackSlot1[16];
       /*0x0ad8*/ QWORD PlayerFieldBankSlot1[28];
       /*0x0bb8*/ QWORD PlayerFieldBankbagSlot1[7];
       /*0x0bf0*/ QWORD PlayerFieldVendorbuybackSlot1[12];
       /*0x0c50*/ QWORD PlayerFieldKeyringSlot1[32];
       /*0x0d50*/ QWORD PlayerFarsight;
       /*0x0d58*/ QWORD PlayerFieldKnownTitles;
       /*0x0d60*/ unsigned int PlayerXp;
       /*0x0d64*/ unsigned int PlayerNextLevelXp;
       /*0x0d68*/ int PlayerSkillInfo11[384];
       /*0x1368*/ unsigned int PlayerCharacterPoints1;
       /*0x136c*/ unsigned int PlayerCharacterPoints2;
       /*0x1370*/ unsigned int PlayerTrackCreatures;
       /*0x1374*/ unsigned int PlayerTrackResources;
       /*0x1378*/ float PlayerBlockPercentage;
       /*0x137c*/ float PlayerDodgePercentage;
       /*0x1380*/ float PlayerParryPercentage;
       /*0x1384*/ unsigned int PlayerExpertise;
       /*0x1388*/ float PlayerCritPercentage;
       /*0x138c*/ float PlayerRangedCritPercentage;
       /*0x1390*/ float PlayerOffhandCritPercentage;
       /*0x1394*/ float PlayerSpellCritPercentage1[7];
       /*0x13b0*/ unsigned int PlayerShieldBlock;
       /*0x13b4*/ char PlayerExploredZones1[256];
       /*0x14b4*/ unsigned int PlayerRestStateExperience;
       /*0x14b8*/ unsigned int PlayerFieldCoinage;
       /*0x14bc*/ unsigned int PlayerFieldModDamageDonePos[7];
       /*0x14d8*/ unsigned int PlayerFieldModDamageDoneNeg[7];
       /*0x14f4*/ unsigned int PlayerFieldModDamageDonePct[7];
       /*0x1510*/ unsigned int PlayerFieldModHealingDonePos;
       /*0x1514*/ unsigned int PlayerFieldModTargetResistance;
       /*0x1518*/ char PlayerFieldBytes[4];
       /*0x151c*/ unsigned int PlayerAmmoId;
       /*0x1520*/ unsigned int PlayerSelfResSpell;
       /*0x1524*/ unsigned int PlayerFieldPvpMedals;
       /*0x1528*/ unsigned int PlayerFieldBuybackPrice1[12];
       /*0x1558*/ unsigned int PlayerFieldBuybackTimestamp1[12];
       /*0x1588*/ int PlayerFieldKills;
       /*0x158c*/ unsigned int PlayerFieldTodayContribution;
       /*0x1590*/ unsigned int PlayerFieldYesterdayContribution;
       /*0x1594*/ unsigned int PlayerFieldLifetimeHonorbaleKills;
       /*0x1598*/ char PlayerFieldBytes2[4];
       /*0x159c*/ unsigned int PlayerFieldWatchedFactionIndex;
       /*0x15a0*/ unsigned int PlayerFieldCombatRating1[24];
       /*0x1600*/ unsigned int PlayerFieldArenaTeamInfo11[18];
       /*0x1648*/ unsigned int PlayerFieldHonorCurrency;
       /*0x164c*/ unsigned int PlayerFieldArenaCurrency;
       /*0x1650*/ float PlayerFieldModManaRegen;
       /*0x1654*/ float PlayerFieldModManaRegenInterrupt;
       /*0x1658*/ unsigned int PlayerFieldMaxLevel;
       /*0x165c*/ unsigned int PlayerFieldDailyQuests1[10];
       /*0x1684*/ unsigned int PlayerFieldPadding;
   };
```