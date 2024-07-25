# VoxelGridLoader

Voxel loader based on RAW files


__Target__: Sofa.Component.IO.Mesh

__namespace__: sofa::component::io::mesh

__parents__:

- VoxelLoader

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
Filename of the object
		</td>
		<td></td>
	</tr>
	<tr>
		<td>position</td>
		<td>
Coordinates of the nodes loaded
		</td>
		<td></td>
	</tr>
	<tr>
		<td>hexahedra</td>
		<td>
Hexahedra loaded
		</td>
		<td></td>
	</tr>
	<tr>
		<td>voxelSize</td>
		<td>
Dimension of one voxel
		</td>
		<td>1 1 1</td>
	</tr>
	<tr>
		<td>resolution</td>
		<td>
Resolution of the voxel file
		</td>
		<td>0 0 0</td>
	</tr>
	<tr>
		<td>ROI</td>
		<td>
Region of interest (xmin, ymin, zmin, xmax, ymax, zmax)
		</td>
		<td>0 0 0 65535 65535 65535</td>
	</tr>
	<tr>
		<td>header</td>
		<td>
Header size in bytes
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>segmentationHeader</td>
		<td>
Header size in bytes
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>idxInRegularGrid</td>
		<td>
indices of the hexa in the grid.
		</td>
		<td></td>
	</tr>
	<tr>
		<td>bgValue</td>
		<td>
Background values (to be ignored)
		</td>
		<td></td>
	</tr>
	<tr>
		<td>dataValue</td>
		<td>
Active data values
		</td>
		<td></td>
	</tr>
	<tr>
		<td>generateHexa</td>
		<td>
Interpret voxel as either hexa or points
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

