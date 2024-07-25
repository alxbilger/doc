# HausdorffDistance

Compute the Hausdorff distance of two point clouds


Templates:

- Rigid2d
- Rigid3d
- Vec1d
- Vec2d
- Vec3d

__Target__: Sofa.Component.Engine.Analyze

__namespace__: sofa::component::engine::analyze

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
		<td>update</td>
		<td>
Recompute every time step
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Input</td>
	</tr>
	<tr>
		<td>points1</td>
		<td>
Points belonging to the first point cloud
		</td>
		<td></td>
	</tr>
	<tr>
		<td>points2</td>
		<td>
Points belonging to the second point cloud
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Output</td>
	</tr>
	<tr>
		<td>d12</td>
		<td>
Distance from point cloud 1 to 2
		</td>
		<td></td>
	</tr>
	<tr>
		<td>d21</td>
		<td>
Distance from point cloud 2 to 1
		</td>
		<td></td>
	</tr>
	<tr>
		<td>max</td>
		<td>
Symmetrical Hausdorff distance
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

