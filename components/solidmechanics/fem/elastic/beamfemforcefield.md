# BeamFEMForceField

Beam finite elements


Templates:

- Rigid3d

__Target__: Sofa.Component.SolidMechanics.FEM.Elastic

__namespace__: sofa::component::solidmechanics::fem::elastic::_beamfemforcefield_

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
		<td>beamsData</td>
		<td>
Internal element data
		</td>
		<td></td>
	</tr>
	<tr>
		<td>poissonRatio</td>
		<td>
Poisson's Ratio
		</td>
		<td>0.49</td>
	</tr>
	<tr>
		<td>youngModulus</td>
		<td>
Young Modulus
		</td>
		<td>5000</td>
	</tr>
	<tr>
		<td>radius</td>
		<td>
radius of the section
		</td>
		<td>0.1</td>
	</tr>
	<tr>
		<td>radiusInner</td>
		<td>
inner radius of the section for hollow beams
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>listSegment</td>
		<td>
apply the forcefield to a subset list of beam segments. If no segment defined, forcefield applies to the whole topology
		</td>
		<td></td>
	</tr>
	<tr>
		<td>useSymmetricAssembly</td>
		<td>
use symmetric assembly of the matrix K
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
|topology|link to the topology container|BaseMeshTopology|

