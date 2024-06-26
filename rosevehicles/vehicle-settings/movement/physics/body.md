---
description: Setting body physics
---

# Body

```yaml
Body:
  Mass: 1550.0
  Collision:
    CCD_Motion_Threshold: 0.5
    CCD_Swept_Sphere_Radius: 0.8
    Restitution: 0.1
    Friction:
      Friction: 1.0
      Rolling: 1.06
      Spinning: 1.05
    Factor:
      Angular: 0.10
      Linear: 0.10
    Damping:
      Angular: 0.20
      Linear: 0.03
    Bounding_Boxes:
      example_box_one:
        Center: "0.0 0.4 0.0"
        Width: 1.0
        Height: 0.5
        Length: 2.3
      example_box_two:
        Center: "0.0 0.7 0.0"
        Width: 0.9
        Height: 0.5
        Length: 1.0
```

## Mass

The weight of the vehicle in kilograms.

## Continuous collision detection (CCD)

When simulating physics in a game or animation, a fast-moving object can sometimes pass through thin obstacles without any collision being detected. This happens because the object moves so quickly that it skips over the obstacle in a single simulation step.

While you could reduce the time step to catch these collisions, this makes the simulation much slower and less efficient.

A better solution is to use Continuous Collision Detection (CCD). CCD checks for collisions between steps by treating the moving object as a sphere that sweeps along its path, detecting any obstacles it might hit.

CCD is turned off by default because it uses more computing power. You should enable it only for fast-moving objects.

For best results, adjust both the motion threshold and the size of the swept sphere. Here's a simple rule of thumb: make sure the threshold and sphere size are balanced based on how fast your object moves.

{% hint style="info" %}
By enabling CCD only when needed and fine-tuning its settings, you can ensure accurate collision detection without unnecessarily slowing down your simulation.
{% endhint %}

**`CCD_Swept_Radius_Sphere`** - Sphere radius

**`CCD_Motion_Threshold`** - Distance per time step

## Restution

When responsive rigid bodies collide, contact forces come into play, altering their velocities. These forces are split into 2 components: restitution and friction.\
\
**Restitution** is a force parallel to the contact normal. Its strength hints at what the bodies might be made out of.

If both bodies were made of hard, springy steel, they might separate without loss of [kinetic energy](https://en.wikipedia.org/wiki/Kinetic\_energy), after undergoing what’s called a _perfectly elastic_ collision. If, on the other hand, both bodies were made of soft, sticky clay, they might cling together, dissipating kinetic energy and undergoing what’s called a _perfectly inelastic_ collision.

In reality, no collision is perfectly elastic. Elasticity is quantified by a _coefficient of restitution_, which ranges from zero (perfectly inelastic) to one (perfectly elastic).

In simulation, collisions are inelastic by default. Each rigid body has a _restitution parameter_, which defaults to zero. For each collision, the coefficient of restitution is calculated by multiplying the parameters of the colliding bodies.

To simulate a perfectly elastic collision, set the restitution parameters of both bodies to 1.

## Friction

While restitution models contact forces parallel to the contact normal, _friction_ models contact forces orthogonal to the contact normal.

Each rigid body has a _friction parameter_ (which defaults to 0.5). This parameter hints at the body’s surface characteristics. Reducing a body’s friction parameter makes it more slippery (think wet ice). Increasing it yields better traction (think sandpaper or dry rubber).

For each collision, a _coefficient of friction_ is calculated by multiplying the parameters of the colliding bodies.

## Factor

All forces, torques, and impulses acting on dynamic rigid bodies are multiplied by _factors_ that can be configured for each body.

## Damping

In the absence of external forces, inertia would keep the velocities of a dynamic body constant. In the real world, however, we’re accustomed to seeing unpowered moving objects eventually come to rest. This behavior is often caused by _drag forces_ (such as air resistance) that increase with speed.

To simulate drag forces, each rigid body has _damping_, which quantifies how quickly its motion decays to zero, assuming the body is dynamic.

More precisely, each body has 2 damping parameters: _linear damping_ and _angular damping_, each of which ranges from zero (no drag) to one (motion ceases immediately). Linear damping damps the linear velocity, and angular damping damps the angular velocity.

## Bounding Boxes

Is a virtual boxes that is used to represent the boundaries of an object's physical body in three-dimensional space. It defines the space occupied by the object and is used for various calculations such as collisions, intersection detection.

### [boundingbox.md](body/boundingbox.md "mention")
