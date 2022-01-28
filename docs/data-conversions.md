# Data Conversions

## Data Buffer

## Image

|  field | type  | available value | optional |default value
|  ----  | ----  | ---- | ---- | ---- |
| pixelFormat  | String | a8Unorm<br><br>r8Unorm\|r8Uint\|r8Snorm\|r8Sint<br>r16Unorm\|r16Uint\|r16Snorm\|r16Sint\|r16Float<br>r32Uint\|r32Sint\|r32Float<br><br>rg8Unorm\|rg8Uint\|rg8Snorm\|rg8Sint<br>rg16Unorm\|rg16Uint\|rg16Snorm\|rg16Sint\|rg16Float<br>rg32Uint\|rg32Sint\|rg32Float<br><br>rgba8Unorm\|rgba8Uint\|rgba8Snorm\|rgba8Sint<br>rgba16Unorm\|rgba16Uint\|rgba16Snorm\|rgba16Sint\|rgba16Float<br>rgba32Uint\|rgba32Sint\|rgba32Float | false |
| dimension  | Integer | 1\|2\|3 | true | 2
| width | Integer | [1, 4096] | false | 
| height | Integer |[1, 4096] | true if dimension < 2 | 1
| depth | Integer | [1, 4096]| true if dimension < 3 | 1
| data | Array of Number\|TypedArray | | false


## Mesh

|  field | type  | available value | optional |default value
|  ----  | ----  | ---- | ---- | ---- |
| geometryType  | String | points<br>lines<br>triangles<br>triangleStrips<br>quads | false | 
| indices  | Uint8Array<br>Uint16Array<br>Uint32Array<br>Array |  | true |
| indexBitDepth | Integer | 8\|16\|32 | true | 32
| attributes | Array of Object |  | false |


## Attribute

|  field | type  | available value |
|  ----  | ----  | ---- |
| name | String |
| format | String | uchar\|uchar2\|uchar3\|uchar4<br><br>ucharNorm\|ucharNorm2\|ucharNorm3\|ucharNorm4<br><br>char\|char2\|char3\|char4<br><br>charNorm\|charNorm2\|charNorm3\|charNorm4<br><br>ushort\|ushort2\|ushort3\|ushort4<br><br>ushortNorm\|ushortNorm2\|ushortNorm3\|ushortNorm4<br><br>short\|short2\|short3\|short4<br><br>shortNorm\|shortNorm2\|shortNorm3\|shortNorm4<br><br>uint\|uint2\|uint3\|uint4<br><br>int\|int2\|int3\|int4<br><br>half\|half2\|half3\|half4<br><br>float\|float2\|float3\|float4
| data | Array of Number\|TypedArray | 