---
title: MergePoints
---

MergePoints
===========

This component belongs to the category of [Engines](https://www.sofa-framework.org/community/doc/simulation-principles/engine/). This engine returns a merged list of positions, given 2 primary lists.

Input Data
----------

-   **position1**: positions of the 1st object
-   **position2**: positions of the 2nd object

Output Data
----------

-   **points**: a new list of positions, containing the 2 previous lists
-   **indices1**: indices of the 1st position list in the new list
-   **indices2**: indices of the 2nd position list in the new list


Examples
--------

An example scene involving the MergePoints engine is available in [*examples/Component/Engine/Generate/MergePoints.scn*](https://github.com/sofa-framework/sofa/blob/master/examples/Component/Engine/Generate/MergePoints.scn)
<!-- automatically generated doc START -->
__Target__: Sofa.Component.Engine.Generate

__namespace__: sofa::component::engine::generate

__parents__:

- DataEngine

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
		<td>noUpdate</td>
		<td>
do not update the output at each time step (false)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Inputs</td>
	</tr>
	<tr>
		<td>position1</td>
		<td>
position coordinates of the degrees of freedom of the first object
		</td>
		<td></td>
	</tr>
	<tr>
		<td>position2</td>
		<td>
Rest position coordinates of the degrees of freedom of the second object
		</td>
		<td></td>
	</tr>
	<tr>
		<td>mappingX2</td>
		<td>
Mapping of indices to inject position2 inside position1 vertex buffer
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Outputs</td>
	</tr>
	<tr>
		<td>indices1</td>
		<td>
Indices of the points of the first object
		</td>
		<td></td>
	</tr>
	<tr>
		<td>indices2</td>
		<td>
Indices of the points of the second object
		</td>
		<td></td>
	</tr>
	<tr>
		<td>points</td>
		<td>
position coordinates resulting from the merge
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


<!-- automatically generated doc END -->
