# MatrixLinearSystem

Linear system
Linear system


Templates:

- CompressedRowSparseMatrixMat2x2d
- CompressedRowSparseMatrixMat3x3d
- CompressedRowSparseMatrixMat4x4d
- CompressedRowSparseMatrixMat6x6d
- CompressedRowSparseMatrixMat8x8d
- CompressedRowSparseMatrixd
- FullMatrix
- SparseMatrix

__Target__: Sofa.Component.LinearSystem

__namespace__: sofa::component::linearsystem

__parents__:

- TypedMatrixLinearSystem

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
		<td>matrixSize</td>
		<td>
Size of the global matrix
		</td>
		<td></td>
	</tr>
	<tr>
		<td>assembleStiffness</td>
		<td>
If true, the stiffness is added to the global matrix
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>assembleMass</td>
		<td>
If true, the mass is added to the global matrix
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>assembleDamping</td>
		<td>
If true, the damping is added to the global matrix
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>assembleGeometricStiffness</td>
		<td>
If true, the geometric stiffness of mappings is added to the global matrix
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>applyProjectiveConstraints</td>
		<td>
If true, projective constraints are applied on the global matrix
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>applyMappedComponents</td>
		<td>
If true, mapped components contribute to the global matrix
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>checkIndices</td>
		<td>
If true, indices are verified before being added in to the global matrix, favoring security over speed
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>parallelAssemblyIndependentMatrices</td>
		<td>
If true, independent matrices (global matrix vs mapped matrices) are assembled in parallel
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

