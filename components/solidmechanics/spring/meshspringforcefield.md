# MeshSpringForceField

Spring force field acting along the edges of a mesh


Templates:

- Vec1d

__Target__: Sofa.Component.SolidMechanics.Spring

__namespace__: sofa::component::solidmechanics::spring

__parents__:

- StiffSpringForceField

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
		<td>stiffness</td>
		<td>
uniform stiffness for the all springs
		</td>
		<td>100</td>
	</tr>
	<tr>
		<td>damping</td>
		<td>
uniform damping for the all springs
		</td>
		<td>5</td>
	</tr>
	<tr>
		<td>spring</td>
		<td>
pairs of indices, stiffness, damping, rest length
		</td>
		<td></td>
	</tr>
	<tr>
		<td>springsIndices1</td>
		<td>
List of indices in springs from the first mstate
		</td>
		<td></td>
	</tr>
	<tr>
		<td>springsIndices2</td>
		<td>
List of indices in springs from the second mstate
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indices1</td>
		<td>
Indices of the source points on the first model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indices2</td>
		<td>
Indices of the fixed points on the second model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>lengths</td>
		<td>
List of lengths to create the springs. Must have the same than indices1 & indices2, or if only one element, it will be applied to all springs. If empty, 0 will be applied everywhere
		</td>
		<td></td>
	</tr>
	<tr>
		<td>linesStiffness</td>
		<td>
Stiffness for the Lines
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>linesDamping</td>
		<td>
Damping for the Lines
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>trianglesStiffness</td>
		<td>
Stiffness for the Triangles
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>trianglesDamping</td>
		<td>
Damping for the Triangles
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>quadsStiffness</td>
		<td>
Stiffness for the Quads
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>quadsDamping</td>
		<td>
Damping for the Quads
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>tetrahedraStiffness</td>
		<td>
Stiffness for the Tetrahedra
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>tetrahedraDamping</td>
		<td>
Damping for the Tetrahedra
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>cubesStiffness</td>
		<td>
Stiffness for the Cubes
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>cubesDamping</td>
		<td>
Damping for the Cubes
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>noCompression</td>
		<td>
Only consider elongation
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>localRange</td>
		<td>
optional range of local DOF indices. Any computation involving only indices outside of this range are discarded (useful for parallelization using mesh partitionning)
		</td>
		<td>4294967295 4294967295</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>showArrowSize</td>
		<td>
size of the axis
		</td>
		<td>0.01</td>
	</tr>
	<tr>
		<td>drawMode</td>
		<td>
The way springs will be drawn:
- 0: Line
- 1:Cylinder
- 2: Arrow
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawMinElongationRange</td>
		<td>
Min range of elongation (red eongation - blue neutral - green compression)
		</td>
		<td>8</td>
	</tr>
	<tr>
		<td>drawMaxElongationRange</td>
		<td>
Max range of elongation (red eongation - blue neutral - green compression)
		</td>
		<td>15</td>
	</tr>
	<tr>
		<td>drawSpringSize</td>
		<td>
Size of drawed lines
		</td>
		<td>8</td>
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
|object1|First object associated to this component|MechanicalState<Vec1d>|
|object2|Second object associated to this component|MechanicalState<Vec1d>|
|topology|link to the topology container|BaseMeshTopology|

- Vec2d

__Target__: Sofa.Component.SolidMechanics.Spring

__namespace__: sofa::component::solidmechanics::spring

__parents__:

- StiffSpringForceField

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
		<td>stiffness</td>
		<td>
uniform stiffness for the all springs
		</td>
		<td>100</td>
	</tr>
	<tr>
		<td>damping</td>
		<td>
uniform damping for the all springs
		</td>
		<td>5</td>
	</tr>
	<tr>
		<td>spring</td>
		<td>
pairs of indices, stiffness, damping, rest length
		</td>
		<td></td>
	</tr>
	<tr>
		<td>springsIndices1</td>
		<td>
List of indices in springs from the first mstate
		</td>
		<td></td>
	</tr>
	<tr>
		<td>springsIndices2</td>
		<td>
List of indices in springs from the second mstate
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indices1</td>
		<td>
Indices of the source points on the first model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indices2</td>
		<td>
Indices of the fixed points on the second model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>lengths</td>
		<td>
List of lengths to create the springs. Must have the same than indices1 & indices2, or if only one element, it will be applied to all springs. If empty, 0 will be applied everywhere
		</td>
		<td></td>
	</tr>
	<tr>
		<td>linesStiffness</td>
		<td>
Stiffness for the Lines
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>linesDamping</td>
		<td>
Damping for the Lines
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>trianglesStiffness</td>
		<td>
Stiffness for the Triangles
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>trianglesDamping</td>
		<td>
