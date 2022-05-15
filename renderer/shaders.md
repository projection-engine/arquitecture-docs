## Shaders 
> Singular float/int/bool/vec3/vec4 uniforms are usually grouped together into matrices to reduce the number of API calls. 

- Point lights

```
// [
//    positionX,    positionY,    positionZ,    0
//    colorR,       colorG,       colorB,       0
//    attenuationX, attenuationY, attenuationZ, 0
//    zFar,         zNear,        hasShadowMap, 0
// ] = mat4
```

- Directional lights
```
// [
//    directionX, directionY, directionZ
//    colorR,     colorG,     colorB
//    atlasX,     atlasY,     hasShadowMap
// ] = mat3
```

- Shader Settings
```
// [
//     dirLightQuantity,   shadowMapResolution, indirectLightAttenuation, pcfSamples, 
//     gridSize,           noGI,                lightQuantity,            0
//     noShadowProcessing, shadowMapsQuantity,  hasAO,                    0
// ] 
```

- AO settings
```
// [
//     total_strength, base,   area,
//     falloff,        radius, samples,
//     0,              0,      0
// ] 
```