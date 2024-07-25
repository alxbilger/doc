# SphereForceField

Repulsion applied by a sphere toward the exterior


Templates:

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
		<td>contacts</td>
		<td>
Contacts
		</td>
		<td></td>
	</tr>
	<tr>
		<td>center</td>
		<td>
sphere center
		</td>
		<td></td>
	</tr>
	<tr>
		<td>radius</td>
		<td>
sphere radius
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>stiffness</td>
		<td>
force stiffness
		</td>
		<td>500</td>
	</tr>
	<tr>
		<td>damping</td>
		<td>
force damping
		</td>
		<td>5</td>
	</tr>
	<tr>
		<td>color</td>
		<td>
sphere color. (default=[0,0,1,1])
		</td>
		<td>0 0 1 1</td>
	</tr>
	<tr>
		<td>localRange</td>
		<td>
optional range of local DOF indices. Any computation involving only indices outside of this range are discarded (useful for parallelization using mesh partitionning)
		</td>
		<td>-1 -1</td>
	</tr>
	<tr>
		<td>bilateral</td>
		<td>
if true the sphere force field is applied on both sides
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
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|mstate|MechanicalState used by this component|MechanicalState<Vec1d>|

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
		<td>contacts</td>
		<td>
Contacts
		</td>
		<td></td>
	</tr>
	<tr>
		<td>center</td>
		<td>
sphere center
		</td>
		<td></td>
	</tr>
	<tr>
		<td>radius</td>
		<td>
sphere radius
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>stiffness</td>
		<td>
force stiffness
		</td>
		<td>500</td>
	</tr>
	<tr>
		<td>damping</td>
		<td>
force damping
		</td>
		<td>5</td>
	</tr>
	<tr>
		<td>color</td>
		<td>
sphere color. (default=[0,0,1,1])
		</td>
		<td>0 0 1 1</td>
	</tr>
	<tr>
		<td>localRange</td>
		<td>
optional range of local DOF indices. Any computation involving only indices outside of this range are discarded (useful for parallelization using mesh partitionning)
		</td>
		<td>-1 -1</td>
	</tr>
	<tr>
		<td>bilateral</td>
		<td>
if true the sphere force field is applied on both sides
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
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|mstate|MechanicalState used by this component|MechanicalState<Vec2d>|

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
		<td>contacts</td>
		<td>
Contacts
		</td>
		<td></td>
	</tr>
	<tr>
		<td>center</td>
		<td>
sphere center
		</td>
		<td></td>
	</tr>
	<tr>
		<td>radius</td>
		<td>
sphere radius
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>stiffness</td>
		<td>
force stiffness
		</td>
		<td>500</td>
	</tr>
	<tr>
		<td>damping</td>
		<td>
force damping
		</td>
		<td>5</td>
	</tr>
	<tr>
		<td>color</td>
		<td>
sphere color. (default=[0,0,1,1])
		</td>
		<td>0 0 1 1</td>
	</tr>
	<tr>
		<td>localRange</td>
		<td>
optional range of local DOF indices. Any computation involving only indices outside of this range are discarded (useful for parallelization using mesh partitionning)
		</td>
		<td>-1 -1</td>
	</tr>
	<tr>
		<td>bilateral</td>
		<td>
if true the sphere force field is applied on both sides
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
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|mstate|MechanicalState used by this component|MechanicalState<Vec3d>|

