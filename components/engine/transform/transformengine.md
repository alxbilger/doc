---
title: TransformEngine
---

TransformEngine
===============

This component belongs to the category of [Engines](https://www.sofa-framework.org/community/doc/simulation-principles/engine/). The TransformEngine transforms the positions of one DataFields into new positions after applying a transformation. This transformation can be either: translation, rotation or scale.

Input Data
----------

- **input\_position**: input array of 3d points
Output Data
----------

- **output\_position**: output array of 3d points

Additional Parameter
--------------------

- **translation**: Vector3 defining the translation to be applied
- **rotation**: Vector3 defining the rotation to be applied
- **scale**: Vector3 describing the scale to be applied

Examples
--------

This component is used as follows in XML format:

``` xml
<TransformEngine name="translationEngine" template="Vec3d" translation="10 0 0" input_position="@meshLoader.position" />
<MechanicalObject name="transform" template="Vec3d" position="@translationEngine.output_position" />
```

or in python:

``` python
node.addObject("TransformEngine", name="translationEngine", template="Vec3d", translation="10 0 0", input_position="@meshLoader.position")
node.addObject("MechanicalObject", name="transform", template="Vec3d", position="@translationEngine.output_position")
```


An example scene involving the TransformEngine engine is available in [*examples/Component/Engine/Transform/TransformEngine.scn*](https://github.com/sofa-framework/sofa/blob/master/examples/Component/Engine/Transform/TransformEngine.scn)
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
		<td colspan="3">Inputs</td>
	</tr>
	<tr>
		<td>input_position</td>
		<td>
input array of 3d points
		</td>
		<td></td>
	</tr>
	<tr>
		<td>translation</td>
		<td>
translation vector (x,y,z)
		</td>
		<td>0 0 0</td>
	</tr>
	<tr>
		<td>rotation</td>
		<td>
rotation vector (x,y,z)
		</td>
		<td>0 0 0</td>
	</tr>
	<tr>
		<td>quaternion</td>
		<td>
rotation quaternion (qx,qy,qz,qw)
		</td>
		<td>0 0 0 1</td>
	</tr>
	<tr>
		<td>scale</td>
		<td>
scale factor
		</td>
		<td>1 1 1</td>
	</tr>
	<tr>
		<td>inverse</td>
		<td>
true to apply inverse transformation
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Outputs</td>
	</tr>
	<tr>
		<td>output_position</td>
		<td>
output array of 3d points
		</td>
		<td></td>
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
