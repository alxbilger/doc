# RestShapeSpringsForceField

Elastic springs generating forces on degrees of freedom between their current and rest shape position


Templates:

- Rigid3d

__Target__: Sofa.Component.SolidMechanics.Spring

__namespace__: sofa::component::solidmechanics::spring

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
		<td>points</td>
		<td>
points controlled by the rest shape springs
		</td>
		<td></td>
	</tr>
	<tr>
		<td>stiffness</td>
		<td>
stiffness values between the actual position and the rest shape position
		</td>
		<td></td>
	</tr>
	<tr>
		<td>angularStiffness</td>
		<td>
angularStiffness assigned when controlling the rotation of the points
		</td>
		<td></td>
	</tr>
	<tr>
		<td>pivot_points</td>
		<td>
global pivot points used when translations instead of the rigid mass centers
		</td>
		<td></td>
	</tr>
	<tr>
		<td>external_points</td>
		<td>
points from the external Mechancial State that define the rest shape springs
		</td>
		<td></td>
	</tr>
	<tr>
		<td>recompute_indices</td>
		<td>
Recompute indices (should be false for BBOX)
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>springColor</td>
		<td>
spring color. (default=[0.0,1.0,0.0,1.0])
		</td>
		<td>0 1 0 1</td>
	</tr>
	<tr>
		<td>activeDirections</td>
		<td>
Directions in which the spring is active (default=[1,1,1,1,1,1,1])
		</td>
		<td>1 1 1 1 1 1 1</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>drawSpring</td>
		<td>
draw Spring
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
|mstate|MechanicalState used by this component|MechanicalState<Rigid3d>|
|external_rest_shape|rest_shape can be defined by the position of an external Mechanical State|MechanicalState<Rigid3d>|
|topology|Link to be set to the topology container in the component graph|BaseMeshTopology|

- Vec1d

__Target__: Sofa.Component.SolidMechanics.Spring

__namespace__: sofa::component::solidmechanics::spring

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
		<td>points</td>
		<td>
points controlled by the rest shape springs
		</td>
		<td></td>
	</tr>
	<tr>
		<td>stiffness</td>
		<td>
stiffness values between the actual position and the rest shape position
		</td>
		<td></td>
	</tr>
	<tr>
		<td>angularStiffness</td>
		<td>
angularStiffness assigned when controlling the rotation of the points
		</td>
		<td></td>
	</tr>
	<tr>
		<td>pivot_points</td>
		<td>
global pivot points used when translations instead of the rigid mass centers
		</td>
		<td></td>
	</tr>
	<tr>
		<td>external_points</td>
		<td>
points from the external Mechancial State that define the rest shape springs
		</td>
		<td></td>
	</tr>
	<tr>
		<td>recompute_indices</td>
		<td>
Recompute indices (should be false for BBOX)
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>springColor</td>
		<td>
spring color. (default=[0.0,1.0,0.0,1.0])
		</td>
		<td>0 1 0 1</td>
	</tr>
	<tr>
		<td>activeDirections</td>
		<td>
Directions in which the spring is active (default=[1])
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>drawSpring</td>
		<td>
draw Spring
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
|external_rest_shape|rest_shape can be defined by the position of an external Mechanical State|MechanicalState<Vec1d>|
|topology|Link to be set to the topology container in the component graph|BaseMeshTopology|

- Vec3d

__Target__: Sofa.Component.SolidMechanics.Spring

__namespace__: sofa::component::solidmechanics::spring

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
		<td>points</td>
		<td>
points controlled by the rest shape springs
		</td>
		<td></td>
	</tr>
	<tr>
		<td>stiffness</td>
		<td>
stiffness values between the actual position and the rest shape position
		</td>
		<td></td>
	</tr>
	<tr>
		<td>angularStiffness</td>
		<td>
angularStiffness assigned when controlling the rotation of the points
		</td>
		<td></td>
	</tr>
	<tr>
		<td>pivot_points</td>
		<td>
global pivot points used when translations instead of the rigid mass centers
		</td>
		<td></td>
	</tr>
	<tr>
		<td>external_points</td>
		<td>
points from the external Mechancial State that define the rest shape springs
		</td>
		<td></td>
	</tr>
	<tr>
		<td>recompute_indices</td>
		<td>
Recompute indices (should be false for BBOX)
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>springColor</td>
		<td>
spring color. (default=[0.0,1.0,0.0,1.0])
		</td>
		<td>0 1 0 1</td>
	</tr>
	<tr>
		<td>activeDirections</td>
		<td>
Directions in which the spring is active (default=[1,1,1])
		</td>
		<td>1 1 1</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>drawSpring</td>
		<td>
draw Spring
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
|external_rest_shape|rest_shape can be defined by the position of an external Mechanical State|MechanicalState<Vec3d>|
|topology|Link to be set to the topology container in the component graph|BaseMeshTopology|

