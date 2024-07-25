# TetrahedronDiffusionFEMForceField

Isotropic or anisotropic diffusion on Tetrahedral Meshes


Templates:

- Vec1d

__Target__: Sofa.Component.Diffusion

__namespace__: sofa::component::diffusion

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
		<td>constantDiffusionCoefficient</td>
		<td>
Constant diffusion coefficient
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>tetraDiffusionCoefficient</td>
		<td>
Diffusion coefficient for each tetrahedron, by default equal to constantDiffusionCoefficient.
		</td>
		<td></td>
	</tr>
	<tr>
		<td>anisotropyRatio</td>
		<td>
Anisotropy ratio (r²>1).
 Default is 1.0 = isotropy.
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>transverseAnisotropyArray</td>
		<td>
Data to handle topology on tetrahedra
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tagMechanics</td>
		<td>
Tag of the Mechanical Object.
		</td>
		<td>meca</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>drawConduc</td>
		<td>
To display conductivity map.
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
|topology|link to the topology container|BaseMeshTopology|

- Vec2d

__Target__: Sofa.Component.Diffusion

__namespace__: sofa::component::diffusion

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
		<td>constantDiffusionCoefficient</td>
		<td>
Constant diffusion coefficient
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>tetraDiffusionCoefficient</td>
		<td>
Diffusion coefficient for each tetrahedron, by default equal to constantDiffusionCoefficient.
		</td>
		<td></td>
	</tr>
	<tr>
		<td>anisotropyRatio</td>
		<td>
Anisotropy ratio (r²>1).
 Default is 1.0 = isotropy.
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>transverseAnisotropyArray</td>
		<td>
Data to handle topology on tetrahedra
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tagMechanics</td>
		<td>
Tag of the Mechanical Object.
		</td>
		<td>meca</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>drawConduc</td>
		<td>
To display conductivity map.
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
|topology|link to the topology container|BaseMeshTopology|

- Vec3d

__Target__: Sofa.Component.Diffusion

__namespace__: sofa::component::diffusion

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
		<td>constantDiffusionCoefficient</td>
		<td>
Constant diffusion coefficient
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>tetraDiffusionCoefficient</td>
		<td>
Diffusion coefficient for each tetrahedron, by default equal to constantDiffusionCoefficient.
		</td>
		<td></td>
	</tr>
	<tr>
		<td>anisotropyRatio</td>
		<td>
Anisotropy ratio (r²>1).
 Default is 1.0 = isotropy.
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>transverseAnisotropyArray</td>
		<td>
Data to handle topology on tetrahedra
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tagMechanics</td>
		<td>
Tag of the Mechanical Object.
		</td>
		<td>meca</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>drawConduc</td>
		<td>
To display conductivity map.
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
|topology|link to the topology container|BaseMeshTopology|

