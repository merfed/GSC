- **Author**:
- **Syntax**:
- **AKA**: GruulMeWDT

GruulMe is a WDT editor using Qt. You can actually edit everything possible in a WDT with it.

# Notes

To make this clear: this is my first soft using Qt, and one of my first in C++. This is pretty old and absolutely not maintained. The code will look awful for any computer-literate person, but it happens to still be working (on MoP, and probably will on WoD). You're warned !

It doesn't need any FAQ, it's pretty instinctive.

This is free software, let's say Beerware.

# Requirements

With the provided dll, it should work out of the box. If you want to compile it, you'll need Qt SDK. I used Qt 4.8 to do it but it can maybe be compiled with older versions.

# Updates

## Version 3

I added a button to scan the ADTs of a directory. Clicking on "Scan dir" will see if ADTs with the same name that your WDT exist in its directory and add them if so. Example: you just created test.wdt, and `test_23_26.adt` exists; use the scan button and the ADT array will be updated at 23-26.

## Version 2

- Clicking on the ADT array or pressing a "filling" button while no WDT is loaded doesn't make the soft crash anymore.
- There is a new button on the 1st tab to create a new WDT from nothing.
- The ADT array now displays well (I hope). Info moved from top/bottom to left.
- Awesome picture for ADT array background when no WDT is loaded.

# Known bugs

Nothing special atm (hard to believe). Just try to be logic while loading, saving, creating a new file, etc.

# Versions

| Name    | Filesize          | Author | Source ? | Notes |
| ------- | ----------------- | ------ | -------- | ----- |
| GruulMe | 917 KB (Source)<br/>11.3 MB (Release) |        | ✔️         |       |

#unknown_author 