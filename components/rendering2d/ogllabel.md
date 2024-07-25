# OglLabel

Display 2D text in the viewport.


__Target__: Sofa.GL.Component.Rendering2D

__namespace__: sofa::gl::component::rendering2d

__parents__:

- VisualModel

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
		<td>prefix</td>
		<td>
The prefix of the text to display
		</td>
		<td></td>
	</tr>
	<tr>
		<td>label</td>
		<td>
The text to display
		</td>
		<td></td>
	</tr>
	<tr>
		<td>suffix</td>
		<td>
The suffix of the text to display
		</td>
		<td></td>
	</tr>
	<tr>
		<td>x</td>
		<td>
The x position of the text on the screen
		</td>
		<td>10</td>
	</tr>
	<tr>
		<td>y</td>
		<td>
The y position of the text on the screen
		</td>
		<td>10</td>
	</tr>
	<tr>
		<td>fontsize</td>
		<td>
The size of the font used to display the text on the screen
		</td>
		<td>14</td>
	</tr>
	<tr>
		<td>color</td>
		<td>
The color of the text to display. (default='gray')
		</td>
		<td>0.5 0.5 0.5 1</td>
	</tr>
	<tr>
		<td>selectContrastingColor</td>
		<td>
Overide the color value but one that contrast with the background color
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>updateLabelEveryNbSteps</td>
		<td>
Update the display of the label every nb of time steps
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

