# Introduction to CGProto

CGProto is a node-based scripting editor aims to help developers rapidly prototype or learn computer graphics algorithms. It provides a sandbox that you could easily write shader(GLSL, HLSL, Metal or even Unity ShaderLab) and javascript to make impressive CG effects.

## Auto IO Reflection
To help you fousing on the algorithm itself, CGProto automatically reflects the parameters and return value of your function to node IO and handle data conversion between them. You don't need to concern about how a javascript Array is fill into a MTLBuffer and then pass to your shader uniforms.

![](_assets/0.gif ':size=70%')
![](_assets/1.gif ':size=70%')

## Data Object Conversion
Besides basic data buffer, passing image or mesh between javascript and shaders is also practicable, which means that you can implement some computational geometry algorithms such as procedure mesh generation or curve intepolation in javascript and view the render result instantly, or vice versa, reading pixel data from shaded gpu texture to cpu to do some non-parallelizable image analysis. Read [JS Data Conversions](data-conversions.md) to discover more about how data pass between javascript and shader.

![](_assets/0.png ':size=70%')

## Preview Object Control
CGProto is applicable of doing 2d and 3d rendering. In both cases, it provides a scalable view to see image output(if exists) of the active node. What is different is that, when some [3d transform matrix](built-in-shader-variables) is defined in the shader of the active node, you are able to toggle the gesture mode to simluate an orbit camera control.

![](_assets/2.gif ':size=70%')

## Hiding Connections
Sometimes it's annoying to see the dizzy lines when you project get complicated. Tapping the connection visiable button to hide connection lines except those linked to the active node.

![](_assets/1.png ':align=center')

## Exporting and Importing Projects
Project files are organized as zip package when importing and exporting. Long press the project cover and tap the Share button to export the project. You are able to view all source files and assets after unzipping the package. To re-import the project you should zip the root project folder, send it to your device via airdrop or email or any other tools that can transfer files to mobile device, then select open with CGProto. After that the project should be in your workspace. From version over 2.0, projects could be imported from document browser via the import button in the right top bar of the root view.

## About the Examples
Several sample projects is provided in example tab to help you get involved to CGProto more quickly. We plan to supply more instructive examples in the future released of CGProto. Some of the sources are modified from open source projects and are under licensed. You should subject to the corresponding licenses when using those sources.

## Contact
If you hava any questions or suggestions about CGProto, feel free to contact us at
- Email: [lorentz.0718@gmail.com](mailto:lorentz.0718@gmail.com).
- Twitter: https://twitter.com/lorentz_albert
- Youtube: https://www.youtube.com/channel/UCD-V2juCR5FWXyCS7kDHsng
- Bilibili: https://space.bilibili.com/475328712



