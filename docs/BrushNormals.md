#Brushed Normals

#Inputs

*Strength* 
  A normalized slider to control the overall effect, from zero (no effect) to 1 (100%).


Brush Strokes: This is where you input the brush strokes map. I’ll come back and talk about this in more detail later, but this is the hand painted brushstoke map that is used to smear an object’s shading normals along the brush strokes. I provide several example brush stroke maps for you to play with, including oil paint, gouache, water color, pencil, pastel, pallet knife, and my favorite hairy brush. You can also create your own brush stroke maps. A great program for this is Rebelle. 

Gain: Is a modifier for the brush strokes map, acting a multiplier, where a value of 1 does nothing, and value above 1 brighten the map, while values below 1 darken it. This allows you to tweek the map. We will see examples of this later on of this in action when I demo the example scene.

Roll: The roll rotates the world normals based on a "paint-roller" effect. Effectively smearing the object’s shading normals along the brush strokes. [show slider’s effect]. 

Notice how the BrushedNormals  is input into the normals channel of our material, to give us our brushed shading. Let’s take a look at what it is doing to the normals. [connect and show roll]

The initial direction the "roller" travels is from the top of the screen downwards. 

Rotation: The direction can be changed with the rotation parameter which rotates clockwise in degrees. So putting in 45 will rotate clockwise 45 degrees, and -45 will rotate counter clockwise 45 degrees.

Dir Light Rotations: You can also connect the rotation values of a sun light into the Dir Light Rotations so that the brush shading direction follows the light direction. To link your light’s values right-click the light rotation and “copy data path”. Then right-click the NormalRoll and “add driver” (turns purple). 

Input as radians: These values are passed by Blender as radians, rather than degrees, which is what the “input radians” check box is for. If you instead want to manually enter the rotations in degrees, you can simply uncheck this. The light’s rotations in world space are converted into screen space, determining the starting direction angle, and the rotation slider becomes an additional tool to tweek that angle. 
