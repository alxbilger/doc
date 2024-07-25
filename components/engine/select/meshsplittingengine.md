# MeshSplittingEngine

This class breaks a mesh in multiple parts, based on selected vertices or cells.


Templates:

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
		<td>position</td>
		<td>
input vertices
		</td>
		<td></td>
	</tr>
	<tr>
		<td>edges</td>
		<td>
input edges
		</td>
		<td></td>
	</tr>
	<tr>
		<td>triangles</td>
		<td>
input triangles
		</td>
		<td></td>
	</tr>
	<tr>
		<td>quads</td>
		<td>
input quads
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tetrahedra</td>
		<td>
input tetrahedra
		</td>
		<td></td>
	</tr>
	<tr>
		<td>hexahedra</td>
		<td>
input hexahedra
		</td>
		<td></td>
	</tr>
	<tr>
		<td>nbInputs</td>
		<td>
Number of input vectors
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>indexPairs</td>
		<td>
couples for input vertices: ROI index + index in the ROI
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Outputs</td>
	</tr>
	<tr>
		<td>position1</td>
		<td>
output vertices(1)
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

