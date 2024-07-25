# BoxROI

Find the primitives (vertex/edge/triangle/quad/tetrahedron/hexahedron) inside given boxes


Templates:

- Rigid3d
- Vec1d
- Vec2d
- Vec3d
- Vec6d

__Target__: Sofa.Component.Engine.Select

__namespace__: sofa::component::engine::select::boxroi

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
		<td>computeEdges</td>
		<td>
If true, will compute edge list and index list inside the ROI. (default = true)
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>computeTriangles</td>
		<td>
If true, will compute triangle list and index list inside the ROI. (default = true)
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>computeTetrahedra</td>
		<td>
If true, will compute tetrahedra list and index list inside the ROI. (default = true)
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>computeHexahedra</td>
		<td>
If true, will compute hexahedra list and index list inside the ROI. (default = true)
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>computeQuad</td>
		<td>
If true, will compute quad list and index list inside the ROI. (default = true)
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>strict</td>
		<td>
If true, an element is inside the box if all of its nodes are inside. If False, only the center point of the element is checked. (default = true)
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>doUpdate</td>
		<td>
If true, updates the selection at the beginning of simulation steps. (default = true)
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td colspan="3">Inputs</td>
	</tr>
	<tr>
		<td>box</td>
		<td>
List of boxes, each defined by two 3D points : xmin,ymin,zmin, xmax,ymax,zmax
		</td>
		<td></td>
	</tr>
	<tr>
		<td>orientedBox</td>
		<td>
List of boxes defined by 3 points (p0, p1, p2) and a depth distance 
A parallelogram will be defined by (p0, p1, p2, p3 = p0 + (p2-p1)). 
The box will finaly correspond to the parallelogram extrusion of depth/2 
along its normal and depth/2 in the opposite direction. 
		</td>
		<td></td>
	</tr>
	<tr>
		<td>position</td>
		<td>
Rest position coordinates of the degrees of freedom. 
If empty the positions from a MechanicalObject then a MeshLoader are searched in the current context. 
If none are found the parent's context is searched for MechanicalObject.
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
		<td>hexahedra</td>
		<td>
Hexahedron Topology
		</td>
		<td></td>
	</tr>
	<tr>
		<td>quad</td>
		<td>
Quad Topology
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
		<td>hexahedronIndices</td>
		<td>
Indices of the hexahedra contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>quadIndices</td>
		<td>
Indices of the quad contained in the ROI
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
		<td>hexahedraInROI</td>
		<td>
Hexahedra contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>quadInROI</td>
		<td>
Quad contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>nbIndices</td>
		<td>
Number of selected indices
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>drawBoxes</td>
		<td>
Draw bounding box (default = false)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawPoints</td>
		<td>
Draw Points. (default = false)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawEdges</td>
		<td>
Draw Edges. (default = false)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawTriangles</td>
		<td>
Draw Triangles. (default = false)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawTetrahedra</td>
		<td>
Draw Tetrahedra. (default = false)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawHexahedra</td>
		<td>
Draw Tetrahedra. (default = false)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawQuads</td>
		<td>
Draw Quads. (default = false)
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

