# ConicalForceField

Repulsion applied by a cone toward the exterior


__Templates__:
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
		<td>isCompliance</td>
		<td>
Consider the component as a compliance, else as a stiffness
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
		<td>coneCenter</td>
		<td>
cone center
</td>
		<td></td>
	</tr>
	<tr>
		<td>coneHeight</td>
		<td>
cone height
</td>
		<td></td>
	</tr>
	<tr>
		<td>coneAngle</td>
		<td>
cone angle
</td>
		<td>10</td>
	</tr>
	<tr>
		<td>stiffness</td>
		<td>
force stiffness
</td>
		<td>500</td>
	</tr>
	<tr>
		<td>damping</td>
		<td>
force damping
</td>
		<td>5</td>
	</tr>
	<tr>
		<td>color</td>
		<td>
cone color. (default=0.0,0.0,0.0,1.0,1.0)
</td>
		<td>0 0 1 1</td>
	</tr>

</tbody>
</table>


## Examples

```xml
<Node name="root" dt="0.01" gravity="0 -10 0">
    <RequiredPlugin name="Sofa.Component.Collision.Detection.Algorithm"/> <!-- Needed to use components [BVHNarrowPhase BruteForceBroadPhase CollisionPipeline] -->
    <RequiredPlugin name="Sofa.Component.Collision.Detection.Intersection"/> <!-- Needed to use components [DiscreteIntersection] -->
    <RequiredPlugin name="Sofa.Component.Collision.Geometry"/> <!-- Needed to use components [SphereCollisionModel] -->
    <RequiredPlugin name="Sofa.Component.Collision.Response.Contact"/> <!-- Needed to use components [CollisionResponse] -->
    <RequiredPlugin name="Sofa.Component.IO.Mesh"/> <!-- Needed to use components [MeshGmshLoader MeshOBJLoader SphereLoader] -->
    <RequiredPlugin name="Sofa.Component.LinearSolver.Iterative"/> <!-- Needed to use components [CGLinearSolver] -->
    <RequiredPlugin name="Sofa.Component.Mapping.Linear"/> <!-- Needed to use components [BarycentricMapping] -->
    <RequiredPlugin name="Sofa.Component.Mass"/> <!-- Needed to use components [UniformMass] -->
    <RequiredPlugin name="Sofa.Component.MechanicalLoad"/> <!-- Needed to use components [ConicalForceField] -->
    <RequiredPlugin name="Sofa.Component.ODESolver.Backward"/> <!-- Needed to use components [EulerImplicitSolver] -->
    <RequiredPlugin name="Sofa.Component.SolidMechanics.FEM.Elastic"/> <!-- Needed to use components [TetrahedronFEMForceField] -->
    <RequiredPlugin name="Sofa.Component.StateContainer"/> <!-- Needed to use components [MechanicalObject] -->
    <RequiredPlugin name="Sofa.Component.Topology.Container.Constant"/> <!-- Needed to use components [MeshTopology] -->
    <RequiredPlugin name="Sofa.Component.Visual"/> <!-- Needed to use components [VisualStyle] -->
    <RequiredPlugin name="Sofa.GL.Component.Rendering3D"/> <!-- Needed to use components [OglModel] -->

    <VisualStyle displayFlags="showBehaviorModels showForceFields" />
    <DefaultAnimationLoop/>
    <CollisionPipeline verbose="0" />
    <BruteForceBroadPhase/>
    <BVHNarrowPhase/>
    <CollisionResponse response="PenalityContactForceField" />
    <DiscreteIntersection />
    <Node name="Liver">
        <EulerImplicitSolver name="cg_odesolver" printLog="false"  rayleighStiffness="0.1" rayleighMass="0.1" />
        <CGLinearSolver iterations="25" name="linear solver" tolerance="1.0e-9" threshold="1.0e-9" />
        <MeshGmshLoader name="loader" filename="mesh/liver.msh" />
        <MeshTopology src="@loader" />
        <MechanicalObject src="@loader" template="Vec3" name="Liver" />
        <UniformMass name="mass" vertexMass="0.05" />
        <TetrahedronFEMForceField name="FEM" youngModulus="5000" poissonRatio="0.3" computeGlobalMatrix="false" method="large" />
        <ConicalForceField template="Vec3" coneCenter="0.0 -10.0 0.0" coneHeight="0 20 0" coneAngle="40" />
        <Node name="Visu">
            <MeshOBJLoader name="meshLoader_0" filename="mesh/liver-smooth.obj" handleSeams="1" />
            <OglModel name="VisualModel" src="@meshLoader_0" color="red" />
            <BarycentricMapping input="@.." output="@VisualModel" />
        </Node>
        <Node name="Surf">
	    <SphereLoader filename="mesh/liver.sph" />
            <MechanicalObject position="@[-1].position" />
            <SphereCollisionModel name="CollisionModel" listRadius="@[-2].listRadius" />
            <BarycentricMapping />
        </Node>
    </Node>
</Node>
```
