# StaticSolver

Static ODE Solver


__Target__: Sofa.Component.ODESolver.Backward

__namespace__: sofa::component::odesolver::backward

__parents__:

- OdeSolver
- LinearSolverAccessor

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
		<td>newton_iterations</td>
		<td>
Number of Netwon iterations between each load increments (normally, one load increment per simulation time-step.
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>absolute_correction_tolerance_threshold</td>
		<td>
Convergence criterion of the norm |du| under which the Netwon iterations stop
		</td>
		<td>1e-05</td>
	</tr>
	<tr>
		<td>relative_correction_tolerance_threshold</td>
		<td>
Convergence criterion regarding the ratio |du| / |U| under which the Netwon iterations stop
		</td>
		<td>1e-05</td>
	</tr>
	<tr>
		<td>absolute_residual_tolerance_threshold</td>
		<td>
Convergence criterion of the norm |R| under which the Netwon iterations stop.Use a negative value to disable this criterion
		</td>
		<td>1e-05</td>
	</tr>
	<tr>
		<td>relative_residual_tolerance_threshold</td>
		<td>
Convergence criterion regarding the ratio |R|/|R0| under which the Netwon iterations stop.Use a negative value to disable this criterion
		</td>
		<td>1e-05</td>
	</tr>
	<tr>
		<td>should_diverge_when_residual_is_growing</td>
		<td>
Boolean stopping Netwon iterations when the residual is greater than the one from the previous iteration
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
|linearSolver|Linear solver used by this component|LinearSolver|

