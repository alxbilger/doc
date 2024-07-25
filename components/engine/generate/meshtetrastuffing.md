# MeshTetraStuffing

Create a tetrahedral volume mesh from a surface, using the algorithm from F. Labelle and J.R. Shewchuk, "Isosurface Stuffing: Fast Tetrahedral Meshes with Good Dihedral Angles", SIGGRAPH 2007.


__Target__: Sofa.Component.Engine.Generate

__namespace__: sofa::component::engine::generate

__parents__:

- BaseObject

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
		<td>vbbox</td>
		<td>
BBox to restrict the volume to
		</td>
		<td></td>
	</tr>
	<tr>
		<td>size</td>
		<td>
Size of the generate tetrahedra. If negative, number of grid cells in the largest bbox dimension
		</td>
		<td>-8</td>
	</tr>
	<tr>
		<td>outputPoints</td>
		<td>
Output volume mesh points
		</td>
		<td></td>
	</tr>
	<tr>
		<td>outputTetrahedra</td>
		<td>
Output volume mesh tetrahedra
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Inputs</td>
	</tr>
	<tr>
		<td>inputPoints</td>
		<td>
Input surface mesh points
		</td>
		<td></td>
	</tr>
	<tr>
		<td>inputTriangles</td>
		<td>
Input surface mesh triangles
		</td>
		<td></td>
	</tr>
	<tr>
		<td>inputQuads</td>
		<td>
Input surface mesh quads
		</td>
		<td></td>
	</tr>
	<tr>
		<td>alphaLong</td>
		<td>
Minimum alpha values on long edges when snapping points
		</td>
		<td>0.24999</td>
	</tr>
	<tr>
		<td>alphaShort</td>
		<td>
Minimum alpha values on short edges when snapping points
		</td>
		<td>0.42978</td>
	</tr>
	<tr>
		<td>snapPoints</td>
		<td>
Snap points to the surface if intersections on edges are closed to given alpha values
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>splitTetrahedra</td>
		<td>
Split tetrahedra crossing the surface
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>draw</td>
		<td>
Activate rendering of internal datasets
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

