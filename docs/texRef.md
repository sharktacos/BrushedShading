# Create Texture Reference Pose

When rendering projected textures (such as triplanar or Box mapping) on animated characters, a *texture reference pose* must be created for the mesh. The projected textures are then applied to the reference pose position, and this is passed to the texture coordinates as a [Pref attribute](triPref.md). This prevents the projected texture from appearing to “slide” or “swim” across the object as it moves. 

![img](img/texRef.jpg)

Adds a Texture Reference Pose modifier to the top of the modifier stack for selected meshes, assigning a [Pref attribute](triPref.md) to the object. 

Appears in the N-Panel, Object menu, and in the Modifiers Properties tab.
