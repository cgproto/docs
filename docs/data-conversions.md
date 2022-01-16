# Data Conversions

## Data Buffer

## Image

|  field | type  | available value | optional |default value
|  ----  | ----  | ---- | ---- | ---- |
| pixelFormat  | String | a8Unorm\|r8Unorm\|r8Uint\|r8Snorm | false |
| dimension  | Integer | 1\|2\|3 | true | 2
| width | Integer | [1, 4096] | false | 
| height | Integer |[1, 4096] | true if dimension < 2 | 1
| depth | Integer | [1, 4096]| true if dimension < 3 | 1
| data | TypedArray | | false


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
| format | String | float\|float2\|float3\|float4
| data | Array of Number<br>TypedArray | 