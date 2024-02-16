> [!Note] This section only applies to versions ≥ <span class="cata">Cata</span>

This is storing bounding boxes for all models (m2). It was added in Cataclysm to help with streaming data.

# MBVR

```cpp
uint32_t version;    // even though format has changed, this is still 0 in Legion
```

# MBB

```cpp
struct {
    #if < Legion
        uint32_t filenameOffset;    // into MBFN chunk
    #else
        uint32_t fileDataId;
    #endif
        CAaBox boundingBox;         // collision bounding box
} entries[];
```

# MBFN

> [!Note] This section only applies to versions < <span class="legion">Legion</span>

```cpp
char filenames[];    // zero-terminated, no file extensions
```