_Sync'd to version from 16 September 2019._

## Getting Started

Before reading through this page, ensure you've read through the material on the loading page first:

- [WMO Format](https://wowdev.wiki/WMO "WMO")
- [WMO Loading](https://wowdev.wiki/WMO/Loading "WMO/Loading")

# Lighting Queries

Lighting for interior WMO groups is prebaked into vertex colors.

This makes it easy to apply to static geometry, but introduces some challenges when lighting things like units and game objects that may be present in a WMO.

The client includes a suite of query functions that can be used to pull lighting colors out of the prebaked vertex colors given a particular position inside a WMO.

These functions are described below.

## CMapObj::QueryLighting

In order to light entities like units, game objects, etc that exist within interior WMO groups, the game does the following:

1. Query for the closest MOPY.
2. Obtain the 3 relevant MOCV values for the MOPY.
3. Create a CImVector color by interpolating the values based on the position of the entity relative to the MOPY (ie barycentric interpolation).

This queried color value is then fed in to the standard lighting logic.

### Query with C3Segment

The following function is used to query lighting when the exact poly is not yet known. It uses a C3Segment to perform a ranged query against the BSP tree for relevant tris.

```
bool CMapObj::QueryLighting(CMapObj *this, uint32_t groupIndex, const C3Segment *seg, CImVector *color, bool *a5) {

  CMapObjGroup group = this->groupList[groupIndex];

  if (!this->unk6[16] || !(group->unk14 & 1) || group->flags & (SMOGroup::EXTERIOR | SMOGroup::EXTERIOR_LIT)) {

    return 0;

  }

  World::TriData::resultFlags = 0;
  World::TriData::nBatches = 0;
  World::TriData::nTriIndices = 0;
  World::TriData::nVertexIndices = 0;
  World::TriData::nMatrices = 0;

  float hitT = 1.0;

  // Query the BSP tree for the group to find appropriate tris

  bool triRes = CMapObjGroup::GetTris(group, seg, &hitT, 0, 0x8, (int)&a2 + 3, 0);

  if (!triRes) {

    return 0;

  }

  // Obtain point matching intersection between segment and tri

  C3Vector point;

  point.x = seg->start.x + hitT * (seg->end.x - seg->start.x);
  point.y = seg->start.y + hitT * (seg->end.y - seg->start.y);
  point.z = seg->start.z + hitT * (seg->end.z - seg->start.z);

  unsigned __int16 hitPoly = word_CD8094;

  bool lightRes = CMapObjGroup::QueryLighting(group, &point, hitPoly, color, a5);

  return lightRes;

}
```

### Query with C3Vector and poly index

The following function is used to query lighting when the relevant poly is already known.

```
bool CMapObj::QueryLighting(CMapObj *this, uint32_t groupIndex, const C3Vector *point, uint16_t polyIdx, CImVector *color, bool *a5) {

  CMapObjGroup group = this->groupList[groupIndex];

  if (!this->unk6[16] || !(group->unk14 & 1) || group->flags & (SMOGroup::EXTERIOR | SMOGroup::EXTERIOR_LIT)) {

    return 0;

  }

  // Since the point and poly are already known, there's no need to query the BSP tree

  bool lightRes = CMapObjGroup::QueryLighting(group, point, polyIdx, color, a5);

  return lightRes;

}
```

## CMapObjGroup::QueryLighting

Once a point and poly have been identified (see the other CMapObj lighting query functions), this function is used to calculate a CImVector color value.

Barycentric interpolation is used to combine the relevant vertex colors, and the CMapObj ambient color is added if the appropriate flag is set.

```
bool CMapObjGroup::QueryLighting(CMapObjGroup *this, const C3Vector *point, uint16_t polyIdx, CImVector *color, bool *a5) {

  // Poly is out of bounds

  if (polyIdx >= this->polyCount) {

    *color = this->parent->ambColor;
    *a5 = 0;

    return 1;

  }

  // Load xyAxisTable

  if (!(dword_D2DC18 & 1)) {

    dword_D2DC18 |= 1u;

    xyAxisTable[0] = { 1, 2 };
    xyAxisTable[1] = { 2, 0 };
    xyAxisTable[2] = { 0, 1 };

  }

  uint16_t* indices = &this->indexList[3 * polyIdx];

  C3Vector* vertices = this->vertexList;

  C3Vector* vert1 = &vertices[indices[0]];
  C3Vector* vert2 = &vertices[indices[1]];
  C3Vector* vert3 = &vertices[indices[2]];

  // Obtain normal for poly

  C4Plane plane;
  C4Plane::From3Pos(&plane, vert1, vert2, vert3);

  C3Vector::EAxis majAxis = C3Vector::MajorAxis(&plane.normal);

  // Obtain 2d coordinates for point and poly

  C2iVector xy = xyAxisTable[majAxis];

  C2Vector pt = { ((float *)(&point))[xy.x], ((float *)(&point))[xy.y] };
  C2Vector v1 = { ((float *)(&vert1))[xy.x], ((float *)(&vert1))[xy.y] };
  C2Vector v2 = { ((float *)(&vert2))[xy.x], ((float *)(&vert2))[xy.y] };
  C2Vector v3 = { ((float *)(&vert3))[xy.x], ((float *)(&vert3))[xy.y] };

  // Calculate barycentric weights
  // https://stackoverflow.com/a/26567573/6770172

  C2Vector sv2 = { v2.x - v1.x, v2.y - v1.y };
  C2Vector sv3 = { v3.x - v1.x, v3.y - v1.y };
  C2Vector spt = { pt.x - v1.x, pt.y - v1.y };

  // total area = cross(sub(v2, v1), sub(v3, v1))
  float at = sv2.x * sv3.y - sv2.y * sv3.x;

  // a3 = cross(sub(v2, v1), sub(pt, v1)) / total area
  float a3 = (sv2.x * spt.y - sv2.y * spt.x) / at;

  // a2 = cross(sub(pt, v1), sub(v3, v1)) / total area
  float a2 = (spt.x * sv3.y - spt.y * sv3.x) / at;

  // Calculate color weights

  int w3 = (a3 * 256.0) - 0.5;
  int w2 = (a2 * 256.0) - 0.5;
  int w1 = 256 - w3 - w2;

  // Adjust weights in cases where point is outside poly

  if (w3 < 0) {

    int o3 = (w3 * w2) / (w1 + w2);

    w2 += o3;
    w1 += w3 - o3;

    w3 = 0;

  }

  if (w2 < 0) {

    int o2 = (w2 * w3) / (w1 + w3);

    w3 += o2;
    w1 += w2 - o2;

    w2 = 0;

  }

  if (w1 < 0) {

    int o1 = (w1 * w2) / (w2 + w3);

    w2 += o1;
    w3 += w1 - o1;

    w1 = 0;

  }

  CImVector c1 = this->colorVertexList[indices[0]];
  CImVector c2 = this->colorVertexList[indices[1]];
  CImVector c3 = this->colorVertexList[indices[2]];

  // Interpolate color by weight

  color->a = (uint16_t)(w1 * c1.a + w2 * c2.a + w3 * c3.a) / 256;
  color->r = (uint16_t)(w1 * c1.r + w2 * c2.r + w3 * c3.r) / 256;
  color->g = (uint16_t)(w1 * c1.g + w2 * c2.g + w3 * c3.g) / 256;
  color->b = (uint16_t)(w1 * c1.b + w2 * c2.b + w3 * c3.b) / 256;

  // Double color RGB values -- not sure why?

  uint32_t v49 = 2 * color->r;
  uint32_t v50 = 2 * color->g;
  uint32_t v51 = 2 * color->b;

  // If MOHD.flags & 0x02, add CMapObj ambient color

  if (this->parent->header->flags & 0x2) {

    v49 += this->parent->ambColor.r;
    v50 += this->parent->ambColor.g;
    v51 += this->parent->ambColor.b;

  }

  // Clamp final color to 255

  color->r = v49 >= 0xFF ? 0xFF : v49;
  color->g = v50 >= 0xFF ? 0xFF : v50;
  color->b = v51 >= 0xFF ? 0xFF : v51;

  // MOPY.flags & 0x01 -- what is this used for?

  *a5 = this->polyList[polyIdx].flags & 0x1;

  return 1;

}
```

# Color Adjustments

## CMapObjGroup::FixColorVertexAlpha

### 3.3.5a

In 3.3.5a this function is called ONLY when MOHD flag 0x8 ("flag_do_not_fix_vertex_color_alpha") is NOT set.

```
void CMapObjGroup::FixColorVertexAlpha()
{
    int32_t intBatchStart;

    if (this->transBatchCount > 0) 
    {
        intBatchStart = this->batchList[this->transBatchCount - 1].maxIndex + 1;
    } 
    else 
    {
        intBatchStart = 0;
    }

    if (this->colorVertexCount > 0)
    {
        for (int32_t i = 0; i < this->colorVertexCount; i++) 
        {
            CImVector* color = &this->colorVertexList[i];

            // Int / ext batches
            if (i >= intBatchStart) 
            {
                int32_t v6 = (color->r + (color->a * color->r / 64)) / 2;
                int32_t v7 = (color->g + (color->a * color->g / 64)) / 2;
                int32_t v8 = (color->b + (color->a * color->b / 64)) / 2;

                v6 = v6 > 255 ? 255 : v6;
                v7 = v7 > 255 ? 255 : v7;
                v8 = v8 > 255 ? 255 : v8;

                color->r = v6;
                color->g = v7;
                color->b = v8;

                color->a = 255;
            // Trans batches
            } 
            else 
            {
                color->r /= 2;
                color->g /= 2;
                color->b /= 2;
            }
        }
    }
}
```

### Build 18179

The approach in this function is rather different from the 3.3.5a version of it The current assumption is that the client no longer suppors the classic render path, where MOHD->color was pre-baked into interior MOCV. Instead, this function subtracts MOHD color from the MOCV values, which is later added back in the lighting formula.

This function is made with the assumption that vertex color was not used in Classic / TBC in exterior groups, otherwise, the resulted render in newer clients would differ. It seems vertex colors were never used in exteriors with classic render path, yet, they have always been supported by the client.

Another assumption is made that classic render path WMOs always had MOHD flag "flag_do_not_fix_vertex_color_alpha" which is likely not true, and these models might have been patched in later versions to have it set.

After color manipulations are done, the function eventually sets MOCV.a values to 255 or 0 for exterior and interior batches correspondingly, and the trans batches alpha remains intact. This is done to allow rendering of WMO geometry in 1-2 render passes in the shader later on. The value is later used for blending between exterior and interior lighting in the shader.

```
void CMapObjGroup::FixColorVertexAlpha(CMapObjGroup *mapObjGroup)
{
  int begin_second_fixup = 0;
  if ( mapObjGroup->transBatchCount )
  {
    batch_int_start_vertex = *((unsigned __int16 *)&mapObjGroup->moba[(unsigned __int16)mapObjGroup->transBatchCount] - 2) + 1;
  }

  if ( mapObjGroup->m_mapObj->mohd->flags & flag_do_not_fix_vertex_color_alpha )
  {
    for (int i = batch_int_start_vertex; i < mapObjGroup->mocv_count; ++i)
    {
      mapObjGroup->mocv[i].w = mapObjGroup->m_groupFlags & SMOGroup::EXTERIOR ? 255 : 0;
    }
  }
  else
  {
    if ( mapObjGroup->m_mapObj->mohd->flags & flag_use_unified_render_path )
    {
      int8_t int_amb_r = 0;
      int8_t int_amb_g = 0;
      int8_t int_amb_b = 0;
    }
    else
    {
      int8_t int_amb_r = mapObjGroup->m_mapObj->mohd.color.r
      int8_t int_amb_g = mapObjGroup->m_mapObj->mohd.color.g
      int8_t int_amb_b = mapObjGroup->m_mapObj->mohd.color.b
    }

    // Trans batch vertices

    for (int mocv_index = 0; mocv_index < batch_int_start_vertex; ++mocv_index)
    {
      mapObjGroup->mocv[mocv_index].b -= int_amb_b;
      mapObjGroup->mocv[mocv_index].g -= int_amb_g;
      mapObjGroup->mocv[mocv_index].r -= int_amb_r;

      float alpha_factor = mapObjGroup->mocv[mocv_index].w / 255.0f;

      float new_b = mapObjGroup->mocv[mocv_index].b - alpha_factor * mapObjGroup->mocv[mocv_index].b;
      assert (new_b > -0.5f);
      assert (new_b < 255.5f);
      mapObjGroup->mocv[mocv_index].b = new_b / 2;

      float new_g = mapObjGroup->mocv[mocv_index].g - alpha_factor * mapObjGroup->mocv[mocv_index].g;
      assert (new_g > -0.5f);
      assert (new_g < 255.5f);
      mapObjGroup->mocv[mocv_index].g = new_g / 2;

      float new_r = mapObjGroup->mocv[mocv_index].r - alpha_factor * mapObjGroup->mocv[mocv_index].r;
      assert (new_r > -0.5f);
      assert (new_r < 255.5f);
      mapObjGroup->mocv[mocv_index++].r = new_r / 2;
    }

    // Int / Ext batch vertices

    for (int i = batch_int_start_vertex; i < mapObjGroup->mocv_count; ++i)
    {
      float new_b = (mapObjGroup->mocv[i].b * mapObjGroup->mocv[i].w) / 64 + mapObjGroup->mocv[i].b - int_amb_b;
      mapObjGroup->mocv[i].b = std::min (255, std::max (new_b / 2, 0));

      float new_g = (mapObjGroup->mocv[i].g * mapObjGroup->mocv[i].w) / 64 + mapObjGroup->mocv[i].g - int_amb_g;
      mapObjGroup->mocv[i].g = std::min (255, std::max (new_g / 2, 0));

      float new_r = (mapObjGroup->mocv[i].r * mapObjGroup->mocv[i].w) / 64 + mapObjGroup->mocv[i].r - int_amb_r;
      mapObjGroup->mocv[i].r = std::min (255, std::max (new_r / 2, 0));

      mapObjGroup->mocv[i].w = mapObjGroup->m_groupFlags & SMOGroup::EXTERIOR ? 255 : 0;
    }
  }
}
```

## CMapObj::AttenTransVerts

TODO

# Group Rendering (WotLK)

This section is applicable to Wrath of the Lich King. Cataclysm significantly changed the CMapObjGroup rendering paths.

Rendering of CMapObjGroups is handled by a pair of functions.

In Wrath of the Lich King, RenderGroup_Int handles groups with MOCV chunks present, and RenderGroup_Ext handles groups that lack the MOCV chunk.

These functions can be replaced by debug rendering functions when CMapObj::s_renderMode is set to one of the various debug rendering modes.

## Render Mode

Various debug rendering modes are available via CMapObj::s_renderMode.

|Value|CMapObj::s_renderMode|Notes|
|---|---|---|
|0|collision|SMOPoly->flags & 0x08|
|1|detail|SMOPoly->flags & 0x04|
|2|render|(SMOPoly->flags & 0x20) && !(SMOPoly->flags & 0x04)|
|3|trans|(SMOPoly->flags & 0x01) && (SMOPoly->flags & 0x04 \| 0x20)|
|4|?|?|
|5|-|Default rendering path|

## Lighting Mode

Depending on material flags, the client selects from 4 potential lighting modes.

These lighting modes control the lighting values fed into the vertex shaders.

Note that the lighting mode 3 is only used when the unified rendering path is executed.

|Value|CMapObj::s_lightingMode|ambColor|dirColor|
|---|---|---|---|
|0|unlit|vec3(0.0, 0.0, 0.0)|vec3(0.0, 0.0, 0.0)|
|1|ext lit|DNInfo->lightInfo->ambColor|DNInfo->lightInfo->dirColor|
|2|window lit|DNInfo->lightInfo->windowAmbColor|DNInfo->lightInfo->windowDirColor|
|3|int lit|CMapObj->header->ambColor|vec3(0.0, 0.0, 0.0)|

## CMapObj::RenderGroup_Int

## CMapObj::RenderGroup_Ext