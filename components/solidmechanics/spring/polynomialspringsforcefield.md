---
title: PolynomialSpringsForceField
---

PolynomialSpringsForceField
===========================

This component belongs to the category of [ForceField](https://www.sofa-framework.org/community/doc/simulation-principles/multi-model-representation/forcefield/). This component allows to simulate springs with Polynomial stress strain behavior. If we note:

- <img class="latex" src="https://latex.codecogs.com/png.latex?F" title="Spring force" /> the spring force
- <img class="latex" src="https://latex.codecogs.com/png.latex?S" title="Cross section" /> the cross section (always 1.0)
- <img class="latex" src="https://latex.codecogs.com/png.latex?\sigma" title="Stress-strain non-linear function" /> the stress-strain non-linear function
- <img class="latex" src="https://latex.codecogs.com/png.latex?l_0" title="Original length of the spring" /> the original length and <img class="latex" src="https://latex.codecogs.com/png.latex?l" title="Current length of the spring" /> the current length of the spring
- <img class="latex" src="https://latex.codecogs.com/png.latex?\Delta%20u%20%3D%20\left\{\begin{matrix}%20\Delta%20x\\%20\Delta%20y\\%20\Delta%20z\\%20\end{matrix}\right." title="Point displacement" /> the point displacement

the generic non-linear force can thus be written:
<img class="latex" src="https://latex.codecogs.com/png.latex?F=S%7E\sigma%20\left(%20\frac{l-l_0}{l_0}%20\right%29%20\frac{\Delta%20u}{l}" title="Generic non-linear spring force" /> 
where <img class="latex" src="https://latex.codecogs.com/png.latex?\sigma" title="Stress-strain non-linear function" /> is polynom as follows:
<img class="latex" src="https://latex.codecogs.com/png.latex?\sigma%20\left(%20\frac{l-l_0}{l_0}%20\right)%20=\sigma(L)=a_1L+a_2L^2+\cdots+a_nL^n" title="Stress-strain non-linear function" />
and
<img class="latex" src="https://latex.codecogs.com/png.latex?\frac{\partial%20\sigma}{\partial%20L}=a_1+a_2L+\cdots+a_nL^{n-1}" title="Derivative of the stress-strain non-linear function" />

The dedication of jacobian matrix for PolynomialSpringForceField is given below:

<img class="latex" src="https://latex.codecogs.com/png.latex?J_F(u)=\left(S\frac{\partial&space;\sigma}{\partial&space;L}\cdot\frac{1}{l_0}-S\sigma\cdot\frac{1}{|l|}&space;\right)\begin{bmatrix}\frac{\Delta&space;x^2}{l^2}&\frac{\Delta&space;x\Delta&space;y}{l^2}&\frac{\Delta&space;x\Delta&space;z}{l^2}\\\frac{\Delta&space;y\Delta&space;x}{l^2}&\frac{\Delta&space;y^2}{l^2}&\frac{\Delta&space;y\Delta&space;z}{l^2}\\\frac{\Delta&space;z\Delta&space;x}{l^2}&\frac{\Delta&space;z\Delta&space;y}{l^2}&&space;\frac{\Delta&space;z^2}{l^2}\end{bmatrix}&plus;S\sigma\cdot\frac{1}{|l|}\begin{bmatrix}1&0&0\\0&1&0\\0&0&1\end{bmatrix}" title="Jacobian of the spring" />


Note that a **RestShape**PolynomialSpringsForceField does exist. It will compute the same non-linear force with regards to the rest shape of one single object. To avoid Nan problems when a spring has a zero length, an exponential addition to the denominator has been added. As a result, the stress simulation is shifted compared with polynomial values, but it keeps its nonlinearity:

<img class="latex" src="https://latex.codecogs.com/png.latex?J_F(u)=\left(S\frac{\partial&space;\sigma}{\partial&space;L}\cdot\frac{(1-sc\cdot&space;e^{sh-sc(\Delta&space;x^2&plus;\Delta&space;y^2&plus;\Delta&space;z^2)})}{l_0}-S\sigma\cdot\frac{(1-sc\cdot&space;e^{sh-sc(\Delta&space;x^2&plus;\Delta&space;y^2&plus;\Delta&space;z^2)})}{\sqrt{\Delta&space;x^2&plus;\Delta&space;y^2&plus;\Delta&space;z^2&plus;e^{sh-sc(\Delta&space;x^2&plus;\Delta&space;y^2&plus;\Delta&space;z^2)}}}&space;\right)\cdot\frac{1}{\sqrt{\Delta&space;x^2&plus;\Delta&space;y^2&plus;\Delta&space;z^2&plus;e^{sh-sc(\Delta&space;x^2&plus;\Delta&space;y^2&plus;\Delta&space;z^2)}}}\cdot\begin{bmatrix}\Delta&space;x^2&\Delta&space;x\Delta&space;y&\Delta&space;x\Delta&space;z\\\Delta&space;y\Delta&space;x&\Delta&space;y^2&\Delta&space;y\Delta&space;z\\\Delta&space;z\Delta&space;x&\Delta&space;z\Delta&space;y&\Delta&space;z^2\end{bmatrix}&plus;S\sigma\cdot\frac{1}{\sqrt{\Delta&space;x^2&plus;\Delta&space;y^2&plus;\Delta&space;z^2&plus;e^{sh-sc(\Delta&space;x^2&plus;\Delta&space;y^2&plus;\Delta&space;z^2)}}}\begin{bmatrix}1&0&0\\0&1&0\\0&0&1\end{bmatrix}" title="Modified Jacobian of the RestShapePolynomialSpringsForceField" />


More details were given in the pull-request [#1342](https://github.com/sofa-framework/sofa/pull/1342).


Data  
----

The polynomial parameters are set as two arrays:

- **polynomialDegree**: describing the set of polynomial degrees for every spring
- **polynomialStiffness**: describing the set of polynomial coefficients sequentially combined in one vector.

The coefficients are put from smaller degree to bigger one, and the free coefficient is always zero (since for no strain we have no stress).
For examples the coefficients for polynomials [3,2,4] will be put as [a1,a2,a3,b1,b2,c1,c2,c3,c4].

- **firstObjectPoints** corresponding to the indices of the points related to the first object
- **secondObjectPoints** corresponding to the indices of the points related to the second object
- **compressible**: indicating if object compresses without reaction force


Usage
-----

The PolynomialSpringsForceField **requires** two different objects to link, which means two MechanicalObjects on which the non-linear spring will act.
On the other hand, RestShapePolynomialSpringsForceField will act on one single body, i.e. one MechanicalObject.

Example
-------

This component is used as follows in XML format:

``` xml
<DiagonalMass massDensity="1000" />
```

or using Python:

``` python
node.createObject('DiagonalMass', massDensity='1000')
```

An example scene involving a PolynomialSpringsForceField is available in [*examples/Component/SolidMechanics/Spring/PolynomialSpringsForceField.scn*](https://github.com/sofa-framework/sofa/blob/master/examples/Component/SolidMechanics/Spring/PolynomialSpringsForceField.scn)
<!-- automatically generated doc START -->
__Target__: Sofa.Component.SolidMechanics.Spring

__namespace__: sofa::component::solidmechanics::spring

__parents__:

- PairInteractionForceField

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
Rayleigh damping - stiffness matrix coefficient
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>firstObjectPoints</td>
		<td>
points related to the first object
		</td>
		<td></td>
	</tr>
	<tr>
		<td>secondObjectPoints</td>
		<td>
points related to the second object
		</td>
		<td></td>
	</tr>
	<tr>
		<td>polynomialStiffness</td>
		<td>
coefficients for all spring polynomials
		</td>
		<td></td>
	</tr>
	<tr>
		<td>polynomialDegree</td>
		<td>
vector of values that show polynomials degrees
		</td>
		<td></td>
	</tr>
	<tr>
		<td>computeZeroLength</td>
		<td>
flag to compute initial length for springs
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>zeroLength</td>
		<td>
initial length for springs
		</td>
		<td></td>
	</tr>
	<tr>
		<td>recompute_indices</td>
		<td>
Recompute indices (should be false for BBOX)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>compressible</td>
		<td>
Indicates if object compresses without any reaction force
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>springColor</td>
		<td>
spring color
		</td>
		<td>0 1 0 1</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>drawMode</td>
		<td>
The way springs will be drawn:
- 0: Line
- 1:Cylinder
- 2: Arrow
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>showArrowSize</td>
		<td>
size of the axis
		</td>
		<td>0.01</td>
	</tr>
	<tr>
		<td>showIndicesScale</td>
		<td>
Scale for indices display (default=0.02)
		</td>
		<td>0.02</td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|object1|First object associated to this component|MechanicalState<Vec3d>|
|object2|Second object associated to this component|MechanicalState<Vec3d>|


<!-- automatically generated doc END -->
