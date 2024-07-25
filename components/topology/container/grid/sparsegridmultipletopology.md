# SparseGridMultipleTopology

Sparse grid in 3D


__Target__: Sofa.Component.Topology.Container.Grid

__namespace__: sofa::component::topology::container::grid

__parents__:

- SparseGridRamificationTopology

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
		<td>filename</td>
		<td>
Filename of the mesh
		</td>
		<td></td>
	</tr>
	<tr>
		<td>position</td>
		<td>
List of point positions
		</td>
		<td></td>
	</tr>
	<tr>
		<td>edges</td>
		<td>
List of edge indices
		</td>
		<td></td>
	</tr>
	<tr>
		<td>triangles</td>
		<td>
List of triangle indices
		</td>
		<td></td>
	</tr>
	<tr>
		<td>quads</td>
		<td>
List of quad indices
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tetrahedra</td>
		<td>
List of tetrahedron indices
		</td>
		<td></td>
	</tr>
	<tr>
		<td>hexahedra</td>
		<td>
List of hexahedron indices
		</td>
		<td></td>
	</tr>
	<tr>
		<td>uv</td>
		<td>
List of uv coordinates
		</td>
		<td></td>
	</tr>
	<tr>
		<td>fillWeighted</td>
		<td>
Is quantity of matter inside a cell taken into account? (.5 for boundary, 1 for inside)
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>onlyInsideCells</td>
		<td>
Select only inside cells (exclude boundary cells)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>n</td>
		<td>
grid resolution
		</td>
		<td>2 2 2</td>
	</tr>
	<tr>
		<td>min</td>
		<td>
Min
		</td>
		<td>0 0 0</td>
	</tr>
	<tr>
		<td>max</td>
		<td>
Max
		</td>
		<td>0 0 0</td>
	</tr>
	<tr>
		<td>cellWidth</td>
		<td>
if > 0 : dimension of each cell in the created grid
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>nbVirtualFinerLevels</td>
		<td>
create virtual (not in the animation tree) finer sparse grids in order to dispose of finest information (usefull to compute better mechanical properties for example)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>dataResolution</td>
		<td>
Dimension of the voxel File
		</td>
		<td>0 0 0</td>
	</tr>
	<tr>
		<td>voxelSize</td>
		<td>
Dimension of one voxel
		</td>
		<td>1 1 1</td>
	</tr>
	<tr>
		<td>marchingCubeStep</td>
		<td>
Step of the Marching Cube algorithm
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>convolutionSize</td>
		<td>
Dimension of the convolution kernel to smooth the voxels. 0 if no smoothing is required.
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>facets</td>
		<td>
Input mesh facets
		</td>
		<td></td>
	</tr>
	<tr>
		<td>finestConnectivity</td>
		<td>
Test for connectivity at the finest level? (more precise but slower by testing all intersections between the model mesh and the faces between boundary cubes)
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>fileTopologies</td>
		<td>
All topology filenames
		</td>
		<td>[]</td>
	</tr>
	<tr>
		<td>stiffnessCoefs</td>
		<td>
A stiffness coefficient for each topology filename
		</td>
		<td></td>
	</tr>
	<tr>
		<td>massCoefs</td>
		<td>
A mass coefficient for each topology filename
		</td>
		<td></td>
	</tr>
	<tr>
		<td>computeRamifications</td>
		<td>
Are ramifications wanted?
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>erasePreviousCoef</td>
		<td>
Does a new stiffness/mass coefficient replace the previous or blend half/half with it?
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>drawEdges</td>
		<td>
if true, draw the topology Edges
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawTriangles</td>
		<td>
if true, draw the topology Triangles
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawQuads</td>
		<td>
if true, draw the topology Quads
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawTetrahedra</td>
		<td>
if true, draw the topology Tetrahedra
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>drawHexahedra</td>
		<td>
if true, draw the topology hexahedra
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

