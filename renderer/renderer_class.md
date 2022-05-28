## Renderer

<img src="https://github.com/projection-engine/engine/blob/v0.1.x-alpha/flow.jpg?raw=true" alt="Editor material"/>

- **start**
> Starts the render loop and stores the current frame inside the `_currentFrame` variable.
- **stop**
> Stops the render loop by canceling the current frame.
- **updatePackage**
> Receives the data required to initialize the rendering loop and structures it inside 4 objects, those being:
> - **systems**: Private variable holding the systems structure by their respective execution order.
> - **data**: Object holding filtered entities relevant to the systems (like lights, meshes, cubemaps and etc..), it also holds the hashMap for all mesh instances and material instances
> - **params**: Object holding rendering settings, camera information and callbacks

