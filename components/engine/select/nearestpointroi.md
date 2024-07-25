# NearestPointROI

Attach given pair of particles, projecting the positions of the second particles to the first ones


Templates:

- Rigid2d

__Target__: Sofa.Component.Engine.Select

__namespace__: sofa::component::engine::select

__parents__:

- DataEngine
- PairStateAccessor

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
		<td>inputIndices1</td>
		<td>
Indices of the points to consider on the first model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>inputIndices2</td>
		<td>
Indices of the points to consider on the first model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>radius</td>
		<td>
Radius to search corresponding fixed point
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>useRestPosition</td>
		<td>
If true will use restPosition only at init
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td colspan="3">Outputs</td>
	</tr>
	<tr>
		<td>indices1</td>
		<td>
Indices from the first model associated to a dof from the second model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indices2</td>
		<td>
Indices from the second model associated to a dof from the first model
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
		<td>indexPairs</td>
		<td>
list of couples (parent index + index in the parent)
		</td>
		<td></td>
	</tr>
	<tr>
		<td>distances</td>
		<td>
List of distances between pairs of points
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
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|object1|First object associated to this component|MechanicalState<Rigid2d>|
|object2|Second object associated to this component|MechanicalState<Rigid2d>|

- Rigid3d

__Target__: Sofa.Component.Engine.Select

__namespace__: sofa::component::engine::select

__parents__:

- DataEngine
- PairStateAccessor

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
		<td>inputIndices1</td>
		<td>
Indices of the points to consider on the first model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>inputIndices2</td>
		<td>
Indices of the points to consider on the first model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>radius</td>
		<td>
Radius to search corresponding fixed point
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>useRestPosition</td>
		<td>
If true will use restPosition only at init
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td colspan="3">Outputs</td>
	</tr>
	<tr>
		<td>indices1</td>
		<td>
Indices from the first model associated to a dof from the second model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indices2</td>
		<td>
Indices from the second model associated to a dof from the first model
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
		<td>indexPairs</td>
		<td>
list of couples (parent index + index in the parent)
		</td>
		<td></td>
	</tr>
	<tr>
		<td>distances</td>
		<td>
List of distances between pairs of points
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
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|object1|First object associated to this component|MechanicalState<Rigid3d>|
|object2|Second object associated to this component|MechanicalState<Rigid3d>|

- Vec1d

__Target__: Sofa.Component.Engine.Select

__namespace__: sofa::component::engine::select

__parents__:

- DataEngine
- PairStateAccessor

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
		<td>inputIndices1</td>
		<td>
Indices of the points to consider on the first model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>inputIndices2</td>
		<td>
Indices of the points to consider on the first model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>radius</td>
		<td>
Radius to search corresponding fixed point
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>useRestPosition</td>
		<td>
If true will use restPosition only at init
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td colspan="3">Outputs</td>
	</tr>
	<tr>
		<td>indices1</td>
		<td>
Indices from the first model associated to a dof from the second model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indices2</td>
		<td>
Indices from the second model associated to a dof from the first model
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
		<td>indexPairs</td>
		<td>
list of couples (parent index + index in the parent)
		</td>
		<td></td>
	</tr>
	<tr>
		<td>distances</td>
		<td>
List of distances between pairs of points
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
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|object1|First object associated to this component|MechanicalState<Vec1d>|
|object2|Second object associated to this component|MechanicalState<Vec1d>|

- Vec2d

__Target__: Sofa.Component.Engine.Select

__namespace__: sofa::component::engine::select

__parents__:

- DataEngine
- PairStateAccessor

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
		<td>inputIndices1</td>
		<td>
Indices of the points to consider on the first model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>inputIndices2</td>
		<td>
Indices of the points to consider on the first model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>radius</td>
		<td>
Radius to search corresponding fixed point
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>useRestPosition</td>
		<td>
If true will use restPosition only at init
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td colspan="3">Outputs</td>
	</tr>
	<tr>
		<td>indices1</td>
		<td>
Indices from the first model associated to a dof from the second model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indices2</td>
		<td>
Indices from the second model associated to a dof from the first model
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
		<td>indexPairs</td>
		<td>
list of couples (parent index + index in the parent)
		</td>
		<td></td>
	</tr>
	<tr>
		<td>distances</td>
		<td>
List of distances between pairs of points
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
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|object1|First object associated to this component|MechanicalState<Vec2d>|
|object2|Second object associated to this component|MechanicalState<Vec2d>|

- Vec3d

__Target__: Sofa.Component.Engine.Select

__namespace__: sofa::component::engine::select

__parents__:

- DataEngine
- PairStateAccessor

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
		<td>inputIndices1</td>
		<td>
Indices of the points to consider on the first model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>inputIndices2</td>
		<td>
Indices of the points to consider on the first model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>radius</td>
		<td>
Radius to search corresponding fixed point
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>useRestPosition</td>
		<td>
If true will use restPosition only at init
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td colspan="3">Outputs</td>
	</tr>
	<tr>
		<td>indices1</td>
		<td>
Indices from the first model associated to a dof from the second model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indices2</td>
		<td>
Indices from the second model associated to a dof from the first model
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
		<td>indexPairs</td>
		<td>
list of couples (parent index + index in the parent)
		</td>
		<td></td>
	</tr>
	<tr>
		<td>distances</td>
		<td>
List of distances between pairs of points
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
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|object1|First object associated to this component|MechanicalState<Vec3d>|
|object2|Second object associated to this component|MechanicalState<Vec3d>|

- Vec6d

__Target__: Sofa.Component.Engine.Select

__namespace__: sofa::component::engine::select

__parents__:

- DataEngine
- PairStateAccessor

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
		<td>inputIndices1</td>
		<td>
Indices of the points to consider on the first model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>inputIndices2</td>
		<td>
Indices of the points to consider on the first model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>radius</td>
		<td>
Radius to search corresponding fixed point
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>useRestPosition</td>
		<td>
If true will use restPosition only at init
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td colspan="3">Outputs</td>
	</tr>
	<tr>
		<td>indices1</td>
		<td>
Indices from the first model associated to a dof from the second model
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indices2</td>
		<td>
Indices from the second model associated to a dof from the first model
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
		<td>indexPairs</td>
		<td>
list of couples (parent index + index in the parent)
		</td>
		<td></td>
	</tr>
	<tr>
		<td>distances</td>
		<td>
List of distances between pairs of points
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
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|object1|First object associated to this component|MechanicalState<Vec6d>|
|object2|Second object associated to this component|MechanicalState<Vec6d>|

