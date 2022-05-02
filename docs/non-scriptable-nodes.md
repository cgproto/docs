# Non-Scriptable Nodes

## SamplerState
Since immediate sampler state is not support in glsl, you need to define a sampler state node and pass it to the automatically generated sampler input of glsl node. When the sampler input is left empty, CGProto automatically create a default sampler state with linear filter mode and clamp to edge address mode.
![](_assets/2.png)

## RenderState
Shader node accept a optional render state input. When the input is leave empty, all states are set to default value. See [MTLRenderPipelineColorAttachmentDescriptor](https://developer.apple.com/documentation/metal/mtlrenderpipelinecolorattachmentdescriptor), [MTLDepthStencilDescriptor](https://developer.apple.com/documentation/metal/mtldepthstencildescriptor/) and [MTLRenderCommandEncoder](https://developer.apple.com/documentation/metal/mtlrendercommandencoder/1516029-settrianglefillmode/) for more details. 

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

## Scalar and Vector

## Timer
## ColorPicker
## Arithmetic and Mix
Arithmetic and Mix nodes take Vector or Scalar as input and return the calculated value. When both inputs are Vector, their dimension must be equal. When one is Vector and the other is Scalar, the scalar would to implicitly converted to vector with all components set to the same value. 

## ImagePicker
## Text
## Split
Split node accpet vector or image as input. The vector could be a javascript array of numbers if array.length is between [2, 4]. When the input of a split node is image, it return multiple single channel pixel format texture according to the pixel format of the input texture. For example, a rg16Sint texture would be split into 2 r16Sint textures.
![](_assets/3.png)
## DebugPreview

