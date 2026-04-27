.
# Toon Principled (Arnold)

Based on OpenPBR, but designed for NPR rendering.  

![img](img/Maya/toonPrincipledAttr2.jpg)

## Inputs / Parameters

**Base Weight**

Scalar multiplier for Base Color

**Base Color**

Overall color of the material used for diffuse and metal.

**Base Flatten**

Controls how flat the diffuse shading is by blending between smooth shading normals (using EON diffuse roughness), and brushed normals.

**Metalness**

A mix between dielectric shading and toon metallic. Uses two specular lobes, one tinted with the base color, to get a stylized metallic look. 

**Metal Roughness**

Roughness of the metal specular lobe.

**Toon Spec** 

Toggle between toon specular (Toon Glossy BSDF), and microfacet GGX specular. 

**Specular Size**

Gives an angle of reflection between 0° and 45°.

**Specular Weight**

Scalar multiplier for Specular Color.

**Specular Color**

Color tint for specular highlight.

**Specular Roughness**

Specifies the roughness of the surface for specular reflection. When Toon Spec is enabled, this controls the toon glossy smoothness. That is, it specifies an angle over which a smooth transition from full to no reflection happens.

**IOR**

Index of refraction for the GGX spec. Defaults to a physically implausible value of 2.0, since we are doing non-physically based rendering (NPR), producing a broader specular highlight. 

**Normal**

Controls the normals of the base layers.

**Spec Normal Strength** 

Controls the amount that the specular is affected by the normal. 

**Emission Weight**

Scalar multiplier for Emission Color.

**Emission Color**

Light emission from the surface.

**Alpha** 

Controls the opacity of the surface. Usually linked to the Alpha output of an Image Texture node.

**Transmission Weight**

Enables stylized glass, which is a mix between refraction at glancing angles and transparency. This allows for stylized glass where indirect reflections and global illumination are disabled for NPR lighting. That is, where the max light bounce is set to zero for diffuse and glossy. 

With both diffuse and glossy rays at zero (0) the glass will appear darkened. Enabling diffuse rays removes the darkening. Enabling glossy rays produces lighter glass.

**Transmission IOR**

Index of refraction for transmission.

## Example material node network

![img](img/network_toon.jpg)
