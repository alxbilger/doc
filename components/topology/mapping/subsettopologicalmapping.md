# SubsetTopologicalMapping

This class is a specific implementation of TopologicalMapping where the destination topology is a subset of the source topology. The implementation currently assumes that both topologies have been initialized correctly.


__Target__: Sofa.Component.Topology.Mapping

__namespace__: sofa::component::topology::mapping

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
		<td>samePoints</td>
		<td>
True if the same set of points is used in both topologies
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>handleEdges</td>
		<td>
True if edges events and mapping should be handled
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>handleTriangles</td>
		<td>
True if triangles events and mapping should be handled
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>handleQuads</td>
		<td>
True if quads events and mapping should be handled
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>handleTetrahedra</td>
		<td>
True if tetrahedra events and mapping should be handled
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>handleHexahedra</td>
		<td>
True if hexahedra events and mapping should be handled
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>pointS2D</td>
		<td>
Internal source -> destination topology points map
		</td>
		<td></td>
	</tr>
	<tr>
		<td>pointD2S</td>
		<td>
Internal destination -> source topology points map (link to SubsetMapping::indices to handle the mechanical-side of the mapping
		</td>
		<td></td>
	</tr>
	<tr>
		<td>edgeS2D</td>
		<td>
Internal source -> destination topology edges map
		</td>
		<td></td>
	</tr>
	<tr>
		<td>edgeD2S</td>
		<td>
Internal destination -> source topology edges map
		</td>
		<td></td>
	</tr>
	<tr>
		<td>triangleS2D</td>
		<td>
Internal source -> destination topology triangles map
		</td>
		<td></td>
	</tr>
	<tr>
		<td>triangleD2S</td>
		<td>
Internal destination -> source topology triangles map
		</td>
		<td></td>
	</tr>
	<tr>
		<td>quadS2D</td>
		<td>
Internal source -> destination topology quads map
		</td>
		<td></td>
	</tr>
	<tr>
		<td>quadD2S</td>
		<td>
Internal destination -> source topology quads map
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tetrahedronS2D</td>
		<td>
Internal source -> destination topology tetrahedra map
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tetrahedronD2S</td>
		<td>
Internal destination -> source topology tetrahedra map
		</td>
		<td></td>
	</tr>
	<tr>
		<td>hexahedronS2D</td>
		<td>
Internal source -> destination topology hexahedra map
		</td>
		<td></td>
	</tr>
	<tr>
		<td>hexahedronD2S</td>
		<td>
Internal destination -> source topology hexahedra map
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

