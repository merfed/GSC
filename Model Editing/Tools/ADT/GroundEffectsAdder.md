- **Author**: Schlumpf
- **AKA**: GEAdder, GroundEffectAdder

There are two versions of this floating around. `groundeffectadder.exe` (480 KB) and `groundeffectadderEmperor.exe` (293 KB). Sources are available for both of these. The only significant changes between these files are in the `FindTextures()` function.

**GroundEffectAdder**

```cpp
void FindTextures()
{
	int nTex=0;
	fseek(Input,0x1060,SEEK_SET);
	fread(&nTex,sizeof(unsigned int),1,Input);
	char text[nTex];
	fseek(Input,0x1064,SEEK_SET);
	fread(text,sizeof(char),nTex,Input);

	int i = 0;
	int j = 0;
	while(i<nTex)
	{
		printf("please assign doodads to: \n\t");
		while(text[i]!='\0')
		{
			printf("%c",text[i]);
			i++;
		}
		printf("\n (-1: no change to existing doodads)\n");
        int newd;
		cin >> newd;
		DoodadForTexture[j] = newd;
		j++;
		i++;
	}
}
```

**GroundEffectAdderEmperor**

```cpp
void FindTextures()
{
	int nTex=0;
	fseek(Input,0x1060,SEEK_SET); // Reads the size of a MTEX chunk 
	fread(&nTex,sizeof(unsigned int),1,Input); 
	char* text = new char[nTex];
	fseek(Input,0x1064,SEEK_SET); 
	fread(text,sizeof(char),nTex,Input);

	int i = 0;
	int j = 0;	
	
	while(i<nTex)
	{	
		string Tileset = "";
		int GeID;
		cout << "\t";
		while(text[i]!='\0')
		{
			cout << text[i];
			Tileset += text[i];
			i++;
		}
		
		if (Tileset == "tileset/expansion02/howlingfjord/hfjords_shoreb.blp"){GeID = 87204;}
		else if(Tileset == "tileset/expansion06/argus/7arg_dirt03_512.blp"){GeID = 36946;}
		else if(Tileset == "tileset/expansion06/argus/7arg_felrock02_512.blp"){GeID = 109531;}
		else if(Tileset == "tileset/expansion06/argus/7arg_felrock04_512.blp"){GeID = 87486;}
		else if(Tileset == "tileset/expansion05/nagrand/6ng_grass05_512.blp"){GeID = 119373;}
		else if(Tileset == "tileset/aerie peaks/aeriepeaksrockymudbase.blp"){GeID = 100592;}
		else if(Tileset == "tileset/expansion02/howlingfjord/hfjords_bushyb.blp"){GeID = 108003;}
		else if(Tileset == "tileset/expansion02/howlingfjord/hfjords_bushyc.blp"){GeID = 119397;}
		else if(Tileset == "tileset/expansion03/vashjir/vj_seaweed_01.blp"){GeID = 106233;}
		else {GeID = -1;}

		cout << " :: " << GeID << "\n";
		DoodadForTexture[j] = GeID;
		j++;
		i++;
	}
}
```

# Scripts

## Process all ADTs in a Directory

```
for %%a in (*.ADT) do <path_to_ground_effect_adder> "%%a"
```

# Versions

| Name                     | Filesize                        | Author   | Source ? | Notes     |
| ------------------------ | ------------------------------- | -------- | -------- | --------- |
| GroundEffectAdder        | 3 KB (Source)<br />480 KB (exe) | Schlumpf | ✔️       | Version 1 |
| GroundEffectAdder        | 3 KB (Source)<br />480 KB (exe) | Schlumpf | ✔️       | Version 2 |
| GroundEffectAdderEmperor | 4 KB (Source)<br />293 KB (exe) | Schlumpf | ✔️       | Emperor   |
