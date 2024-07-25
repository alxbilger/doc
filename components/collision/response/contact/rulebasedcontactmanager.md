# RuleBasedContactManager

Create different response to the collisions based on a set of rules


__Target__: Sofa.Component.Collision.Response.Contact

__namespace__: sofa::component::collision::response::contact

__parents__:

- CollisionResponse

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
		<td>response</td>
		<td>
contact response class
		</td>
		<td></td>
	</tr>
	<tr>
		<td>responseParams</td>
		<td>
contact response parameters (syntax: name1=value1&name2=value2&...)
		</td>
		<td></td>
	</tr>
	<tr>
		<td>variables</td>
		<td>
Define a list of variables to be used inside the rules
		</td>
		<td></td>
	</tr>
	<tr>
		<td>rules</td>
		<td>
Ordered list of rules, each with a triplet of strings.
The first two define either the name of the collision model, its group number, or * meaning any model.
The last string define the response algorithm to use for contacts matched by this rule.
Rules are applied in the order they are specified. If none match a given contact, the default response is used.

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

