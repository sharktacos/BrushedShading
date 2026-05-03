## [Brushed Shading for Maya/MaterialX](../index_maya.md)
# Edge Mask
*ND_EdgeMask_float*

Facing ratio edge transitioning from white, into masked (with brush strokes), then to black. Use as a mix for a mix shader to add a brushed toon sheen component.

<img src="img/Maya/EdgemaskNodes.jpg" width="900" alt="menu">



## Inputs / Parameters

<img src="img/Maya/EdgemaskAttr.jpg" width="500" alt="menu">

**Strength** 

A normalized slider to control the overall effect, from zero (no effect) to 1 (100%).

**Brush Mask**

This is where you input the Triplanar brush strokes texture map, used to add brush strokes to the edge.

**Spread**

Spread the mask from the edges into the center.

