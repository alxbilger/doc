# SpotLight

A spot light illuminating the scene.The light has a location and a illumination cone restricting the directionstaken by the rays of light  (can cast shadows).


__Target__: Sofa.GL.Component.Shader

__namespace__: sofa::gl::component::shader

__parents__:

- PositionalLight

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
		<td>color</td>
		<td>
Set the color of the light. (default=[1.0,1.0,1.0,1.0])
		</td>
		<td>1 1 1 1</td>
	</tr>
	<tr>
		<td>shadowTextureSize</td>
		<td>
[Shadowing] Set size for shadow texture 
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>zNear</td>
		<td>
[Shadowing] Light's ZNear
		</td>
		<td></td>
	</tr>
	<tr>
		<td>zFar</td>
		<td>
[Shadowing] Light's ZFar
		</td>
		<td></td>
	</tr>
	<tr>
		<td>shadowsEnabled</td>
		<td>
[Shadowing] Enable Shadow from this light
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>softShadows</td>
		<td>
[Shadowing] Turn on Soft Shadow from this light
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>shadowFactor</td>
		<td>
[Shadowing] Shadow Factor (decrease/increase darkness)
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>VSMLightBleeding</td>
		<td>
[Shadowing] (VSM only) Light bleeding paramter
		</td>
		<td>0.05</td>
	</tr>
	<tr>
		<td>VSMMinVariance</td>
		<td>
[Shadowing] (VSM only) Minimum variance parameter
		</td>
		<td>0.001</td>
	</tr>
	<tr>
		<td>textureUnit</td>
		<td>
[Shadowing] Texture unit for the genereated shadow texture
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>modelViewMatrix</td>
		<td>
[Shadowing] ModelView Matrix
		</td>
		<td></td>
	</tr>
	<tr>
		<td>projectionMatrix</td>
		<td>
[Shadowing] Projection Matrix
		</td>
		<td></td>
	</tr>
	<tr>
		<td>fixed</td>
		<td>
Fix light position from the camera
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>position</td>
		<td>
Set the position of the light
		</td>
		<td>-0.7 0.3 0</td>
	</tr>
	<tr>
		<td>attenuation</td>
		<td>
Set the attenuation of the light
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>direction</td>
		<td>
Set the direction of the light
		</td>
		<td>0 0 -1</td>
	</tr>
	<tr>
		<td>cutoff</td>
		<td>
Set the angle (cutoff) of the spot
		</td>
		<td>30</td>
	</tr>
	<tr>
		<td>exponent</td>
		<td>
Set the exponent of the spot
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>lookat</td>
		<td>
If true, direction specify the point at which the spotlight should be pointed to
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>drawSource</td>
		<td>
Draw Light Source
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

