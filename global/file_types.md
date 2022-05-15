## File types

#### Mesh primitive
> .mesh

Primitive file, stores mesh information like vertices and normals in a JSON format.

#### Node wrapper 
> .nwrap

Node wrap file stores the node name and reference to all its child node registry id in a JSON format.

#### Mesh wrapper
> .mwrap

Mesh wrap file stores the mesh name and reference to all its child primitive registry id in a JSON format.

#### Script 
> .flow

Script object, stores in a JSON format the script nodes, links comments and compiled JS code.

#### Raw script 
> .flowRaw

Raw script, stores javascript class without export.

#### Material
> .material

Material object, stores in a JSON format the material nodes, links and the compiled result (shaders, images, uniforms, etc...)
#### Image 
> .pimg

Image asset, stores base64 data of image.

#### Registry
> .reg

Registry file always located at `projectsFolder/projectID/assetsRegistry`, stores the file absolute path and ID in the JSON format.



#### Scene
> .scene

Stores scene relationships with Nodes.