Damping for the Triangles
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>quadsStiffness</td>
		<td>
Stiffness for the Quads
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>quadsDamping</td>
		<td>
Damping for the Quads
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>tetrahedraStiffness</td>
		<td>
Stiffness for the Tetrahedra
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>tetrahedraDamping</td>
		<td>
Damping for the Tetrahedra
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>cubesStiffness</td>
		<td>
Stiffness for the Cubes
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>cubesDamping</td>
		<td>
Damping for the Cubes
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>noCompression</td>
		<td>
Only consider elongation
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>localRange</td>
		<td>
optional range of local DOF indices. Any computation involving only indices outside of this range are discarded (useful for parallelization using mesh partitionning)
		</td>
		<td>4294967295 4294967295</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>showArrowSize</td>
		<td>
size of the axis
		</td>
		<td>0.01</td>
	</tr>
	<tr>
		<td>drawMode</td>
		<td>
The way springs will be drawn:
- 0: Line
- 1:Cylinder
- 2: Arrow
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawMinElongationRange</td>
		<td>
Min range of elongation (red eongation - blue neutral - green compression)
		</td>
		<td>8</td>
	</tr>
	<tr>
		<td>drawMaxElongationRange</td>
		<td>
Max range of elongation (red eongation - blue neutral - green compression)
		</td>
		<td>15</td>
	</tr>
	<tr>
		<td>drawSpringSize</td>
		<td>
Size of drawed lines
		</td>
		<td>8</td>
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
|object1|First object associated to this component|MechanicalState<Vec2d>|
|object2|Second object associated to this component|MechanicalState<Vec2d>|
|topology|link to the topology container|BaseMeshTopology|

- Vec3d

__Target__: Sofa.Component.SolidMechanics.Spring

__namespace__: sofa::component::solidmechanics::spring

__parents__:

- StiffSpringForceField

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
		<td>stiffness</td>
		<td>
uniform stiffness for the all springs
		</td>
		<td>100</td>
	</tr>
	<tr>
		<td>damping</td>
		<td>
uniform damping for the all springs
		</td>
		<td>5</td>
	</tr>
	<tr>
		<td>spring</td>
		<td>
pairs of indices, stiffness, damping, rest length
		</td>
		<td></td>
	</tr>
	<tr>
		<td>springsIndices1</td>
		<td>
List of indices in springs from the first mstate
		</td>
		<td></td>
	</tr>
	<tr>
		<td>springsIndices2</td>
		<td>
List of indices in springs from the second mstate
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indices1</td>
		<td>
Indices of the source points on the first model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indices2</td>
		<td>
Indices of the fixed points on the second model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>lengths</td>
		<td>
List of lengths to create the springs. Must have the same than indices1 & indices2, or if only one element, it will be applied to all springs. If empty, 0 will be applied everywhere
		</td>
		<td></td>
	</tr>
	<tr>
		<td>linesStiffness</td>
		<td>
Stiffness for the Lines
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>linesDamping</td>
		<td>
Damping for the Lines
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>trianglesStiffness</td>
		<td>
Stiffness for the Triangles
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>trianglesDamping</td>
		<td>
Damping for the Triangles
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>quadsStiffness</td>
		<td>
Stiffness for the Quads
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>quadsDamping</td>
		<td>
Damping for the Quads
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>tetrahedraStiffness</td>
		<td>
Stiffness for the Tetrahedra
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>tetrahedraDamping</td>
		<td>
Damping for the Tetrahedra
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>cubesStiffness</td>
		<td>
Stiffness for the Cubes
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>cubesDamping</td>
		<td>
Damping for the Cubes
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>noCompression</td>
		<td>
Only consider elongation
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>localRange</td>
		<td>
optional range of local DOF indices. Any computation involving only indices outside of this range are discarded (useful for parallelization using mesh partitionning)
		</td>
		<td>4294967295 4294967295</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>showArrowSize</td>
		<td>
size of the axis
		</td>
		<td>0.01</td>
	</tr>
	<tr>
		<td>drawMode</td>
		<td>
The way springs will be drawn:
- 0: Line
- 1:Cylinder
- 2: Arrow
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawMinElongationRange</td>
		<td>
Min range of elongation (red eongation - blue neutral - green compression)
		</td>
		<td>8</td>
	</tr>
	<tr>
		<td>drawMaxElongationRange</td>
		<td>
Max range of elongation (red eongation - blue neutral - green compression)
		</td>
		<td>15</td>
	</tr>
	<tr>
		<td>drawSpringSize</td>
		<td>
Size of drawed lines
		</td>
		<td>8</td>
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
|object1|First object associated to this component|MechanicalState<Vec3d>|
|object2|Second object associated to this component|MechanicalState<Vec3d>|
|topology|link to the topology container|BaseMeshTopology|

