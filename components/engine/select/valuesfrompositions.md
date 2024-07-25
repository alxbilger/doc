# ValuesFromPositions

Assign values to primitives (vertex/edge/triangle/tetrahedron) based on a linear interpolation of values along a direction


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
		<td>fieldType</td>
		<td>
field type of output elements
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Inputs</td>
	</tr>
	<tr>
		<td>inputValues</td>
		<td>
Input values
		</td>
		<td></td>
	</tr>
	<tr>
		<td>direction</td>
		<td>
Direction along which the values are interpolated
		</td>
		<td>0 1 0</td>
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
		<td>values</td>
		<td>
Values of the points contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>edgeValues</td>
		<td>
Values of the edges contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>triangleValues</td>
		<td>
Values of the triangles contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tetrahedronValues</td>
		<td>
Values of the tetrahedra contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>pointVectors</td>
		<td>
Vectors of the points contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>edgeVectors</td>
		<td>
Vectors of the edges contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>triangleVectors</td>
		<td>
Vectors of the triangles contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tetrahedronVectors</td>
		<td>
Vectors of the tetrahedra contained in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>drawVectors</td>
		<td>
draw vectors line
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawVectorLength</td>
		<td>
vector length visualisation. 
		</td>
		<td>10</td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|

