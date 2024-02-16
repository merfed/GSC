- **Author**: Mjollna
- **Syntax**: `importMH20.exe <target adt> <water to import.mh20>`
- **Syntax**: `exportMH20.exe <target adt>`

Alternative solution to using [[AllWater]], especially when an ADT has different water levels and liquid types in it.

**exportMH20** exports the MH20 of an ADT into a `.mh20` file. 

**importMH20** imports an exported `.mh20` file into a an ADT. It reintegrates the MH20 at the correct place (and subsequently does all the offsets and calculates the correct chunk size), rather than at the end of the file. It creates an ADT with the extension "`.adt_new`" to avoid modifying the source ADT.

Apart from the MH20 and MCIN offsets, all other chunks will remain untouched. This means if you have MCLQ chunks in your ADT they will be kept, and you probably won't get the result you expect. You can use the "*remove all awater information*" option from AllWater <span class="wrath">Wrath</span> to fix this issue.

# Compiling

Requires [[Gillijim Project]] to compile.

# Versions

| Name       | Filesize                        | Author  | Source ? | Notes                               |
| ---------- | ------------------------------- | ------- | -------- | ----------------------------------- |
| exportMH20 | 1 KB (Source)<br />336 KB (exe) | Mjollna | ✔️       | <= <span class="wrath">Wrath</span> |
| importMH20 | 1 KB (Source)<br />329 KB (exe) | Mjollna | ✔️       | <= <span class="wrath">Wrath</span> |
