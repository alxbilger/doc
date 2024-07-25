# LightManager

Manage a set of lights that can cast hard and soft shadows.Soft Shadows is done using Variance Shadow Mapping (http://developer.download.nvidia.com/SDK/10.5/direct3d/Source/VarianceShadowMapping/Doc/VarianceShadowMapping.pdf)


__Target__: Sofa.GL.Component.Shader

__namespace__: sofa::gl::component::shader

__parents__:

- VisualManager

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
		<td>shadows</td>
		<td>
Enable Shadow in the scene. (default=0)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>softShadows</td>
		<td>
If Shadows enabled, Enable Variance Soft Shadow in the scene. (default=0)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>ambient</td>
		<td>
Ambient lights contribution (Vec4f)(default=[0.0f,0.0f,0.0f,0.0f])
		</td>
		<td>0 0 0 1</td>
	</tr>
	<tr>
		<td>debugDraw</td>
		<td>
enable/disable drawing of lights shadow textures. (default=false)
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

