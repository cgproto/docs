# Unity ShaderLab Support

## Built-in Include Files
Not all unity built-in include files are contained in CGProto. Here is the list of available files.
- HLSLSupport.cginc
- UnityCG.cginc
- UnityInstancing.cginc
- UnityLightingCommon.cginc
- UnityShaderUtilities.cginc
- UnityShaderVariables.cginc

## Commands
See [Unity doc](https://docs.unity3d.com/Manual/shader-shaderlab-commands.html) for details about command values

| Command | Supported
| ---- | ---- |
| AlphaToMask | ❌
| Blend | ✅
| BlendOp | ✅
| ColorMask | ✅
| Conservative | ❌
| Cull | ✅
| Offset | ❌
| Stencil | ✅
| ZClip | ✅
| ZTest | ✅
| ZWrite | ✅
| UsePass | ❌
| GrabPass | ❌

## Built-in shader variables
See [Unity doc](https://docs.unity3d.com/Manual/SL-UnityShaderVariables.html) for details about variable values

| Variable | Supported | |
| ---- | ---- | ---- |
| UNITY_MATRIX_MVP | ✅
| UNITY_MATRIX_MV | ✅
| UNITY_MATRIX_V | ✅
| UNITY_MATRIX_P | ✅
| UNITY_MATRIX_VP | ✅
| UNITY_MATRIX_T_MV | ✅
| UNITY_MATRIX_IT_MV | ✅
| unity_ObjectToWorld | ✅
| unity_WorldToObject | ✅
| _WorldSpaceCameraPos | ✅
| _ProjectionParams | ✅
| _ScreenParams | ✅
| _ZBufferParams | ✅
| unity_OrthoParams | ❌
| unity_CameraProjection | ✅
| unity_CameraInvProjection | ✅
| unity_CameraWorldClipPlanes | ❌
| _Time | ❌
| _SinTime | ❌
| _CosTime | ❌
| unity_DeltaTime | ❌
| _LightColor0 | ✅
| _WorldSpaceLightPos0 | ✅
| unity_WorldToLight | ❌
| unity_4LightPosZ0 | ✅
| unity_4LightPosX0<br>unity_4LightPosY0<br>unity_4LightPosZ0 | ✅
| unity_4LightAtten0 | ❌
| unity_LightColor | ✅
| unity_WorldToShadow | ❌
| unity_LightPosition | ❌
| unity_LightAtten | ❌
| unity_SpotDirection | ❌
| unity_Lightmap | ❌
| unity_LightmapST | ❌
| unity_AmbientSky | ❌
| unity_AmbientEquator | ❌
| unity_AmbientGround | ❌
| UNITY_LIGHTMODEL_AMBIENT | ✅
| unity_FogColor | ❌
| unity_FogParams | ❌
| unity_LODFade | ❌
| _TextureSampleAdd | ❌