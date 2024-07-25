# TopologicalChangeProcessor

Read topological Changes and process them.


__Target__: Sofa.Component.Topology.Utility

__namespace__: sofa::component::topology::utility

__parents__:

- BaseObject

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
		<td>filename</td>
		<td>
input file name for topological changes.
		</td>
		<td></td>
	</tr>
	<tr>
		<td>listChanges</td>
		<td>
0 for adding, 1 for removing, 2 for cutting and associated indices.
		</td>
		<td></td>
	</tr>
	<tr>
		<td>interval</td>
		<td>
time duration between 2 actions
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>shift</td>
		<td>
shift between times in the file and times when they will be read
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>loop</td>
		<td>
set to 'true' to re-read the file when reaching the end
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>useDataInputs</td>
		<td>
If true, will perform operation using Data input lists rather than text file.
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>timeToRemove</td>
		<td>
If using option useDataInputs, time at which will be done the operations. Possibility to use the interval Data also.
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>pointsToRemove</td>
		<td>
List of point IDs to be removed.
		</td>
		<td></td>
	</tr>
	<tr>
		<td>edgesToRemove</td>
		<td>
List of edge IDs to be removed.
		</td>
		<td></td>
	</tr>
	<tr>
		<td>trianglesToRemove</td>
		<td>
List of triangle IDs to be removed.
		</td>
		<td></td>
	</tr>
	<tr>
		<td>quadsToRemove</td>
		<td>
List of quad IDs to be removed.
		</td>
		<td></td>
	</tr>
	<tr>
		<td>tetrahedraToRemove</td>
		<td>
List of tetrahedron IDs to be removed.
		</td>
		<td></td>
	</tr>
	<tr>
		<td>hexahedraToRemove</td>
		<td>
List of hexahedron IDs to be removed.
		</td>
		<td></td>
	</tr>
	<tr>
		<td>saveIndicesAtInit</td>
		<td>
set to 'true' to save the incision to do in the init to incise even after a movement
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>epsilonSnapPath</td>
		<td>
epsilon snap path
		</td>
		<td>0.1</td>
	</tr>
	<tr>
		<td>epsilonSnapBorder</td>
		<td>
epsilon snap path
		</td>
		<td>0.25</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>draw</td>
		<td>
draw information
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
|topology|link to the topology container|BaseMeshTopology|

