---
title: MultiStepAnimationLoop
---

MultiStepAnimationLoop
======================

This component belongs to the category of [AnimationLoop](https://www.sofa-framework.org/community/doc/main-principles/animation-loop/).

The MultiStepAnimationLoop derives from the [DefaultAnimationLoop](https://www.sofa-framework.org/community/doc/using-SOFA/components/animationloop/defaultanimationloop/). This animation loop is different due to the fact that it allows - at each iteration - for running several collision (_collisionSteps_), and within each of these collision steps, several integration sub-steps can be computes (_integrationSteps_).

<a href="https://github.com/sofa-framework/doc/blob/master/images/animationloop/MultiStepAnimationLoop.png?raw=true"><img src="https://github.com/sofa-framework/doc/blob/master/images/animationloop/MultiStepAnimationLoop.png?raw=true" title="Flow diagram for a MultiStepAnimationLoop"/></a>

Data
----

The MultiStepAnimationLoop has the following data:

- **collisionSteps**: the number of collision steps computed within one time step
- **integrationSteps**: the number of time integration (time sub-steps involving the physics resolution) computed within one time step
- **computeBoundingBox**: a boolean defining whether the global bounding box of the scene is computed at each time step. Used mostly for rendering.


Usage
-----

The MultiStepAnimationLoop has **no pre-requisite**.

Note that this MultiStepAnimationLoop does not handle constraints solved using [Lagrange multipliers](https://www.sofa-framework.org/community/doc/main-principles/constraints/lagrange-constraint/).


Example
-------

This component is used as follows in XML format:

``` xml
<MultiStepAnimationLoop collisionSteps="10" integrationSteps="2" />
```

or using SofaPython3:

``` python
node.addObject('MultiStepAnimationLoop', collisionSteps='10', integrationSteps='2')
```

An example scene involving a MultiStepAnimationLoop is available in [*examples/Component/AnimationLoop/MultiStepAnimationLoop.scn*](https://github.com/sofa-framework/sofa/blob/master/examples/Component/AnimationLoop/MultiStepAnimationLoop.scn)
<!-- automatically generated doc START -->
__Target__: Sofa.Component.AnimationLoop

__namespace__: sofa::component::animationloop

__parents__:

- BaseAnimationLoop

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
		<td>computeBoundingBox</td>
		<td>
If true, compute the global bounding box of the scene at each time step. Used mostly for rendering.
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>collisionSteps</td>
		<td>
number of collision steps between each frame rendering
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>integrationSteps</td>
		<td>
number of integration steps between each collision detection
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
|targetNode|Link to the scene's node that will be processed by the loop|BaseNode|


<!-- automatically generated doc END -->
