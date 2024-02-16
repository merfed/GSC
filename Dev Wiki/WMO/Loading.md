_Sync'd to version from 16 November 2017._

As is frequently the case with Blizzard's various model formats, depending on format versions and flags, some WMO data can be modified when it is read from disk.

When implementing a renderer, these load-time manipulations are important to understand and recreate to ensure correct rendering.

This page attempts to catalog known manipulations that happen prior to rendering.

# Color Adjustments

## CMapObjGroup::FixColorVertexAlpha

When loading a CMapObjGroup, if SMOHeader->flags 0x8 is **not** set, a vertex color adjustment routine called FixColorVertexAlpha is run against all vertex colors present in colorVertexList.

```
if ((this->parent->header->flags & 0x8) == 0) {
  CMapObjGroup::FixColorVertexAlpha(this);
}

The logic is taken from build 3.3.5.12340. Later versions of the function may involve SMOHeader->ambColor and slightly different logic.

void CMapObjGroup::FixColorVertexAlpha(CMapObjGroup *this) {
  int firstNonTransIndex;

  if (this->transBatchCount > 0) {
    firstNonTransIndex = this->batchList[this->transBatchCount - 1]->maxIndex + 1;
  } else {
    firstNonTransIndex = 0;
  }

  if (this->colorVertexCount) {
    for (int i = 0; i < this->colorVertexCount; i++) {
      CImVector *color = &this->colorVertexList[i];

      // Adjust color in int or ext batch
      if (i >= firstNonTransIndex) {
        uint32_t r = (color->r + (((uint32_t)color->a * color->r) / 64)) / 2;
        uint32_t g = (color->g + (((uint32_t)color->a * color->g) / 64)) / 2;
        uint32_t b = (color->b + (((uint32_t)color->a * color->b) / 64)) / 2;

        color->r = r > 255 ? 255 : r;
        color->g = g > 255 ? 255 : g;
        color->b = b > 255 ? 255 : b;

        color->a = 255;
      // Adjust color in trans batch
      } else {
        color->r /= 2;
        color->g /= 2;
        color->b /= 2;
      }
    }
  }
}
```