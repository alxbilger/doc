# VariationalSymplecticSolver

Implicit time integrator which conserves linear momentum and mechanical energy


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
		<td>newtonError</td>
		<td>
Error tolerance for Newton iterations
		</td>
		<td>0.01</td>
	</tr>
	<tr>
		<td>steps</td>
		<td>
Maximum number of Newton steps
		</td>
		<td>5</td>
	</tr>
	<tr>
		<td>rayleighStiffness</td>
		<td>
Rayleigh damping coefficient related to stiffness, > 0
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>rayleighMass</td>
		<td>
Rayleigh damping coefficient related to mass, > 0
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>saveEnergyInFile</td>
		<td>
If kinetic and potential energies should be dumped in a CSV file at each iteration
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>explicitIntegration</td>
		<td>
Use explicit integration scheme
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>file</td>
		<td>
File name where kinetic and potential energies are saved in a CSV file
		</td>
		<td></td>
	</tr>
	<tr>
		<td>computeHamiltonian</td>
		<td>
Compute hamiltonian
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>hamiltonianEnergy</td>
		<td>
hamiltonian energy
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>useIncrementalPotentialEnergy</td>
		<td>
use real potential energy, if false use approximate potential energy
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>threadSafeVisitor</td>
		<td>
If true, do not use realloc and free visitors in fwdInteractionForceField.
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

