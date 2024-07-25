---
title: VisualStyle
---

Customize what to render on screen
----------------------------------

#### Description

**VisualStyle** component controls the *DisplayFlags* state embedded in
the **VisualParams** for the current subgraph. It merges the
**DisplayFlags** conveyed by the **VisualParams** with its own
DisplayFlags. Example Taken from
[*examples/Component/Visual/VisualStyle.scn*](https://github.com/sofa-framework/sofa/blob/master/examples/Component/Visual/VisualStyle.scn)



\[caption id="attachment\_1566" align="aligncenter"
width="533"\][![Resulting View from the previous XML
scene](https://www.sofa-framework.org/wp-content/uploads/2014/11/VisualStyle.jpg){.size-full
.wp-image-1566 width="533"
height="400"}](https://www.sofa-framework.org/wp-content/uploads/2014/11/VisualStyle.jpg)
Resulting View from the previous XML scene\[/caption\]

#### XML Usage

```xml
<VisualStyle displayFlags="showBehavior showVisual" />
```

allowed values for displayFlags data are a combination of the following:

```xml
showAll, hideAll,
  showVisual, hideVisual,
   showVisualModels, hideVisualModels,
  showBehavior, hideBehavior,
    showBehaviorModels, hideBehaviorModels,
    showForceFields, hideForceFields,
    showInteractionForceFields, hideInteractionForceFields
  showMapping, hideMapping
    showMappings, hideMappings
    showMechanicalMappings, hideMechanicalMappings
  showCollision, hideCollision
     showCollisionModels, hideCollisionModels
     showBoundingCollisionModels, hideBoundingCollisionModels
showOptions hideOptions
  showNormals hideNormals
  showWireframe hideWireframe
```

#### C++ Usage

In C++, to set the visual style in a node, you have to create a
VisualStyle component, attach it to the node, create and tune a
!DisplayFlags object and set the !VisualStyle with it, as shown in the
following example:

```
  VisualStyle::SPtr visualStyle = New();
  root->addObject(visualStyle);
  VisualStyle::DisplayFlags displayFlags;
  displayFlags.setShowAll();
  visualStyle->displayFlags.setValue(displayFlags);
```

You can also use method component::visualmodel::addVisualStyle(
simulation::Node::SPtr ) to insert a VisualStyle component at the given
node and return a WriteAccessor on the display flags:

```
addVisualStyle(root)->setShowVisual().setShowBehavior().setShowMapping(false);
```
<!-- automatically generated doc START -->
__Target__: Sofa.Component.Visual

__namespace__: sofa::component::visual

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
		<td>displayFlags</td>
		<td>
Display Flags
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
