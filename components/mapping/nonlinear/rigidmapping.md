# RigidMapping

Set the positions and velocities of points attached to a rigid parent


Templates:

- Rigid2d,Vec2d

__Target__: Sofa.Component.Mapping.NonLinear

__namespace__: sofa::component::mapping::nonlinear

__parents__:

- Mapping

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
		<td>mapForces</td>
		<td>
Are forces mapped ?
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>mapConstraints</td>
		<td>
Are constraints mapped ?
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>mapMasses</td>
		<td>
Are masses mapped ?
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>mapMatrices</td>
		<td>
Are matrix explicit mapped?
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>applyRestPosition</td>
		<td>
set to true to apply this mapping to restPosition at init
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>geometricStiffness</td>
		<td>
Method used to compute the geometric stiffness:
-None: geometric stiffness is not computed
-Exact: the exact geometric stiffness is computed
-Stabilized: the exact geometric stiffness is approximated in order to improve stability
		</td>
		<td>Stabilized</td>
	</tr>
	<tr>
		<td>initialPoints</td>
		<td>
Local Coordinates of the points
		</td>
		<td></td>
	</tr>
	<tr>
		<td>index</td>
		<td>
input DOF index
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>filename</td>
		<td>
Xsp file where rigid mapping information can be loaded from.
		</td>
		<td></td>
	</tr>
	<tr>
		<td>useX0</td>
		<td>
Use x0 instead of local copy of initial positions (to support topo changes)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>indexFromEnd</td>
		<td>
input DOF index starts from the end of input DOFs vector
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>rigidIndexPerPoint</td>
		<td>
For each mapped point, the index of the Rigid it is mapped from
		</td>
		<td></td>
	</tr>
	<tr>
		<td>globalToLocalCoords</td>
		<td>
are the output DOFs initially expressed in global coordinates
		</td>
		<td></td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|input|Input object to map|State<Rigid2d>|
|output|Output object to map|State<Vec2d>|

- Rigid3d,Rigid3d

__Target__: Sofa.Component.Mapping.NonLinear

__namespace__: sofa::component::mapping::nonlinear

__parents__:

- Mapping

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
		<td>mapForces</td>
		<td>
Are forces mapped ?
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>mapConstraints</td>
		<td>
Are constraints mapped ?
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>mapMasses</td>
		<td>
Are masses mapped ?
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>mapMatrices</td>
		<td>
Are matrix explicit mapped?
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>applyRestPosition</td>
		<td>
set to true to apply this mapping to restPosition at init
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>geometricStiffness</td>
		<td>
Method used to compute the geometric stiffness:
-None: geometric stiffness is not computed
-Exact: the exact geometric stiffness is computed
-Stabilized: the exact geometric stiffness is approximated in order to improve stability
		</td>
		<td>Stabilized</td>
	</tr>
	<tr>
		<td>initialPoints</td>
		<td>
Local Coordinates of the points
		</td>
		<td></td>
	</tr>
	<tr>
		<td>index</td>
		<td>
input DOF index
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>filename</td>
		<td>
Xsp file where rigid mapping information can be loaded from.
		</td>
		<td></td>
	</tr>
	<tr>
		<td>useX0</td>
		<td>
Use x0 instead of local copy of initial positions (to support topo changes)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>indexFromEnd</td>
		<td>
input DOF index starts from the end of input DOFs vector
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>rigidIndexPerPoint</td>
		<td>
For each mapped point, the index of the Rigid it is mapped from
		</td>
		<td></td>
	</tr>
	<tr>
		<td>globalToLocalCoords</td>
		<td>
are the output DOFs initially expressed in global coordinates
		</td>
		<td></td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|input|Input object to map|State<Rigid3d>|
|output|Output object to map|State<Rigid3d>|

- Rigid3d,Vec3d

__Target__: Sofa.Component.Mapping.NonLinear

__namespace__: sofa::component::mapping::nonlinear

__parents__:

- Mapping

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
		<td>mapForces</td>
		<td>
Are forces mapped ?
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>mapConstraints</td>
		<td>
Are constraints mapped ?
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>mapMasses</td>
		<td>
Are masses mapped ?
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>mapMatrices</td>
		<td>
Are matrix explicit mapped?
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>applyRestPosition</td>
		<td>
set to true to apply this mapping to restPosition at init
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>geometricStiffness</td>
		<td>
Method used to compute the geometric stiffness:
-None: geometric stiffness is not computed
-Exact: the exact geometric stiffness is computed
-Stabilized: the exact geometric stiffness is approximated in order to improve stability
		</td>
		<td>Stabilized</td>
	</tr>
	<tr>
		<td>initialPoints</td>
		<td>
Local Coordinates of the points
		</td>
		<td></td>
	</tr>
	<tr>
		<td>index</td>
		<td>
input DOF index
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>filename</td>
		<td>
Xsp file where rigid mapping information can be loaded from.
		</td>
		<td></td>
	</tr>
	<tr>
		<td>useX0</td>
		<td>
Use x0 instead of local copy of initial positions (to support topo changes)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>indexFromEnd</td>
		<td>
input DOF index starts from the end of input DOFs vector
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>rigidIndexPerPoint</td>
		<td>
For each mapped point, the index of the Rigid it is mapped from
		</td>
		<td></td>
	</tr>
	<tr>
		<td>globalToLocalCoords</td>
		<td>
are the output DOFs initially expressed in global coordinates
		</td>
		<td></td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|input|Input object to map|State<Rigid3d>|
|output|Output object to map|State<Vec3d>|

