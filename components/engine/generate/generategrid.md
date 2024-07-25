# GenerateGrid

Generate a Grid Tetrahedral or Hexahedral Mesh


Templates:

- Vec2d
- Vec3d

__Target__: Sofa.Component.Engine.Generate

__namespace__: sofa::component::engine::generate

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
		<td colspan="3">Outputs</td>
	</tr>
	<tr>
		<td>output_position</td>
		<td>
output array of 3d points
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tetrahedra</td>
		<td>
output mesh tetrahedra
		</td>
		<td></td>
	</tr>
	<tr>
		<td>quads</td>
		<td>
output mesh quads
		</td>
		<td></td>
	</tr>
	<tr>
		<td>triangles</td>
		<td>
output mesh triangles
		</td>
		<td></td>
	</tr>
	<tr>
		<td>hexahedra</td>
		<td>
output mesh hexahedra
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Inputs</td>
	</tr>
	<tr>
		<td>min</td>
		<td>
the 3 coordinates of the minimum corner
		</td>
		<td>0 0 0</td>
	</tr>
	<tr>
		<td>max</td>
		<td>
the 3 coordinates of the maximum corner
		</td>
		<td>0 0 0</td>
	</tr>
	<tr>
		<td>resolution</td>
		<td>
the number of cubes in the x,y,z directions. If resolution in the z direction is  0 then a 2D grid is generated
		</td>
		<td>3 3 3</td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|

