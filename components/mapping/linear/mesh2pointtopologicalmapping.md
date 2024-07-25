# Mesh2PointTopologicalMapping

This class maps any mesh primitive (point, edge, triangle...) into a point using a relative position from the primitive


__Target__: Sofa.Component.Mapping.Linear

__namespace__: sofa::component::mapping::linear

__parents__:

- TopologicalMapping

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
		<td>copyEdges</td>
		<td>
Activate mapping of input edges into the output topology (requires at least one item in pointBaryCoords)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>copyTriangles</td>
		<td>
Activate mapping of input triangles into the output topology (requires at least one item in pointBaryCoords)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>copyTetrahedra</td>
		<td>
Activate mapping of input tetrahedra into the output topology (requires at least one item in pointBaryCoords)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">BaryCoords</td>
	</tr>
	<tr>
		<td>pointBaryCoords</td>
		<td>
Coordinates for the points of the output topology created from the points of the input topology
		</td>
		<td></td>
	</tr>
	<tr>
		<td>edgeBaryCoords</td>
		<td>
Coordinates for the points of the output topology created from the edges of the input topology
		</td>
		<td></td>
	</tr>
	<tr>
		<td>triangleBaryCoords</td>
		<td>
Coordinates for the points of the output topology created from the triangles of the input topology
		</td>
		<td></td>
	</tr>
	<tr>
		<td>quadBaryCoords</td>
		<td>
Coordinates for the points of the output topology created from the quads of the input topology
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tetraBaryCoords</td>
		<td>
Coordinates for the points of the output topology created from the tetra of the input topology
		</td>
		<td></td>
	</tr>
	<tr>
		<td>hexaBaryCoords</td>
		<td>
Coordinates for the points of the output topology created from the hexa of the input topology
		</td>
		<td></td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|input|Input topology to map|BaseMeshTopology|
|output|Output topology to map|BaseMeshTopology|

