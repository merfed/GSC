_Sync'd to version from 25 June 2020._

All time data is located within the time block. Time of day as it is shown on the watch (mouse over the day icon on the minimap) is locked to the apearence of the day. So 12:00 will bring midday while 0:00 will bring night. Changes to the time it self will be updated every tick (1min). While changes to the WorldTimeOfDay is a instant change and will force the timeofday to change too.

# WorldTimeOfDay format per version

First of all, you should know that WorldTimeOfDay has changed in format over the years. From WoW Alpha 0.5.3 to WoW Cataclysm WorldTimeOfDay is a float value from 0 to 1:

_WorldTimeOfDay from WoW Alpha 0.5.3 to WoW Cataclysm_

```
**Value	TimeOfDayMoment**
0   	dawn
0.2     sunrise
0.5     midday
0.7     evening
1       dawn
```

From Mist of Pandaria to the current retail release (BFA), WorldTimeOfDay is a float value that goes from 0 to 1440. You can consider this value to be a minute counter, where 1440 equals 1 day - as 1440 minutes of a day equals 24 hours -.

_WorldTimeOfDay from WoW Mist of Pandaria to retail_

```
**Value	TimeOfDayMoment**
0   	 dawn
360      sunrise
720      midday
1080     evening
1440     dawn
```

So, let's say you want to convert hour and minutes into any of those 2 WorldTimeOfDay formats.

If you want to convert 12:00 (midday) to WoW Alpha 0.5.3 <> WoW Cataclysm format, just do this:

```
var hour = 12;
var minutes = 0;
((3600 * hour) + (60 * minutes)) / 86400
> 0.5
```

And from Mist of Pandaria to the current retail release:

```
var hour = 12;
var minutes = 0;
(((3600 * hour) + (60 * minutes)) / 86400) * 1440
> 720
```

You should also know that WorldTimeOfDay gets updated per every tick of the game from WoW Alpha 0.5.3 to WoW Cataclysm, unlike for Mist of Pandaria to the current retail release that gets updated based on a float value called timeOfDaySpeed.

For any WoW version below 4.x you can just use this pattern **E8 ?? ?? ?? 00 D9 ?? 04** to find where the instructions that update WorldTimeOfDay are located.

From Mist of Pandaria to the current WoW retail release you don't have to patch the binary in order to change the WorldTimeOfDay, you should only replace the timeOfDaySpeed and set it to 0 to prevent the game from updating it.

```
['5.4.8']
timeOfDay: 0xC8DF14,
timeOfDaySpeed: 0xC8DF00,
['6.2.3']
timeOfDay: 0xD7D614,
timeOfDaySpeed: 0xD7D600,
['7.2.5']
timeOfDay: 0xE116C4,
timeOfDaySpeed: 0xE116B0,
```

Just add **WoW.exe + timeOfDay** to get the existing address in memory.

## Structure

_Memory Time Block by Malu05_

```
**Offset	Type	Description**
0x0   	Integer	TimeInMinutes
0x4   	Integer	TimeInHours
0x2C  	Float	TimeSpeed
0x30  	Float	WorldTimeOfDay
```

## 3.3.5.12340 offsets to Time Values

```
**Offset	    Type     Description**
0x00D37F98  Integer  TimeInMinutes
0x00D37F9C  Integer  TimeInHours
0x00D37FC8  Float    TimeSpeed
```

## Legacy offset to TimeMinutes

```
"3.0.2.9056", "diffrenceB2_TimeMin", "0x012D8B78"
"3.0.1.8334", "diffrenceB2_TimeMin", "0x00c6fd30"
"2.4.3.8606", "diffrenceB2_TimeMin", "0x00E11AB8"
"2.4.2.8278", "diffrenceB2_TimeMin", "0x00c6fd30"
"2.4.1.8125", "diffrenceB2_TimeMin", "0x00c6fd30"
"2.3.3.7799", "diffrenceB2_TimeMin", "0x00DBDB08"
```