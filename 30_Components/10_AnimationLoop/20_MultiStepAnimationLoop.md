MultiStepAnimationLoop
======================

This component belongs to the category of [AnimationLoop](https://www.sofa-framework.org/community/doc/main-principles/animation-loop/).

The MultiStepAnimationLoop derives from the [DefaultAnimationLoop](https://www.sofa-framework.org/community/doc/using-SOFA/components/animationloop/defaultanimationloop/). This animation loop is different due to the fact that it allows - at each iteration - for running several collision (_collisionSteps_), and within each of these collision steps, several integration sub-steps can be computes (_integrationSteps_).

<a href="https://github.com/sofa-framework/doc/blob/master/images/animationloop/MultiStepAnimationLoop.png?raw=true"><img src="https://github.com/sofa-framework/doc/blob/master/images/animationloop/MultiStepAnimationLoop.png?raw=true" title="Flow diagram for a MultiStepAnimationLoop"/></a>

Data
----

The MultiStepAnimationLoop has the following data:

- **collisionSteps**: the number of collision steps computed within one time step
- **integrationSteps**: the number of time integration (time sub-steps involving the physics resolution) computed within one time step
- **computeBoundingBox**: a boolean defining whether the global bounding box of the scene is computed at each time step. Used mostly for rendering.


Usage
-----

The MultiStepAnimationLoop has **no pre-requisite**.

Note that this MultiStepAnimationLoop does not handle constraints solved using [Lagrange multipliers](https://www.sofa-framework.org/community/doc/main-principles/constraints/lagrange-constraint/).


Example
-------

This component is used as follows in XML format:

``` xml
<MultiStepAnimationLoop collisionSteps="10" integrationSteps="2" />
```

or using SofaPython3:

``` python
node.addObject('MultiStepAnimationLoop', collisionSteps='10', integrationSteps='2')
```

An example scene involving a MultiStepAnimationLoop is available in [*examples/Component/AnimationLoop/MultiStepAnimationLoop.scn*](https://github.com/sofa-framework/sofa/blob/master/examples/Component/AnimationLoop/MultiStepAnimationLoop.scn)
