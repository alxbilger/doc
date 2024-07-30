# MinResLinearSolver

Linear system solver using the MINRES iterative algorithm


Templates:

- CompressedRowSparseMatrixMat2x2d

__Target__: Sofa.Component.LinearSolver.Iterative

__namespace__: sofa::component::linearsolver::iterative

__parents__:

- MatrixLinearSolver

## Data

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
		<td>parallelInverseProduct</td>
		<td>
Parallelize the computation of the product J*M^{-1}*J^T where M is the matrix of the linear system and J is any matrix with compatible dimensions
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>iterations</td>
		<td>
maximum number of iterations of the Conjugate Gradient solution
		</td>
		<td>25</td>
	</tr>
	<tr>
		<td>tolerance</td>
		<td>
desired precision of the Conjugate Gradient Solution (ratio of current residual norm over initial residual norm)
		</td>
		<td>1e-05</td>
	</tr>
	<tr>
		<td>graph</td>
		<td>
Graph of residuals at each iteration
		</td>
		<td></td>
	</tr>

</tbody>
</table>

## Links


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|linearSystem|The linear system to solve|TypedMatrixLinearSystem<CompressedRowSparseMatrixMat2x2d>|

Templates:

- CompressedRowSparseMatrixMat3x3d

__Target__: Sofa.Component.LinearSolver.Iterative

__namespace__: sofa::component::linearsolver::iterative

__parents__:

- MatrixLinearSolver

## Data

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
		<td>parallelInverseProduct</td>
		<td>
Parallelize the computation of the product J*M^{-1}*J^T where M is the matrix of the linear system and J is any matrix with compatible dimensions
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>iterations</td>
		<td>
maximum number of iterations of the Conjugate Gradient solution
		</td>
		<td>25</td>
	</tr>
	<tr>
		<td>tolerance</td>
		<td>
desired precision of the Conjugate Gradient Solution (ratio of current residual norm over initial residual norm)
		</td>
		<td>1e-05</td>
	</tr>
	<tr>
		<td>graph</td>
		<td>
Graph of residuals at each iteration
		</td>
		<td></td>
	</tr>

</tbody>
</table>

## Links


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|linearSystem|The linear system to solve|TypedMatrixLinearSystem<CompressedRowSparseMatrixMat3x3d>|

Templates:

- CompressedRowSparseMatrixMat4x4d

__Target__: Sofa.Component.LinearSolver.Iterative

__namespace__: sofa::component::linearsolver::iterative

__parents__:

- MatrixLinearSolver

## Data

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
		<td>parallelInverseProduct</td>
		<td>
Parallelize the computation of the product J*M^{-1}*J^T where M is the matrix of the linear system and J is any matrix with compatible dimensions
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>iterations</td>
		<td>
maximum number of iterations of the Conjugate Gradient solution
		</td>
		<td>25</td>
	</tr>
	<tr>
		<td>tolerance</td>
		<td>
desired precision of the Conjugate Gradient Solution (ratio of current residual norm over initial residual norm)
		</td>
		<td>1e-05</td>
	</tr>
	<tr>
		<td>graph</td>
		<td>
Graph of residuals at each iteration
		</td>
		<td></td>
	</tr>

</tbody>
</table>

## Links


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|linearSystem|The linear system to solve|TypedMatrixLinearSystem<CompressedRowSparseMatrixMat4x4d>|

Templates:

- CompressedRowSparseMatrixMat6x6d

__Target__: Sofa.Component.LinearSolver.Iterative

__namespace__: sofa::component::linearsolver::iterative

__parents__:

- MatrixLinearSolver

## Data

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
		<td>parallelInverseProduct</td>
		<td>
Parallelize the computation of the product J*M^{-1}*J^T where M is the matrix of the linear system and J is any matrix with compatible dimensions
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>iterations</td>
		<td>
maximum number of iterations of the Conjugate Gradient solution
		</td>
		<td>25</td>
	</tr>
	<tr>
		<td>tolerance</td>
		<td>
desired precision of the Conjugate Gradient Solution (ratio of current residual norm over initial residual norm)
		</td>
		<td>1e-05</td>
	</tr>
	<tr>
		<td>graph</td>
		<td>
Graph of residuals at each iteration
		</td>
		<td></td>
	</tr>

</tbody>
</table>

## Links


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|linearSystem|The linear system to solve|TypedMatrixLinearSystem<CompressedRowSparseMatrixMat6x6d>|

Templates:

- CompressedRowSparseMatrixMat8x8d

__Target__: Sofa.Component.LinearSolver.Iterative

__namespace__: sofa::component::linearsolver::iterative

__parents__:

- MatrixLinearSolver

## Data

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
		<td>parallelInverseProduct</td>
		<td>
