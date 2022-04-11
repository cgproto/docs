# Built-in Shader Variables

## Transformations
|  name | type  | value
|  ----  | ----  | ---- |
| MATRIX_M | float4x4 | transform matrix which contains a translation automatically move the center of mesh to world origin and a scale resize the mesh to a bound of -1 ~ 1
| MATRIX_V | float4x4 | view matrix of the orbit camera
| MATRIX_P | float4x4 | projection matrix taking 60 as fov and apsect of the render node
| MATRIX_MV | float4x4 | MATRIX_V * MATRIX_M
| MATRIX_VP | float4x4 | MATRIX_P * MATRIX_V
| MATRIX_MVP | float4x4 | MATRIX_P * MATRIX_V * MATRIX_M
| VIEW_POSITION | float3 | camera position in world space

Because MATRIX_M and MATRIX_V doesn't contain non-uniform scale, you could simply transform normal vector by `float3 worldNormal = (MATRIX_M * float4(normal, 0.0)).xyz` or `float3 viewNormal = (MATRIX_MV * float4(normal, 0.0)).xyz`. Be aware that the multiplication order of the matrix and vector should be inversed when you are writing hlsl.

## Lighting
| name | type | value
| ---- | ---- | ---- |
| AMBIENT_COLOR | float4 | 
| LIGHT_COLORS | float4[9] | 
| LIGHT_POSITIONS | float4[9] | Directional lights: (world space direction, 0). Point lights: (world space position, 1).
| REFLECTION_MAP | texturecube\<float\> | the skybox pass to clearColor input of shader node

When writting metal shader, it is not legal to declare array of float4 as qualified function parameter. You could alternatively declare lights as device pointer or struct type.

```cpp
const device float4 *LIGHT_COLORS
const device float4 *LIGHT_POSITIONS
```

```cpp
//struct name is arbitrary
struct MyStruct {
  float4 LIGHT_COLORS[9];
  float4 LIGHT_POSITIONS[9];
};
constant MyStruct &lights
```