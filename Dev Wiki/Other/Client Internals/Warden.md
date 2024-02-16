_Sync'd to version from 21 February 2016._

Page is based on WoW 2.4.3 01/9/08 by kynox

# Current methods of attack

- **Hashing module names**
    - Module: 089801ff6aca7b00bbad8d4fefeab53c75e58c61 Key: EF3FC08A
    - Module: 147571bff593004edea415f2390a308d50f4d307 Key: 84A01C4B
    - Module: 29ab9d8324afeec0e8a4504a738ccf61f2919392 Key: 1A44494F
    - Module: 2c4060ba93f31950d9c727d7d499a62ee6b7cfb1 Key: 273A7E44
    - Module: 4a91be8ec38cbdf88a60fe82eb1322829f09aff0 Key: 1AA85316
    - Module: 6ec6545b867fe99ddb315ef3b7118aae341667fe Key: 446A539A
    - Module: 8b0e1572e708106820abdd144bd6537363e55693 Key: 1D8A1BEB
    - Module: ba1272f5c390d8d62984289a6ecb293c5a698208 Key: 777739AA
    - Module: badd8b801de1b9ed3bc65bb6a7a42db5806b6008 Key: 712F9F07
    - Module: bd107865a859de4f0acef954157255b7a4db7c51 Key: 381755D8
    - Module: bfd6aa808dc04c2a5585c63fbb8286dc3f46b13f Key: 93A6E04A
    - Module: ff76bc9112912e53a97517bd78b952e1c4f0272e Key: 5D2621D3

To obtain a hash of your DLL, refer to [http://en.wikipedia.org/wiki/HMAC#Implementation](https://en.wikipedia.org/wiki/HMAC#Implementation) "hash" is SHA-1 for Warden.

- **Hashing regions of memory**

```
**Offset		Size		Description**
0x420541	0xA		WS2_32.Send check
0x48A2CC	0x6		Unknown Chat Related (Called by CGChat__AdChatMessage) // Cypher	
0x48A2F0	0x5		Unknown Chat Related (Called by CGChat__AdChatMessage) // Cypher
0x48D4A0	0xC		AddChatMessage
0x490430	0xC		SendChatMessage
0x49DBB2	0x7		Protected Lua Func Check // Cypher
0x4AA9C2	0x5		FrameXML Signature Check
0x5CDC20	0x6		Unknown Falling Check	 // Cypher
0x61535A	0x9		Unknown. CGUnit_C Member Function. Uses SummonedBy/CreatedBy. ?? // Cypher
0x681778	0x5		
0x7B9D42	0x6		Unknown. Movement related. (?) Only Xref uses CInputControl. // Cypher
0x7BAA98	0xC	
0x8C8398	0x8		Maximum Wall Climb
0x8C845C	0x8		Gravity	 // Cypher
0x8F7AC8	0x8		Jump Velocity // Note from Cypher: Physics sucks ass, its not really velocity but we're calling it that anyway.
0xB93714	0x8		Unknown Login Check (Parental restrictions??) // Cypher	
```

An interesting thing to note about the "Unknown Login Check" is that it's in the .data segment, which is strange given that - except for this - Warden exclusively monitors 'read-only' - .text and .rdata - memory (for obvious reasons).

- **Hashing relative offsets in modules/sections**
- **Hashing driver names**
    - IPSect
    - Afde32u
    - Afde32uu
    - HideEx
- **Determining if certain LUA strings are loaded**

Examples are "OoOoOoooo0oOO" and "BG_DESERTER".

# Countermeasures

Some countermeasures I'm willing to make public are:

- **VirtualQuery** - Hooking VirtualQuery, you can prevent Warden from reading data from your module.
- **Module32First/Next** - You can either use these API to hide your module. An alternative to this is just to remove your module from the PEB linked list. See [[1]](http://www.battleforums.com/forums/diablo-hacking/104427-cloakdll-cpp.html) (scroll down).