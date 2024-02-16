_Sync'd to version from 29 June 2023._

An M2 is rendered as a series of `M2Elements` which are constructed at runtime in `CM2SceneRender::BeginDraw()`, and sorted prior to drawing.

## Element Alpha

For a given `M2Element`, whole-element alpha is calculated by multiplying the following things together:

- `batch->color.alpha` is the `M2Batch` animated color track alpha value (if present)
- `batch->textureWeight` is the `M2Batch` animated texture weight track value (if present); if `batch->textureCount` is > 1, only the first `textureWeight` value is used
- `m2->alpha` is overall model opacity, which can be manipulated by things like distance fading and similar effects; default: `1.0`

```
element->alpha = batch->color.alpha * batch->textureWeight * m2->alpha;
```

## Element Sorting

**TODO**.

# Blending Modes

The full blending state table for can be found on the Rendering page. 

## M2Blend

In World of Warcraft, the value listed in `M2Material->blendMode` is not a direct lookup in the EGxBlend state table. The value is translated as outlined below. 

Blend modes 3 and 7 are not used by any model in 3.3.5.

| Idx | M2BLEND                | EGxBlend Idx | EGxBlend             |
| --- | ---------------------- | ------------ | -------------------- |
| 0   | `M2BLEND_OPAQUE`       | 0            | `GxBlend_Opaque`     |
| 1   | `M2BLEND_ALPHA_KEY`    | 1            | `GxBlend_AlphaKey`   |
| 2   | `M2BLEND_ALPHA`        | 2            | `GxBlend_Alpha`      |
| 3   | `M2BLEND_NO_ALPHA_ADD` | 10           | `GxBlend_NoAlphaAdd` |
| 4   | `M2BLEND_ADD`          | 3            | `GxBlend_Add`        |
| 5   | `M2BLEND_MOD`          | 4            | `GxBlend_Mod`        |
| 6   | `M2BLEND_MOD2X`        | 5            | `GxBlend_Mod2x`      |
| 7   | `M2BLEND_BlendAdd`     | 13           | `GxBlend_BlendAdd`   |

# Combiners

This enum map 1:1 against `EGxTexBlend`.

## M2COMBINER

| Idx | M2COMBINER            |
| --- | --------------------- |
| 0   | `M2COMBINER_OPAQUE`   |
| 1   | `M2COMBINER_MOD`      |
| 2   | `M2COMBINER_DECAL`    |
| 3   | `M2COMBINER_ADD`      |
| 4   | `M2COMBINER_MOD2X`    |
| 5   | `M2COMBINER_FADE`     |
| 6   | `M2COMBINER_MOD2X_NA` |
| 7   | `M2COMBINER_ADD_NA`   |
| 7   | `M2COMBINER_OP_MASK`  |
| 8   | `M2COMBINER_ENVMAP`   |

# Fog Modes

Because blending modes adjust how color is applied during a draw call, fog color often has to be modified accordingly. The client maps blending modes to fog modes using `s_fogModeList`.

`M2Material` flag `0x02` causes fog mode 0 (disabled) to always be selected, regardless of blending mode.

In certain cases (possibly when the mesh or the camera is underwater), `s_blendDisableUWFog` may force fog mode 0 (disabled) to be selected based on blending mode. As of Mists of Pandaria, it appears this applies to `Blend_Add` and `Blend_NoAlphaAdd`.

The following fog modes were taken from Mists of Pandaria (build 15662).

| Fog Mode | Action                                                                         | Blending Modes                                  |
| -------- | ------------------------------------------------------------------------------ | ----------------------------------------------- |
| 0        | Disable fog logic in shader                                                    | -                                               |
| 1        | Use fog color (without changes)                                                | `Blend_Opaque`, `Blend_AlphaKey`, `Blend_Alpha` |
| 2        | Override fog color to `0x000000` (black)                                       | `Blend_Add`, possibly: `Blend_NoAlphaAdd`       |
| 3        | Override fog color to `0xFFFFFF` (white)                                       | `Blend_Mod`                                     |
| 4        | Override fog color to `0x808080` (gray)                                        | `Blend_Mod2x`                                   |
| 5        | ? Submerged camera related; use `ViewSettings::s_fogInfo`2 or 3                | -                                               |
| 6        | ? Liquid plane related; use `ViewSettings:s_fogInfo` 3 or use `CM2Lighting`fog | -                                               |

# Lighting Modes

Similar to fog modes above, blending modes also impact lighting. The client maps blending modes to lighting modes using `s_shadedList`.

`M2Material` flag `0x01` always causes lighting mode 0 (disabled) to be selected.

The following lighting modes were taken from Mists of Pandaria (build 15662).

