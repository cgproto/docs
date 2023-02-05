# ChangeLogs

## 2.9

* support [adding third-party library](README?id=importing-custom-library) by git
* support referencing custom shader header in glsl and hlsl with #include syntax

## 2.8

* fix crash when logging with the logger view hidden on iOS16

## 2.7

* add DeepLabV3 example

## 2.6

* support import coreml model(.mlmodel, .mlpackage)
* add [numjs](https://github.com/cgproto/numjs/tree/cgproto) built-in javascript library
* add facial landmarks detection example

## 2.5

* support clone project from git
* add json node
* add catmull-clark example

## 2.4

* support remote coding on desktop by using the [CGProto VSCode extension](vscode-extension)
* Javascript mesh supports defining [submeshes](data-conversions?id=submesh)
* model assetes imported from document browser could be passed to Javascript node

## 2.3

* add [arkit face tracking node](non-scriptable-nodes?id=FaceTrackingAR)

## 2.2

* add [touch node](touch-api)
* add painting example

## 2.1

* support import audio from document browser
* add 2 audio visualization examples
* support [set mesh bounding box](data-conversions?id=mesh) explicitly in javascript
* change the address mode of default texture sampler from repeat to clampToEdge

## 2.0

* support camera capture node(Add Node Menu > Texture > Camera)
* add realtime camera filter example

## 1.9

* support import project(.zip), javascript file(.js), 3d model(.obj, .usdz) or image from document browser

## 1.8

* [add background texture or skybox support](shader-nodes?id=the-clearcolor-input)
* add environment map reflection example
* fix inappropriate keyboard type in mobile device