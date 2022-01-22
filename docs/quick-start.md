# Quick Start

### Javascript


### MetalRender
A single draw pass with configurable render size, clear color, geometry mesh, render state and vertex and fragment shaders written in Metal shading language. The default value of clear color is [0.5, 0.5, 0.5, 1.0]. 

### GLSLRender
Same as MetalRender node but written in OpenGL shading language. Actually all glsl would be translated to metal by [glslang](https://github.com/KhronosGroup/glslang) and [SPIRV-Cross](https://github.com/KhronosGroup/SPIRV-Cross) before building the render pipeline.

### SamplerState
Since immediate sampler state is not support in glsl, you need to define a sampler state node and pass it to the automatically generated sampler input of glsl node. 
![](_assets/2.png)

### RenderState
Each render pass accept a optional render state input. When the input is leave empty, all states are set to default value. See for [MTLRenderPipelineColorAttachmentDescriptor](https://developer.apple.com/documentation/metal/mtlrenderpipelinecolorattachmentdescriptor), [MTLDepthStencilDescriptor](https://developer.apple.com/documentation/metal/mtldepthstencildescriptor/) and [MTLRenderCommandEncoder](https://developer.apple.com/documentation/metal/mtlrendercommandencoder/1516029-settrianglefillmode/) for more details. 

|  state | default value
| ---- | ---- |
| wire frame mode | false
| enable blend | false
| rgb blend operation | add
| alpha blend operation | add
| src rgb blend factor | one
| src alpha blend factor | one
| dst rgb blend factor | zero
| dst alpha blend factor | zero
| enable depth write | false
| depth compare function | always

### Scalar and Vector

### Timer
### ColorPicker
### Arithmetic and Mix
Arithmetic and Mix nodes take Vector or Scalar as input and return the calculated value. When both inputs are Vector, their dimension must be equal. When one is Vector and the other is Scalar, the scalar would to implicitly converted to vector with all components set to the value. 
### ImagePicker
### Text
### Split
Split node accpet vector or image as input. The vector could be a javascript array of numbers if array.length is between [2, 4]. When the input of a split node is image, it return multiple single channel pixel format texture according to the pixel format of the input texture. For example, a rg16Sint texture would be split into 2 r16Sint textures.
![](_assets/3.png)
### DebugPreview

