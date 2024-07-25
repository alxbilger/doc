---
title: FreeMotionAnimationLoop
---

FreeMotionAnimationLoop
=======================

This component belongs to the category of [AnimationLoop](https://www.sofa-framework.org/community/doc/main-principles/animation-loop/).

The FreeMotionAnimationLoop is the component that rules the simulation in two main steps: a free motion, then a correction step. First, the free motion computes the projective constraints, the physics, solving the resulting free linear system. Second, the correction step solves the constraints based on the Lagrange multipliers. More information on the constraint resolution can be found [here](https://www.sofa-framework.org/community/doc/main-principles/constraints/lagrange-constraint/).

<a href="https://github.com/sofa-framework/doc/blob/master/images/animationloop/FreeMotionAnimationLoop.png?raw=true"><img src="https://github.com/sofa-framework/doc/blob/master/images/animationloop/FreeMotionAnimationLoop.png?raw=true" title="Flow diagram for a FreeMotionAnimationLoop"/></a>

Data
----

The DefaultAnimationLoop has one data:

- **computeBoundingBox**: a boolean defining whether the global bounding box of the scene is computed at each time step. Used mostly for rendering.


Usage
-----

The FreeMotionAnimationLoop must be used specifically for constraint resolution based on the Lagrange multiplier. It therefore **requires**:

- a [ConstraintSolver](https://www.sofa-framework.org/community/doc/main-principles/constraints/lagrange-constraint/#constraintsolver-in-sofa). If no constraint solver can be found, a LCPConstraintSolver is automatically created by default.

Note that one or multiple [ConstraintCorrection](https://www.sofa-framework.org/community/doc/main-principles/constraints/lagrange-constraint/#constraintcorrection) may be required by the [ConstraintSolver](https://www.sofa-framework.org/community/doc/main-principles/constraints/lagrange-constraint/#constraintsolver-in-sofa).


Example
-------

This component is used as follows in XML format:

``` xml
<FreeMotionAnimationLoop />
```

or using SofaPython3:

``` python
node.addObject('FreeMotionAnimationLoop')
```

An example scene involving a FreeAnimationLoop is available in [*examples/Component/AnimationLoop/FreeMotionAnimationLoop.scn*](https://github.com/sofa-framework/sofa/blob/master/examples/Component/AnimationLoop/FreeMotionAnimationLoop.scn)
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
		<td>solveVelocityConstraintFirst</td>
		<td>
solve separately velocity constraint violations before position constraint violations
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>threadSafeVisitor</td>
		<td>
If true, do not use realloc and free visitors in fwdInteractionForceField.
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Multithreading</td>
	</tr>
	<tr>
		<td>parallelCollisionDetectionAndFreeMotion</td>
		<td>
If true, executes free motion step and collision detection step in parallel.
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>parallelODESolving</td>
		<td>
If true, solves all the ODEs in parallel during the free motion step.
		</td>
		<td>0</td>
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
|constraintSolver|The ConstraintSolver used in this animation loop (required)|ConstraintSolver|


<!-- automatically generated doc END -->
