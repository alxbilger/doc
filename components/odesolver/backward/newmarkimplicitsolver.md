---
title: NewmarkImplicitSolver
---

NewmarkImplicitSolver  
=====================

This component belongs to the category of [integration schemes or ODE Solver](https://www.sofa-framework.org/community/doc/main-principles/system-resolution/integration-schemes/).  

This scheme is an implicit time integrator for dynamic system using the Newmark scheme. To compute the new position or new velocity, the NewmarkImplicitSolver is based on the following equations:

<img class="latex" src="https://latex.codecogs.com/png.latex?x_{t+h}=x_t+h%20v_t+\frac{h^2}{2}((1-2\beta)a_t+2\beta%20a_{t+h})" title="Newmark scheme in position" />

<img class="latex" src="https://latex.codecogs.com/png.latex?v_{t+h}=v_t+h((1-\gamma)a_t+\gamma%20a_{t+h})" title="Newmark scheme in velocity" />


Applied to a mechanical system where <img class="latex" src="https://latex.codecogs.com/png.latex?\small%20Ma_t+(r_MM+r_KK)v_t+Kx_t=f_{ext}" title="Mechanical system with Rayleigh damping" />, we need to solve the following system:


<img class="latex" src="https://latex.codecogs.com/png.latex?\tiny%20Ma_{t+h}+(r_MM+r_KK)v_{t+h}+Kx_{t+h}=f_{ext}" title="System expanded following the Newmark scheme (1)" />

<img class="latex" src="https://latex.codecogs.com/png.latex?\tiny%20Ma_{t+h}+(r_MM+r_KK)(v_t+h((1-\gamma)a_t+\gamma%20a_{t+h}))+K(x_t+hv_t+\frac{h^2}{2}((1-2\beta)a_t+2\beta%20a_{t+h}))=f_{ext}" title="System expanded following the Newmark scheme (2)" />

<img class="latex" src="https://latex.codecogs.com/png.latex?\tiny%20(M+h\gamma(r_MM+r_KK)+h^2\beta%20K)a_{t+h}=f_{ext}-(r_MM+r_KK)(v_t+h(1-\gamma)a_t)-K(x_t+hv_t+\frac{h^2(1-2\beta)}{2}a_t)" title="System expanded following the Newmark scheme (3)" />

<img class="latex" src="https://latex.codecogs.com/png.latex?\tiny%20((1+h\gamma%20r_M)M+(h^2\beta%20+h\gamma%20r_K)K)a_{t+h}=f_{ext}-(r_MM+r_KK)v_t-Kx_t-(r_MM+r_KK)(h(1-\gamma)a_t)-K(hv_t+\frac{h^2(1-2\beta)}{2}a_t)" title="System expanded following the Newmark scheme (4)" />

<img class="latex" src="https://latex.codecogs.com/png.latex?\tiny%20((1+h\gamma%20r_M)M+(h^2\beta+h\gamma%20r_K)K)a_{t+h}=a_t-(r_MM+r_KK)(h(1-\gamma)a_t)-K(hv_t+\frac{h^2(1-2\beta)}{2}a_t)" title="System expanded following the Newmark scheme (5)" />




Sequence diagram
----------------

<a href="https://github.com/sofa-framework/doc/blob/master/images/integrationscheme/NewmarkImplicitSolver.png?raw=true"><img src="https://github.com/sofa-framework/doc/blob/master/images/integrationscheme/NewmarkImplicitSolver.png?raw=true" title="Flow diagram for the NewmarkImplicitSolver"/></a>
 

Data 
----

The solver is ruled by several breaking (converging or diverging) conditions:  

- **gamma** is the Newmark scheme gamma coefficient
- **beta** is the Newmark scheme beta coefficient


Usage  
-----  

At each simulation step and each Newton Raphson iteration, the NewmarkImplicitSolver **requires**:

- a [LinearSolver](https://www.sofa-framework.org/community/doc/main-principles/system-resolution/linear-solvers/) to solve the linear system
- and a MechanicalObject to store the state vectors.


Example  
-------

This component is used as follows in XML format:  

``` xml  
<NewmarkImplicitSolver rayleighMass="0.01" rayleighStiffness="0.01" />
```  

or using SofaPython3:

``` python  
node.addObject('NewmarkImplicitSolver', rayleighMass='0.01', rayleighStiffness='0.01')  
```  

An example scene involving a NewmarkImplicitSolver is available in [*examples/Component/ODESolver/Backward/NewmarkImplicitSolver.scn*](https://github.com/sofa-framework/sofa/blob/master/examples/Component/ODESolver/Backward/NewmarkImplicitSolver.scn)
<!-- automatically generated doc START -->
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
		<td>rayleighStiffness</td>
		<td>
Rayleigh damping coefficient related to stiffness
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>rayleighMass</td>
		<td>
Rayleigh damping coefficient related to mass
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>vdamping</td>
		<td>
Velocity decay coefficient (no decay if null)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>gamma</td>
		<td>
Newmark scheme gamma coefficient
		</td>
		<td>0.5</td>
	</tr>
	<tr>
		<td>beta</td>
		<td>
Newmark scheme beta coefficient
		</td>
		<td>0.25</td>
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


<!-- automatically generated doc END -->
