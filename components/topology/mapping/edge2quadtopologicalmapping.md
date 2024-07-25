# Edge2QuadTopologicalMapping

Special case of mapping where EdgeSetTopology is converted to QuadSetTopology.


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
		<td>nbPointsOnEachCircle</td>
		<td>
Discretization of created circles
		</td>
		<td></td>
	</tr>
	<tr>
		<td>radius</td>
		<td>
Radius of created circles in yz plan
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>radiusFocal</td>
		<td>
If greater than 0., radius in focal axis of created ellipses
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>focalAxis</td>
		<td>
In case of ellipses
		</td>
		<td>0 0 1</td>
	</tr>
	<tr>
		<td>edgeList</td>
		<td>
list of input edges for the topological mapping: by default, all considered
		</td>
		<td></td>
	</tr>
	<tr>
		<td>flipNormals</td>
		<td>
Flip Normal ? (Inverse point order when creating quad)
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
|input|Input topology to map|BaseMeshTopology|
|output|Output topology to map|BaseMeshTopology|
|toQuadContainer|Output container storing Quads|QuadSetTopologyContainer|
|toQuadModifier|Output modifier handling Quads|QuadSetTopologyModifier|

