_Sync'd to version from 26 June 2018._

For updating files WoW uses bsdiff. Have a look at "[http://www.daemonology.net/bsdiff/](http://www.daemonology.net/bsdiff/)" or "[http://www.pokorra.de/coding/bsdiff.html](http://www.pokorra.de/coding/bsdiff.html)"

Depending on version, this might not be BSDIFF40 but ZBSDIFF1, which is a variant of BSDIFF40 with seemingly no differences than exchanging BZ2 library calls with their libz inflate equivalents.

# Format

## bsdiff_int64_t

For unknown reason, bsdiff reimplements signed integrals. It also uses them for all values, even those that will never be negative (literally all but seek_in_input), because bsdiff is horrible code.

```
struct bsdiff_int64_t {
  int64_t value : 63;
  int64_t sign : 1;
  operator int64_t() const { return sign ? -value : value; }
  bsdiff_int64_t (int64_t x) : value (abs (x)), sign (value < 0) {}
};

int64_t alternative_manual_implementation (uint64_t raw) {
  int64_t const value = raw & 0x7FFFFFFFFFFFFFFF;
  return                raw & 0x8000000000000000 ? -value : value;
}
uint64_t alternative_manual_implementation (int64_t raw) {
  return abs (raw) | (raw < 0 ? 0x8000000000000000 : 0);
}
```

## File

The files themselves are a rather simple format:

```
struct {
  char magic[8];                                          // "ZBSDIFF1" or "BSDIFF40"
  bsdiff_int64_t control_block_size;
  bsdiff_int64_t diff_block_size;
  bsdiff_int64_t output_file_size;
} header;
char compressed_control_block[header.control_block_size]; // format as given in [#Control_block](https://wowdev.wiki/Patching_Files#Control_block)
char compressed_diff_block[header.diff_block_size];       // raw data
char compressed_extra_block[0];                           // to the end of the file
```

where compressed blocks are either BZ2 or zlib compressed depending on header.magic.

### Control block

While the size is given in bytes, the decompressed control block entries are always the same structure

```
struct {
  bsdiff_int64_t bytes_from_diff_block;
  bsdiff_int64_t bytes_from_extra_block;
  bsdiff_int64_t seek_in_input;
};
```

# How to patch

To patch a file, first decompress the blocks and iterate the data according to control_block:

- Copy bytes_from_diff_block data from input, bytewise += bytes from diff_block and copy to output: `o[x] = i[x] + d[x]`
- Copy bytes_from_extra_block bytes from extra_block to the output: `o[x] = e[x]`
- Seek seek_in_input in input, keep offset in output.
- Repeat.

This means that

- copying without modification: diff block filled with 0 (and rely on compression to make it small)
- copying with modification: diff block filled with bytewise diff
- addition: extra bytes
- removal: seek over removed bytes
- tuples of up to three operations are collapsed into one control blovk

  
For an implementation, consult bspatch from BSDIFF4.