| Lighting Mode | Action                                                   | Blending Modes             |
| ------------- | -------------------------------------------------------- | -------------------------- |
| 0             | Disable lighting logic in shader, including local lights | `Blend_Mod`, `Blend_Mod2x` |
| 1             | Enable lighting logic in shader                          | `Blend_Opaque`, `Blend_AlphaKey`, `Blend_Alpha`, `Blend_Add`, possibly: `Blend_NoAlphaAdd`

# Alpha Testing

Alpha testing is enabled for most or all `M2Elements` being rendered. The alpha comparison function is always `D3DCMP_GREATEREQUAL`, which discards pixels with alpha values lower than the provided alphaRef.

For `Blend_AlphaKey` blending, the `alphaRef` value starts at a baseline, and is multiplied by the `M2Element->alpha`. This multiplication prevents inappropriate pixel discards during things like fades for distance culling. See the `M2Element` alpha section above for details on what can modify M2Element` `alpha.

For all other blending modes (ie `!(Blend_AlphaKey)`, the `alphaRef` value is constant.

| Blending Mode       | alphaRef                                         |
| ------------------- | ------------------------------------------------ |
| `!(Blend_AlphaKey)` | **All**: `1.0 / 255.0 (Constant)`                |
| `Blend_AlphaKey`    | **>= Cata**: `(128.0 / 255.0) * element->alpha`  |
| `Blend_AlphaKey`    | **<= WotLK**: `(244.0 / 255.0) * element->alpha` |

# Shading

## Vertex Shaders

**TODO**

# Pixel Shaders

The following pixel shaders are used to blend mesh color and textures together, prior to drawing the relevant geometry to the framebuffer.

See the [texture blending section](https://wowdev.wiki/Rendering#Texture_Blending "Rendering") on the [main rendering page](https://wowdev.wiki/Rendering "Rendering") for more information on the intent and history of the logic performed in the pixel shaders.

As with the other shaders used by the game, the M2 pixel shaders are housed within [BLS files](https://wowdev.wiki/BLS "BLS") in the shaders directory in the game data.

# Particle Emitters

| Shader Name                       | # Tex | RGB Logic                                                                 | Alpha Logic                               |
| --------------------------------- | ----- | ------------------------------------------------------------------------- | ----------------------------------------- |
| `Combiners_Add`                   | 1     | `out.rgb = in.rgb + tex0.rgb;`                                            | `out.a = in.a + tex0.a;`                  |
| `Combiners_Decal`                 | 1     | `out.rgb = mix(in.rgb, tex0.rgb, in.a);`                                  | `out.a = in.a;`                           |
| `Combiners_Fade`                  | 1     | `out.rgb = mix(tex0.rgb, in.rgb, in.a);`                                  | `out.a = in.a;`                           |
| `Combiners_Mod`                   | 1     | `out.rgb = in.rgb * tex0.rgb;`                                            | `out.a = in.a * tex0.a;`                  |
| `Combiners_Mod2x`                 | 1     | `out.rgb = in.rgb * tex0.rgb * 2.0;`                                      | `out.a = in.a * tex0.a * 2.0;`            |
| `Combiners_Opaque`                | 1     | `out.rgb = in.rgb * tex0.rgb;`                                            | `out.a = in.a;`                           |
| `Combiners_Add_Add`               | 2     | `out.rgb = (in.rgb + tex0.rgb) + tex1.rgb;`                               | `out.a = (in.a + tex0.a) + tex1.a;`       |
| `Combiners_Add_Mod`               | 2     | `out.rgb = (in.rgb + tex0.rgb) * tex1.rgb;`                               | `out.a = (in.a + tex0.a) * tex1.a;`       |
| `Combiners_Add_Mod2x`             | 2     | `out.rgb = (in.rgb + tex0.rgb) * tex1.rgb * 2.0;`                         | `out.a = (in.a + tex0.a) * tex1.a * 2.0;` |
| `Combiners_Add_Opaque`            | 2     | `out.rgb = (in.rgb + tex0.rgb) * tex1.rgb;`                               | `out.a = in.a + tex0.a;`                  |
| `Combiners_Mod_Add`               | 2     | `out.rgb = (in.rgb * tex0.rgb) + tex1.rgb;`                               | `out.a = (in.a * tex0.a) + tex1.a;`       |
| `Combiners_Mod_AddNA`             | 2     | `out.rgb = (in.rgb * tex0.rgb) + tex1.rgb;`                               | `out.a = in.a * tex0.a;`                  |
| `Combiners_Mod_Mod`               | 2     | `out.rgb = (in.rgb * tex0.rgb) * tex1.rgb;`                               | `out.a = (in.a * tex0.a) * tex1.a;`       |
| `Combiners_Mod_Mod2x`             | 2     | `out.rgb = (in.rgb * tex0.rgb) * tex1.rgb * 2.0;`                         | `out.a = (in.a * tex0.a) * tex1.a * 2.0;` |
| `Combiners_Mod_Mod2xNA`           | 2     | `out.rgb = (in.rgb * tex0.rgb) * tex1.rgb * 2.0;`                         | `out.a = in.a * tex0.a;`                  |
| `Combiners_Mod_Opaque`            | 2     | `out.rgb = (in.rgb * tex0.rgb) * tex1.rgb;`                               | `out.a = in.a * tex0.a;`                  |
| `Combiners_Mod2x_Add`             | 2     | `out.rgb = (in.rgb * tex0.rgb) * 2.0 + tex1.rgb;`                         | `out.a = tex0.a * 2.0 + tex1.a;`          |
| `Combiners_Mod2x_Mod2x`           | 2     | `out.rgb = (in.rgb * tex0.rgb) * tex1.rgb * 4.0;`                         | `out.a = tex0.a * tex1.a * 4.0;`          |
| `Combiners_Mod2x_Opaque`          | 2     | `out.rgb = (in.rgb * tex0.rgb) * tex1.rgb * 2.0;`                         | `out.a = tex0.a * 2.0;`                   |
| `Combiners_Opaque_Add`            | 2     | `out.rgb = (in.rgb * tex0.rgb) + tex1.rgb;`                               | `out.a = in.a + tex1.a;`                  |
| `Combiners_Opaque_AddAlpha`       | 2     | `out.rgb = (in.rgb * tex0.rgb) + (tex1.rgb * tex1.a);`                    | `out.a = in.a;`                           |
| `Combiners_Opaque_AddAlpha_Alpha` | 2     | `out.rgb = (in.rgb * tex0.rgb) + (tex1.rgb * tex1.a * tex0.a);`           | `out.a = in.a;`                           |
| `Combiners_Opaque_AddNA`          | 2     | `out.rgb = (in.rgb * tex0.rgb) + tex1.rgb;`                               | `out.a = in.a;`                           |
| `Combiners_Opaque_Mod`            | 2     | `out.rgb = (in.rgb * tex0.rgb) * tex1.rgb;`                               | `out.a = in.a * tex1.a;`                  |
| `Combiners_Opaque_Mod2x`          | 2     | `out.rgb = (in.rgb * tex0.rgb) * tex1.rgb * 2.0;`                         | `out.a = in.a * tex1.a * 2.0;`            |
| `Combiners_Opaque_Mod2xNA`        | 2     | `out.rgb = (in.rgb * tex0.rgb) * tex1.rgb * 2.0;`                         | `out.a = in.a;`                           |
| `Combiners_Opaque_Mod2xNA_Alpha`  | 2     | `out.rgb = (in.rgb * tex0.rgb) * mix(tex1.rgb * 2.0, vec3(1.0), tex0.a);` | `out.a = in.a;`                           |
| `Combiners_Opaque_Opaque`         | 2     | `out.rgb = (in.rgb * tex0.rgb) * tex1.rgb;`                               | `out.a = in.a;`                           |

**Table Notes**

- `tex0.rgba`, `tex1.rgba`, etc are vec4s containing sampled textures
- `in.rgba` is a vec4 containing the input color for the pixel shader, which comes from the output of the vertex shader
- `out.rgba` is a vec4 containing the result of texture blending
- `# Tex` shows the number of textures required for the given shader
- In the interest of clarity / brevity, no lighting or fogging operations are shown

## CParticleMat

CParticleMat structs are set up by the client at runtime, based on the data present in the M2Particle structs in the M2 data files.

The structure is quite simple:

```cpp
struct CParticleMat {
  uint32_t blending;

  // flags
  __int32 enableLighting : 1;
  __int32 enableFog : 1;
  __int32 enableDepthWrites : 1;
};
```

### Blending Type

`CParticleMat->blending` is set to the result of the lookup of `M2Particle->blendingType` in `s_gxBlend[]`. The value translates to a mode from `EGxBlend` (pixel blending modes).

In more recent clients, s_gxBlend[] maps 1:1 to EGxBlend. In older clients, s_gxBlend can be a bit different. [Learn more about pixel blending](https://wowdev.wiki/Rendering#Pixel_Blending "Rendering").

### Flags

`0.5.3.3368` through `3.3.5.12340`:

| Value | Flag                |
| ----- | ------------------- |
| `0x1` | `enableLighting`    |
| `0x2` | `enableFog`         |
| `0x3` | `enableDepthWrites` |

### Logic

**3.3.5a**:

```cpp
CParticleMat newMat;

newMat->enableLighting = 1;
newMat->enableFog = 1;
newMat->enableDepthWrites = 1;

EGxBlend gxBlend = s_gxBlend[m2Particle->blendingType];

newMat->blending = gxBlend;

switch (gxBlend) {
case GxBlend_Opaque:
case GxBlend_AlphaKey:
  newMat->enableDepthWrites = 1;
  break;

case GxBlend_Alpha:
case GxBlend_Mod:
case GxBlend_Mod2x:
case GxBlend_NoAlphaAdd:
  newMat->enableDepthWrites = 0;
  break;

default:
  break;
}
```