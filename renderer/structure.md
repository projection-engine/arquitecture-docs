## Structure

- **Systems**
> Systems are the rendering pipe-line it-self. They work by updating and using components present on each entity relevant to it-self. 
 
- **Entities**
> Entities are wrappers for the components, every system works with entities as the basis.
An entity will always have a `components` key holding an objects that stores the components.

- **Components**
> Components are classes that primarily store data for the systems to use. Systems usually use filters for entities with a certain component that is required for it to work,
like the `Mesh`, it is used by multiple systems that need a `MeshInstance` to work.

- **Instances**
> Instances are classes that serve data or actions to multiple systems, for example, the `FrameBufferInstance` offers an easy-to-use abstraction for frameBuffers in webgl2,
it can be used by multiple systems. `MaterialInstance` is another abstraction for shaders and textures.
