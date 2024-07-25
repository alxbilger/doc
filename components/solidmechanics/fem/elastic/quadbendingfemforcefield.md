---
title: QuadBendingFEMForceField
---

QuadBendingFEMForceField
========================

This component belongs to the category of [ForceField](https://www.sofa-framework.org/community/doc/simulation-principles/multi-model-representation/forcefield/). The page is still incomplete, but give us a bit of time to work on it!

Description of the component ...

What it is made for, what it does



Sequence diagram
----------------


Data  
----



Usage
-----

How to use it, what **required** component, case

In which case it works, in which case it doesn't

Limitations

Example
-------

This component is used as follows in XML format:

``` xml
<QuadBendingFEMForceField data_field="X" />
```
or using SofaPython3:

``` python
node.addObject('QuadBendingFEMForceField', data_field='X')
```

With a description of each data

An example scene involving a QuadBendingFEMForceField is available in [*examples/Component/SolidMechanics/FEM/QuadBendingFEMForceField.scn*](https://github.com/sofa-framework/sofa/blob/master/examples/Component/SolidMechanics/FEM/QuadBendingFEMForceField.scn)
<!-- automatically generated doc START -->
__Target__: Sofa.Component.SolidMechanics.FEM.Elastic

__namespace__: sofa::component::solidmechanics::fem::elastic

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
		<td>quadInfo</td>
		<td>
Internal quad data
		</td>
		<td></td>
	</tr>
	<tr>
		<td>vertexInfo</td>
		<td>
Internal point data
		</td>
		<td></td>
	</tr>
	<tr>
		<td>edgeInfo</td>
		<td>
Internal edge data
		</td>
		<td></td>
	</tr>
	<tr>
		<td>method</td>
		<td>
large: large displacements, small: small displacements
		</td>
		<td>small</td>
	</tr>
	<tr>
		<td>poissonRatio</td>
		<td>
Poisson ratio in Hooke's law (vector)
		</td>
		<td>0.45</td>
	</tr>
	<tr>
		<td>youngModulus</td>
		<td>
Young modulus in Hooke's law (vector)
		</td>
		<td>1000</td>
	</tr>
	<tr>
		<td>thickness</td>
		<td>
Thickness of the elements
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
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|mstate|MechanicalState used by this component|MechanicalState<Vec3d>|
|topology|link to the topology container|BaseMeshTopology|


<!-- automatically generated doc END -->
