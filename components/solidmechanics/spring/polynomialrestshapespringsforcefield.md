# PolynomialRestShapeSpringsForceField

Simple elastic springs applied to given degrees of freedom between their current and rest shape position


Templates:

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
		<td>external_points</td>
		<td>
points from the external Mechancial State that define the rest shape springs
		</td>
		<td></td>
	</tr>
	<tr>
		<td>polynomialStiffness</td>
		<td>
coefficients for all spring polynomials
		</td>
		<td></td>
	</tr>
	<tr>
		<td>polynomialDegree</td>
		<td>
vector of values that show polynomials degrees
		</td>
		<td></td>
	</tr>
	<tr>
		<td>recompute_indices</td>
		<td>
Recompute indices (should be false for BBOX)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>springColor</td>
		<td>
spring color
		</td>
		<td>0 1 0 1</td>
	</tr>
	<tr>
		<td>initialLength</td>
		<td>
initial virtual length of the spring
		</td>
		<td></td>
	</tr>
	<tr>
		<td>smoothShift</td>
		<td>
denominator correction adding shift value
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>smoothScale</td>
		<td>
denominator correction adding scale
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
	<tr>
		<td>showIndicesScale</td>
		<td>
Scale for indices display. (default=0.02)
		</td>
		<td>0.02</td>
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

