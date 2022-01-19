# Introduction to CGProto

CGProto is a node-based scripting editor aims to help developers rapidly prototype or learn computer graphics algorithms. It provides a sandbox that you could easily write javascript and shader languages(metal and glsl currently) and collaborate them together by connecting their inputs and outputs. Read [Quick Start](quick-start.md) to browse all node types and their functionality.

### Auto Reflection
To help you fousing on the algorithm itself, CGProto automatically [reflects](io-reflection.md) the parameters and return value of your function to node IO and handle data conversion between them. You don't need to concern about how a javascript Array is fill into a MTLBuffer and then pass to your shader uniforms.

![](_assets/0.gif ':size=70%')
![](_assets/1.gif ':size=70%')

### Data Object Conversion
Besides basic data buffer, passing image or mesh between javascript and shaders is also practicable, means that you can implement some computational geometry algorithms such as procedure mesh generation or curve intepolation in javascript and view the render result instantly. Or, in the contrast, reading pixel data from shaded gpu texture to cpu to do some non-parallelizable image analysis. Read [Data Conversions](data-conversions.md) to discover more about how data pass between javascript and shader.

![](_assets/0.png ':size=70%')

### Preview Object Control
CGProto is applicable of doing 2d and 3d rendering. In both cases, it provides a scalable view to see image output(if exists) of the active node. What is different is that,
when some inputless [3d transform matrix](built-in-shader-variables) is defined in the shader of the active node, you are able to toggle the gesture mode to simlutae an orbit camera control.

![](_assets/2.gif ':size=70%')

### Built-in Library
We try to keep your javascript dependency-free as possiable. However, it's really hard to do calculating without a 3d math library. So we did embed a javascript library named 'math3d' which you could import by calling `const math3d = require('math3d')`. This library is modified from the math module of [three.js](https://github.com/mrdoob/three.js/tree/dev/src/math). See the github repo [here](https://github.com/cgproto/math3d).

### Hiding Connections
Sometimes it's annoying to see the dizzy lines when you project get complicated. Tapping the connection visiable button to hide connection lines except those linked to the active node.

![](_assets/1.png ':align=center')

### About the examples
Several sample projects is provided in example tab to help you get involved to CGProto more quickly. We plan to supply more instructive examples in the future released of CGProto. Some of the sources are modified from open source projects and are under licensed. You should subject to the corresponding licenses when using those sources.

### Contact
If you hava any questions or suggestions about CGProto, feel free to contact us at [lorentz.0718@gmail.com](mailto:lorentz.0718@gmail.com).