Parallelize the computation of the product J*M^{-1}*J^T where M is the matrix of the linear system and J is any matrix with compatible dimensions
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>iterations</td>
		<td>
maximum number of iterations of the Conjugate Gradient solution
		</td>
		<td>25</td>
	</tr>
	<tr>
		<td>tolerance</td>
		<td>
desired precision of the Conjugate Gradient Solution (ratio of current residual norm over initial residual norm)
		</td>
		<td>1e-05</td>
	</tr>
	<tr>
		<td>graph</td>
		<td>
Graph of residuals at each iteration
		</td>
		<td></td>
	</tr>

</tbody>
</table>

## Links


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|linearSystem|The linear system to solve|TypedMatrixLinearSystem<CompressedRowSparseMatrixMat8x8d>|

Templates:

- CompressedRowSparseMatrixd

__Target__: Sofa.Component.LinearSolver.Iterative

__namespace__: sofa::component::linearsolver::iterative

__parents__:

- MatrixLinearSolver

## Data

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
		<td>parallelInverseProduct</td>
		<td>
Parallelize the computation of the product J*M^{-1}*J^T where M is the matrix of the linear system and J is any matrix with compatible dimensions
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>iterations</td>
		<td>
maximum number of iterations of the Conjugate Gradient solution
		</td>
		<td>25</td>
	</tr>
	<tr>
		<td>tolerance</td>
		<td>
desired precision of the Conjugate Gradient Solution (ratio of current residual norm over initial residual norm)
		</td>
		<td>1e-05</td>
	</tr>
	<tr>
		<td>graph</td>
		<td>
Graph of residuals at each iteration
		</td>
		<td></td>
	</tr>

</tbody>
</table>

## Links


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|linearSystem|The linear system to solve|TypedMatrixLinearSystem<CompressedRowSparseMatrixd>|

Templates:

- FullMatrix

__Target__: Sofa.Component.LinearSolver.Iterative

__namespace__: sofa::component::linearsolver::iterative

__parents__:

- MatrixLinearSolver

## Data

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
		<td>parallelInverseProduct</td>
		<td>
Parallelize the computation of the product J*M^{-1}*J^T where M is the matrix of the linear system and J is any matrix with compatible dimensions
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>iterations</td>
		<td>
maximum number of iterations of the Conjugate Gradient solution
		</td>
		<td>25</td>
	</tr>
	<tr>
		<td>tolerance</td>
		<td>
desired precision of the Conjugate Gradient Solution (ratio of current residual norm over initial residual norm)
		</td>
		<td>1e-05</td>
	</tr>
	<tr>
		<td>graph</td>
		<td>
Graph of residuals at each iteration
		</td>
		<td></td>
	</tr>

</tbody>
</table>

## Links


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|linearSystem|The linear system to solve|TypedMatrixLinearSystem<FullMatrix>|

Templates:

- GraphScattered

__Target__: Sofa.Component.LinearSolver.Iterative

__namespace__: sofa::component::linearsolver::iterative

__parents__:

- MatrixLinearSolver

## Data

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
		<td>parallelInverseProduct</td>
		<td>
Parallelize the computation of the product J*M^{-1}*J^T where M is the matrix of the linear system and J is any matrix with compatible dimensions
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>iterations</td>
		<td>
maximum number of iterations of the Conjugate Gradient solution
		</td>
		<td>25</td>
	</tr>
	<tr>
		<td>tolerance</td>
		<td>
desired precision of the Conjugate Gradient Solution (ratio of current residual norm over initial residual norm)
		</td>
		<td>1e-05</td>
	</tr>
	<tr>
		<td>graph</td>
		<td>
Graph of residuals at each iteration
		</td>
		<td></td>
	</tr>

</tbody>
</table>

## Links


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|linearSystem|The linear system to solve|TypedMatrixLinearSystem<GraphScattered>|

Templates:

- SparseMatrix

__Target__: Sofa.Component.LinearSolver.Iterative

__namespace__: sofa::component::linearsolver::iterative

__parents__:

- MatrixLinearSolver

## Data

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
		<td>parallelInverseProduct</td>
		<td>
Parallelize the computation of the product J*M^{-1}*J^T where M is the matrix of the linear system and J is any matrix with compatible dimensions
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>iterations</td>
		<td>
maximum number of iterations of the Conjugate Gradient solution
		</td>
		<td>25</td>
	</tr>
	<tr>
		<td>tolerance</td>
		<td>
desired precision of the Conjugate Gradient Solution (ratio of current residual norm over initial residual norm)
		</td>
		<td>1e-05</td>
	</tr>
	<tr>
		<td>graph</td>
		<td>
Graph of residuals at each iteration
		</td>
		<td></td>
	</tr>

</tbody>
</table>

## Links


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|linearSystem|The linear system to solve|TypedMatrixLinearSystem<SparseMatrix>|

