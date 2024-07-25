# SimpleTesselatedTetraTopologicalMapping

Special case of mapping where TetrahedronSetTopology is converted into a finer TetrahedronSetTopology


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
		<td>tetrahedraMappedFromTetra</td>
		<td>
Each Tetrahedron of the input topology is mapped to the 8 tetrahedrons in which it can be divided
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tetraSource</td>
		<td>
Which tetra from the input topology map to a given tetra in the output topology (sofa::InvalidID if none)
		</td>
		<td></td>
	</tr>
	<tr>
		<td>pointMappedFromPoint</td>
		<td>
Each point of the input topology is mapped to the same point
		</td>
		<td></td>
	</tr>
	<tr>
		<td>pointMappedFromEdge</td>
		<td>
Each edge of the input topology is mapped to his midpoint
		</td>
		<td></td>
	</tr>
	<tr>
		<td>pointSource</td>
		<td>
Which input topology element map to a given point in the output topology : 0 -> none, > 0 -> point index + 1, < 0 , - edge index -1
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

