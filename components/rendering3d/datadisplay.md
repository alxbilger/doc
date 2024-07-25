# DataDisplay

Rendering of meshes colored by data


__Target__: Sofa.GL.Component.Rendering3D

__namespace__: sofa::gl::component::rendering3d

__parents__:

- VisualModel
- VisualState

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
		<td>enable</td>
		<td>
Display the object or not
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>maximalRange</td>
		<td>
Keep the maximal range through all timesteps
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>pointData</td>
		<td>
Data associated with nodes
		</td>
		<td></td>
	</tr>
	<tr>
		<td>triangleData</td>
		<td>
Data associated with triangles
		</td>
		<td></td>
	</tr>
	<tr>
		<td>quadData</td>
		<td>
Data associated with quads
		</td>
		<td></td>
	</tr>
	<tr>
		<td>pointTriangleData</td>
		<td>
Data associated with nodes per triangle
		</td>
		<td></td>
	</tr>
	<tr>
		<td>pointQuadData</td>
		<td>
Data associated with nodes per quad
		</td>
		<td></td>
	</tr>
	<tr>
		<td>colorNaN</td>
		<td>
Color used for NaN values (default=[0.0,0.0,0.0,1.0])
		</td>
		<td>0 0 0 1</td>
	</tr>
	<tr>
		<td>userRange</td>
		<td>
Clamp to this values (if max>min)
		</td>
		<td>1 -1</td>
	</tr>
	<tr>
		<td>currentMin</td>
		<td>
Current min range
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>currentMax</td>
		<td>
Current max range
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>shininess</td>
		<td>
Shininess for rendering point-based data [0,128].  <0 means no specularity
		</td>
		<td>-1</td>
	</tr>
	<tr>
		<td>transparency</td>
		<td>
transparency draw objects with transparency, the value varies between 0. and 1. Where 1. means no transparency and 0 full transparency
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td colspan="3">Vector</td>
	</tr>
	<tr>
		<td>position</td>
		<td>
Vertices coordinates
		</td>
		<td></td>
	</tr>
	<tr>
		<td>restPosition</td>
		<td>
Vertices rest coordinates
		</td>
		<td></td>
	</tr>
	<tr>
		<td>normal</td>
		<td>
Normals of the model
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
|topology|link to the topology container|BaseMeshTopology|

