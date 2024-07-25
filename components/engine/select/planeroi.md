# PlaneROI

Find the primitives inside a given plane


Templates:

- Rigid3d
- Vec3d

__Target__: Sofa.Component.Engine.Select

__namespace__: sofa::component::engine::select

__parents__:

- DataEngine

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
		<td>plane</td>
		<td>
List of planes defined by 3 points and a depth distance
		</td>
		<td></td>
	</tr>
	<tr>
		<td>computeEdges</td>
		<td>
If true, will compute edge list and index list inside the ROI.
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>computeTriangles</td>
		<td>
If true, will compute triangle list and index list inside the ROI.
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>computeTetrahedra</td>
		<td>
If true, will compute tetrahedra list and index list inside the ROI.
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td colspan="3">Inputs</td>
	</tr>
	<tr>
		<td>position</td>
		<td>
Rest position coordinates of the degrees of freedom
		</td>
		<td></td>
	</tr>
	<tr>
		<td>edges</td>
		<td>
Edge Topology
		</td>
		<td></td>
	</tr>
	<tr>
		<td>triangles</td>
		<td>
Triangle Topology
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tetrahedra</td>
		<td>
Tetrahedron Topology
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Outputs</td>
	</tr>
	<tr>
		<td>indices</td>
		<td>
Indices of the points contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>edgeIndices</td>
		<td>
Indices of the edges contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>triangleIndices</td>
		<td>
Indices of the triangles contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tetrahedronIndices</td>
		<td>
Indices of the tetrahedra contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>pointsInROI</td>
		<td>
Points contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>edgesInROI</td>
		<td>
Edges contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>trianglesInROI</td>
		<td>
Triangles contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tetrahedraInROI</td>
		<td>
Tetrahedra contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>drawBoxes</td>
		<td>
Draw Box(es)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawPoints</td>
		<td>
Draw Points
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawEdges</td>
		<td>
Draw Edges
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawTriangles</td>
		<td>
Draw Triangles
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawTetrahedra</td>
		<td>
Draw Tetrahedra
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawSize</td>
		<td>
rendering size for box and topological elements
		</td>
		<td>1</td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|

