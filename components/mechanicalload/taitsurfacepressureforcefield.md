# TaitSurfacePressureForceField

This component computes the volume enclosed by a surface mesh and apply a pressure force following Tait's equation: $P = P_0 - B((V/V_0)^\gamma - 1)$.
This ForceField can be used to apply :
 * a constant pressure (set $B=0$ and use $P_0$)
 * an ideal gas pressure (set $\gamma=1$ and use $B$)
 * a pressure from water (set $\gamma=7$ and use $B$)


Templates:

- Vec3d

__Target__: Sofa.Component.MechanicalLoad

__namespace__: sofa::component::mechanicalload

__parents__:

- ForceField

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
		<td>rayleighStiffness</td>
		<td>
Rayleigh damping - stiffness matrix coefficient
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>pressureTriangles</td>
		<td>
OUT: list of triangles where a pressure is applied (mesh triangles + tesselated quads)
		</td>
		<td></td>
	</tr>
	<tr>
		<td colspan="3">Controls</td>
	</tr>
	<tr>
		<td>p0</td>
		<td>
IN: Rest pressure when V = V0
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>B</td>
		<td>
IN: Bulk modulus (resistance to uniform compression)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>gamma</td>
		<td>
IN: Bulk modulus (resistance to uniform compression)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>injectedVolume</td>
		<td>
IN: Injected (or extracted) volume since the start of the simulation
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>maxInjectionRate</td>
		<td>
IN: Maximum injection rate (volume per second)
		</td>
		<td>1000</td>
	</tr>
	<tr>
		<td colspan="3">Results</td>
	</tr>
	<tr>
		<td>initialVolume</td>
		<td>
OUT: Initial volume, as computed from the surface rest position
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>currentInjectedVolume</td>
		<td>
OUT: Current injected (or extracted) volume (taking into account maxInjectionRate)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>v0</td>
		<td>
OUT: Rest volume (as computed from initialVolume + injectedVolume)
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>currentVolume</td>
		<td>
OUT: Current volume, as computed from the last surface position
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>currentPressure</td>
		<td>
OUT: Current pressure, as computed from the last surface position
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>currentStiffness</td>
		<td>
OUT: dP/dV at current volume and pressure
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>volumeAfterTC</td>
		<td>
OUT: Volume after a topology change
		</td>
		<td></td>
	</tr>
	<tr>
		<td>surfaceAreaAfterTC</td>
		<td>
OUT: Surface area after a topology change
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Stats</td>
	</tr>
	<tr>
		<td>initialSurfaceArea</td>
		<td>
OUT: Initial surface area, as computed from the surface rest position
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td>currentSurfaceArea</td>
		<td>
OUT: Current surface area, as computed from the last surface position
		</td>
		<td>0</td>
	</tr>
	<tr>
		<td colspan="3">Visualization</td>
	</tr>
	<tr>
		<td>drawForceScale</td>
		<td>
DEBUG: scale used to render force vectors
		</td>
		<td>0.001</td>
	</tr>
	<tr>
		<td>drawForceColor</td>
		<td>
DEBUG: color used to render force vectors
		</td>
		<td>0 1 1 1</td>
	</tr>

</tbody>
</table>

Links: 


| Name | Description | Destination type name |
| ---- | ----------- | --------------------- |
|context|Graph Node containing this object (or BaseContext::getDefault() if no graph is used)|BaseContext|
|slaves|Sub-objects used internally by this object|BaseObject|
|master|nullptr for regular objects, or master object for which this object is one sub-objects|BaseObject|
|mechanicalStates|List of mechanical states to which this component is associated|BaseMechanicalState|
|mstate|MechanicalState used by this component|MechanicalState<Vec3d>|
|topology|link to the topology container|BaseMeshTopology|

