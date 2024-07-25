# OglViewport

OglViewport


__Target__: Sofa.GL.Component.Rendering2D

__namespace__: sofa::gl::component::rendering2d

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
		<td>screenPosition</td>
		<td>
Viewport position
		</td>
		<td></td>
	</tr>
	<tr>
		<td>screenSize</td>
		<td>
Viewport size
		</td>
		<td></td>
	</tr>
	<tr>
		<td>cameraPosition</td>
		<td>
Camera's position in eye's space
		</td>
		<td>0 0 0</td>
	</tr>
	<tr>
		<td>cameraOrientation</td>
		<td>
Camera's orientation
		</td>
		<td>0 0 0 1</td>
	</tr>
	<tr>
		<td>cameraRigid</td>
		<td>
Camera's rigid coord
		</td>
		<td></td>
	</tr>
	<tr>
		<td>zNear</td>
		<td>
Camera's ZNear
		</td>
		<td></td>
	</tr>
	<tr>
		<td>zFar</td>
		<td>
Camera's ZFar
		</td>
		<td></td>
	</tr>
	<tr>
		<td>fovy</td>
		<td>
Field of View (Y axis)
		</td>
		<td>60</td>
	</tr>
	<tr>
		<td>enabled</td>
		<td>
Enable visibility of the viewport
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>advancedRendering</td>
		<td>
If true, viewport will be hidden if advancedRendering visual flag is not enabled
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>useFBO</td>
		<td>
Use a FBO to render the viewport
		</td>
		<td>1</td>
	</tr>
	<tr>
		<td>swapMainView</td>
		<td>
Swap this viewport with the main view
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>drawCamera</td>
		<td>
Draw a frame representing the camera (see it in main viewport)
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

