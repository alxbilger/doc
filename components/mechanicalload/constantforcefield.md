---
title: ConstantForceField
---

ConstantForceField
==================

This component belongs to the category of [ForceField](https://www.sofa-framework.org/community/doc/simulation-principles/multi-model-representation/forcefield/). The ConstantForceField is a simple force field applying the same constant force on each node. This force field is not integrated over the domain of our object, but simply distributed over the number of nodes.


<a href="https://github.com/sofa-framework/doc/blob/master/images/FEM/ConstantForceField.png?raw=true"><img src="https://github.com/sofa-framework/doc/blob/master/images/FEM/ConstantForceField.png?raw=true" title="Nodal constant force over a liver mesh" style="width: 50%;text-align: center; "/></a>



Data  
----

- **indices**: list of node indices where the forces are applied and distributed
- **force**: single value corresponding to the constant force applied on each node
- **totalForce**: single value corresponding to total force for all points, i.e. the sum of the forces distributed uniformly over the nodes
- **forces**: vector containing the force amplitude applied at each node


Usage
-----

As a Forcefield, the ConstantForceField requires a **MechanicalObject** and the associated **solvers** (integration scheme and linear solver), as well as a **PointSetTopologyContainer**.


Example
-------

This component is used as follows in XML format:

``` xml
<ConstantForceField indices="0 1 2" forces="-1 -1 0   1 -1 0   1 1 0" />
```

or using SofaPython3:

``` python
node.addObject('ConstantForceField', indices=[0 1 2], forces=[[-1 -1 0] [1 -1 0] [1 1 0]])
```

With a description of each data

An example scene involving a ConstantForceField is available in [*examples/Component/MechanicalLoad/ConstantForceField.scn*](https://github.com/sofa-framework/sofa/blob/master/examples/Component/MechanicalLoad/ConstantForceField.scn)
<!-- automatically generated doc START -->
__Target__: Sofa.Component.MechanicalLoad

__namespace__: sofa::component::mechanicalload

__parents__:

- ForceField

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
		<td>rayleighStiffness</td>
		<td>
Rayleigh damping - stiffness matrix coefficient
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>indices</td>
		<td>
indices where the forces are applied
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indexFromEnd</td>
		<td>
Concerned DOFs indices are numbered from the end of the MState DOFs vector. (default=false)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Force info</td>
	</tr>
	<tr>
		<td>forces</td>
		<td>
vector containing the force amplitude applied at each node
		</td>
		<td></td>
	</tr>
	<tr>
		<td>totalForce</td>
		<td>
total force for all points, will be distributed uniformly over points
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>showArrowSize</td>
		<td>
Size of the drawn arrows (0->no arrows, sign->direction of drawing. (default=0)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>showColor</td>
		<td>
Color for object display (default: [0.2,0.9,0.3,1.0])
		</td>
		<td>0.2 0.9 0.3 1</td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|mstate|MechanicalState used by this component|MechanicalState<Rigid2d>|
|topology|link to the topology container|BaseMeshTopology|

- Rigid3d

__Target__: Sofa.Component.MechanicalLoad

__namespace__: sofa::component::mechanicalload

__parents__:

- ForceField

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
		<td>rayleighStiffness</td>
		<td>
Rayleigh damping - stiffness matrix coefficient
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>indices</td>
		<td>
indices where the forces are applied
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indexFromEnd</td>
		<td>
Concerned DOFs indices are numbered from the end of the MState DOFs vector. (default=false)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Force info</td>
	</tr>
	<tr>
		<td>forces</td>
		<td>
vector containing the force amplitude applied at each node
		</td>
		<td></td>
	</tr>
	<tr>
		<td>totalForce</td>
		<td>
total force for all points, will be distributed uniformly over points
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>showArrowSize</td>
		<td>
Size of the drawn arrows (0->no arrows, sign->direction of drawing. (default=0)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>showColor</td>
		<td>
Color for object display (default: [0.2,0.9,0.3,1.0])
		</td>
		<td>0.2 0.9 0.3 1</td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|mstate|MechanicalState used by this component|MechanicalState<Rigid3d>|
|topology|link to the topology container|BaseMeshTopology|

- Vec1d

__Target__: Sofa.Component.MechanicalLoad

__namespace__: sofa::component::mechanicalload

__parents__:

- ForceField

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
		<td>rayleighStiffness</td>
		<td>
Rayleigh damping - stiffness matrix coefficient
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>indices</td>
		<td>
indices where the forces are applied
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indexFromEnd</td>
		<td>
Concerned DOFs indices are numbered from the end of the MState DOFs vector. (default=false)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Force info</td>
	</tr>
	<tr>
		<td>forces</td>
		<td>
vector containing the force amplitude applied at each node
		</td>
		<td></td>
	</tr>
	<tr>
		<td>totalForce</td>
		<td>
total force for all points, will be distributed uniformly over points
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>showArrowSize</td>
		<td>
Size of the drawn arrows (0->no arrows, sign->direction of drawing. (default=0)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>showColor</td>
		<td>
Color for object display (default: [0.2,0.9,0.3,1.0])
		</td>
		<td>0.2 0.9 0.3 1</td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|mstate|MechanicalState used by this component|MechanicalState<Vec1d>|
|topology|link to the topology container|BaseMeshTopology|

- Vec2d

__Target__: Sofa.Component.MechanicalLoad

__namespace__: sofa::component::mechanicalload

__parents__:

- ForceField

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
		<td>rayleighStiffness</td>
		<td>
Rayleigh damping - stiffness matrix coefficient
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>indices</td>
		<td>
indices where the forces are applied
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indexFromEnd</td>
		<td>
Concerned DOFs indices are numbered from the end of the MState DOFs vector. (default=false)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Force info</td>
	</tr>
	<tr>
		<td>forces</td>
		<td>
vector containing the force amplitude applied at each node
		</td>
		<td></td>
	</tr>
	<tr>
		<td>totalForce</td>
		<td>
total force for all points, will be distributed uniformly over points
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>showArrowSize</td>
		<td>
Size of the drawn arrows (0->no arrows, sign->direction of drawing. (default=0)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>showColor</td>
		<td>
Color for object display (default: [0.2,0.9,0.3,1.0])
		</td>
		<td>0.2 0.9 0.3 1</td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|mstate|MechanicalState used by this component|MechanicalState<Vec2d>|
|topology|link to the topology container|BaseMeshTopology|

- Vec3d

__Target__: Sofa.Component.MechanicalLoad

__namespace__: sofa::component::mechanicalload

__parents__:

- ForceField

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
		<td>rayleighStiffness</td>
		<td>
Rayleigh damping - stiffness matrix coefficient
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>indices</td>
		<td>
indices where the forces are applied
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indexFromEnd</td>
		<td>
Concerned DOFs indices are numbered from the end of the MState DOFs vector. (default=false)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Force info</td>
	</tr>
	<tr>
		<td>forces</td>
		<td>
vector containing the force amplitude applied at each node
		</td>
		<td></td>
	</tr>
	<tr>
		<td>totalForce</td>
		<td>
total force for all points, will be distributed uniformly over points
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>showArrowSize</td>
		<td>
Size of the drawn arrows (0->no arrows, sign->direction of drawing. (default=0)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>showColor</td>
		<td>
Color for object display (default: [0.2,0.9,0.3,1.0])
		</td>
		<td>0.2 0.9 0.3 1</td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|mstate|MechanicalState used by this component|MechanicalState<Vec3d>|
|topology|link to the topology container|BaseMeshTopology|

- Vec6d

__Target__: Sofa.Component.MechanicalLoad

__namespace__: sofa::component::mechanicalload

__parents__:

- ForceField

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
		<td>rayleighStiffness</td>
		<td>
Rayleigh damping - stiffness matrix coefficient
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>indices</td>
		<td>
indices where the forces are applied
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indexFromEnd</td>
		<td>
Concerned DOFs indices are numbered from the end of the MState DOFs vector. (default=false)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Force info</td>
	</tr>
	<tr>
		<td>forces</td>
		<td>
vector containing the force amplitude applied at each node
		</td>
		<td></td>
	</tr>
	<tr>
		<td>totalForce</td>
		<td>
total force for all points, will be distributed uniformly over points
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>showArrowSize</td>
		<td>
Size of the drawn arrows (0->no arrows, sign->direction of drawing. (default=0)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>showColor</td>
		<td>
Color for object display (default: [0.2,0.9,0.3,1.0])
		</td>
		<td>0.2 0.9 0.3 1</td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|mstate|MechanicalState used by this component|MechanicalState<Vec6d>|
|topology|link to the topology container|BaseMeshTopology|


<!-- automatically generated doc END -->
