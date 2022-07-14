## Scripts execution

The parsing occurs on the start of the renderer, it will take the code string and generate a class instance.

All javascript code that needs to be executed in the Scripting needs one entry point,
that being the `execute` method, this method will receive the required attributes to perform any operation.
These are the following attributes:
```js
{
    elapsed, // Elapsed time
    entities, // Entities hash map ({[entityID]: entityRef})
    renderTarget, // DOM render target
    pressedKeys, // Currently pressed keys (example: {KeyA: true})
    KEYS, // Hash map referencing the JS events for keys (example: {KeyA: "KeyA"})
    mousePosition, // Current mouse position {x, y}
    camera, // RootCameraInstance instance 
    glMatrix, // all glMatrix libs
    COMPONENTS // components names for accessing the components inside an entity.
}
```

The `COMPONENTS` object:
```js
 {
    TRANSFORM,
    CUBE_MAP,
    COLLIDER,
    DIRECTIONAL_LIGHT,
    POINT_LIGHT,
    PICK,
    SPOT_LIGHT,
    FOLDER,
    MATERIAL,
    MESH,
    PHYSICS,
    SKYBOX,
    TERRAIN,
    SKYLIGHT,
    SCRIPT,
    CAMERA
}
```

