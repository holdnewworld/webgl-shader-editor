# webgl-shader-editor
Realtime editor for creating webgl shaders with debugging tools to allow for inspecting local variable definitions in a fragment shader.

[Demo](https://gkjohnson.github.io/webgl-shader-editor/dist/index.bundle.html)

![Example](/docs/example.gif)

## Goal
After lot of frustration with developing shaders and not being able to easily track the calculations within a shader, I wanted explore what the possibilities for enabling a rich shader debugger might be light while still affording the direct shader code editing.

## Features
#### Real Time Compilation and Render
As the vertex and fragment shader are updated, the render display is updated and errors are displayed as annotations.

#### Pixel Zoom
Zooming in on the image zooms in to a pixel view of the image.

#### Local Variable Value Inspection
Hovering over a pixel in the preview pane will display the values of all the local variables used for that pixel.

#### Local Variable Color Display
Every local variable will be displayed as a rendered image in the preview bar as though that variable were used to output the color for that fragment.

#### LocalStorage Saving
The vertex and fragment shader being written are saved and reloaded on refresh

## Caveats
- Because colors are stored as 4 8bit values, there is a severe loss of precision when reading out floating point values. [Issue 1](https://github.com/gkjohnson/webgl-shader-editor/issues/2), [Issue 2](https://github.com/gkjohnson/webgl-shader-editor/issues/1)

## TODO
- [ ] Add pause button for animated variables
- [ ] Texture upload
- [ ] Uniform variable edit UI
- [ ] Multi-pass shaders, stencil buffer, and screen post-effects
- [ ] Add mouse position into shader uniforms
