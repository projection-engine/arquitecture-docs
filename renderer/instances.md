## Instances

#### MeshInstance
- **WindowBuilder**
```js
{
    id, // Defaults to new UUID
    gpu, // canvas context

    vertices, // Array of vertices values; size 3
    indices, // Array of indices values; size 3
    normals, // Array of normals values; size 3
    uvs, // Array of uvs values; size 2
    tangents, // Array of tangent values; size 3

    maxBoundingBox,// Max bounding box; Vec3 (x, y, z) = [x, y, z]
    minBoundingBox, // Min bounding box; Vec3 (x, y, z) = [x, y, z]
    material // Original material ID (disabled)
}
```
- **Methods**
```js
    use() // Binds mesh VAO and VBOs
    finish() // Remove bounded VAO and VBOs  
```
- **keys**
  - verticesQuantity
  - trianglesQuantity 
  - maxBoundingBox 
  - minBoundingBox 
  - VAO
  - vertexVBO
  - indexVBO
  - normalVBO
  - uvVBO
  - tangentVBO


#### CubeMapInstance

- **WindowBuilder**
```js
(
    gpu, // Canvas context 
    resolution, // Cubemap resolution
    asDepth  // Boolean indicating that cubemap will be used for depth rendering
)
```
- **Methods**
```js
    set resolution(resolution) // Setter for cubemap shader 
    generateIrradiance(cubeBuffer, sampler=this.texture) // Generates irradiance texture and stores into the irradianceTexture key
    draw(
        callback,  // Callback called every render loop (6 times); Attributes: yaw, pitch, perspectiveMatrix, index
        cubeBuffer, // Buffer
        zFar, // Projection matrix zFar
        zNear, // Projection matrix zNear
    )
    generatePrefiltered(mipLevels = 6, resolution = 128, cubeBuffer) 
```

- **keys**
  - gpu
  - resolution
  - texture
  - prefiltered
  - irradianceTexture
  
#### MaterialInstance

- **WindowBuilder**
```js
(
    gpu, // canvas context
    vertexShader, // Vertex shader code
    shader, // Fragment shader code
    uniformData = [], // Array of objects containing uniform name/type and data
    settings = {}, // Settings object
    onCompiled = () => null, // Callback after all textures are loaded
    id, // Defaults to new UUID
    cubeMapShaderCode // Code for fragment shader for the cubemap/probe generation
)
```
- **Methods**
```js
    set cubeMapShader([fragment, vertex]) // Setter for cubemap shader 
    set shader([fragment, vertex, uniformData, onCompiled, settings]) // Setter for editor shader
    use(bind, additionalUniforms, isCubeMap) // Prepares material for render
```

- **keys**
  - ready 
  - uniformData
  - uniforms
  - id
  - settings
  - rsmAlbedo
  - hasCubeMap
  - gpu
  - uniformData
  - _shader
  - rsmAlbedo
  - cubeMapShader