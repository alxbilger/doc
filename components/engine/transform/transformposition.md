---
title: TransformPosition
---

TransformPosition
===============

This component belongs to the category of [Engines](https://www.sofa-framework.org/community/doc/simulation-principles/engine/). The TransformPosition engine transforms the positions of one DataFields into new positions after applying a transformation. This transformation can be either:

-   Projection on a plane (plane defined by an origin and a normal vector)
-   Translation, rotation, scale and some combinations of translation rotation and scale


Input Data
----------

-   **input\_position**: input array of 3d points.

Output Data
----------

-   **output\_position**: output array of 3d points projected on a plane.

Additional parameters
---------------------

-   **method**: transformation method either translation or scale or rotation or projectOnPlane.

Examples
---------

An example scene involving the TransformPosition engine is available in [*examples/Component/Engine/Transform/TransformPosition.scn*](https://github.com/sofa-framework/sofa/blob/master/examples/Component/Engine/Transform/TransformPosition.scn)
<!-- automatically generated doc START -->
__Target__: Sofa.Component.Engine.Transform

__namespace__: sofa::component::engine::transform

__parents__:

- DataEngine

Data: 

<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
            <th>Default value</th>
        </tr>
    </thead>
    <tbody>
	<tr>
		<td>name</td>
		<td>
object name
		</td>
		<td>unnamed</td>
	</tr>
	<tr>
		<td>printLog</td>
		<td>
if true, emits extra messages at runtime.
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>tags</td>
		<td>
list of the subsets the objet belongs to
		</td>
		<td></td>
	</tr>
	<tr>
		<td>bbox</td>
		<td>
this object bounding box
		</td>
		<td></td>
	</tr>
	<tr>
		<td>componentState</td>
		<td>
The state of the component among (Dirty, Valid, Undefined, Loading, Invalid).
		</td>
		<td>Undefined</td>
	</tr>
	<tr>
		<td>listening</td>
		<td>
if true, handle the events, otherwise ignore the events
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>method</td>
		<td>
transformation method either translation or scale or rotation or random or projectOnPlane
		</td>
		<td></td>
	</tr>
	<tr>
		<td>seedValue</td>
		<td>
the seed value for the random generator
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>maxRandomDisplacement</td>
		<td>
the maximum displacement around initial position for the random transformation
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>filename</td>
		<td>
filename of an affine matrix. Supported extensions are: .trm, .tfm, .xfm and .txt(read as .xfm)
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Inputs</td>
	</tr>
	<tr>
		<td>origin</td>
		<td>
A 3d point on the plane/Center of the scale
		</td>
		<td></td>
	</tr>
	<tr>
		<td>input_position</td>
		<td>
input array of 3d points
		</td>
		<td></td>
	</tr>
	<tr>
		<td>normal</td>
		<td>
plane normal
		</td>
		<td></td>
	</tr>
	<tr>
		<td>translation</td>
		<td>
translation vector 
		</td>
		<td></td>
	</tr>
	<tr>
		<td>rotation</td>
		<td>
rotation vector 
		</td>
		<td></td>
	</tr>
	<tr>
		<td>scale</td>
		<td>
scale factor
		</td>
		<td>1 1 1</td>
	</tr>
	<tr>
		<td>matrix</td>
		<td>
4x4 affine matrix
		</td>
		<td>[1 0 0 0,0 1 0 0,0 0 1 0,0 0 0 1]</td>
	</tr>
	<tr>
		<td>fixedIndices</td>
		<td>
Indices of the entries that are not transformed
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Outputs</td>
	</tr>
	<tr>
		<td>output_position</td>
		<td>
output array of 3d points projected on a plane
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>drawInput</td>
		<td>
Draw input points
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawOutput</td>
		<td>
Draw output points
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>pointSize</td>
		<td>
Point size
		</td>
		<td>1</td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|


<!-- automatically generated doc END -->
