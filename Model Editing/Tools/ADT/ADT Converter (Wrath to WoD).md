- **Author**: ???

ADTConverter converts ADTs from <span class="wrath">Wrath</span> (3.3.5) to <span class="wod">WoD</span> (6.x.x).

# How to use

1. Put your <span class="wrath">Wrath</span> ADTs in the data Folder
2. Start the `ConvertADTs.cmd`

# Changelog

- **v0.0.0**
	- ADTConvert is deprecated and no longer supported
- **v1.0.5.1127**
	- Fix a bug that added 4 wrong bytes to the end of the MH20 Chunk.
	- Fix crash on one digit adt naming
- **v1.0.4.469**
	- Implement Legion convert for `_obj1.adt`
	- Implement World Table (WDT, WDL, & TEX) files
	- Implement WDL generation
		- **With correctly generated WDL**:
		- ![[lqd0a5r7.bmp]]
		- **With incorrectly generated WDL**:
		- ![[nuk81q1u.bmp]]
- **v1.0.3.158**
	- Fix Multiple MVAR chunks in Root ADT
	- ![[6fdc6ni7.bmp]]
- **v1.0.3.15**
	- Add folder convert (see `ConvertADTs.cmd`)
	- Optimize for Mono (Linux .NET Framework)
	- Change "any key to close" to ESC key
- **v1.0.2.4**
	- Add [watch mode](https://youtu.be/ZAz_256wfwg)
	- Add output path argument
	- Add help argument
	- Change arugment handling
	- Clear code
- **v1.0.1.2**
	- Rewrite MHDR chunk
	- Fix chunk order in root ADT
	- Clean code
	- Add dynamic revision number

# Versions

| Version    | Source ? | Date                                        |
| ---------- | -------- | ------------------------------------------- |
| 1.0.0      | ✔️       | *No date*                                   |
| 1.0.0.0    | ✔️       | Sep 29, 2016                                |
| 1.0.1.2    | ✔️       | Oct 1, 2016                                 |
| 1.0.2.4    | ✔️       | Oct 3, 2016                                 |
| 1.0.3.15   | ✔️       | Oct 14, 2016                                |
| 1.0.3.158  | ✔️       | Mar 6, 2017                                 |
| 1.0.4.469  | ✔️       | Jan 1, 2018                                 |
| 1.0.5.1127 | ✔️       | Oct 31, 2019                                |
| 0.0.0      | ✔️       | Apr 2, 2020, *Final version, repo archived* |
