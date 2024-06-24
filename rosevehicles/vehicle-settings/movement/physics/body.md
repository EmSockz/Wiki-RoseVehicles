---
description: Setting body physics
---

# Body

```yaml
  Body:
    Mass: 1550.0 #КГ.
    Collision:
      CCD_Motion_Threshold: 0.5
      CCD_Swept_Sphere_Radius: 0.8
      Restitution: 0.1 #Прыгучесть
      Friction:
        Friction: 1.0
        Rolling: 1.06
        Spinning: 1.05
      Factor:
        Angular: 0.10 #Ускорение угловой скорости
      Damping:
        Linear: 0.003 #Замедление линейной скорости
        Angular: 0.20 #Замедление угловой скорости
      Bounding_Boxes:
        box1:
          Type: BOX
          Center: "0.0 0.4 0.0"
          Width: 0.9
          Height: 0.1
          Length: 2.3
        box2:
          Type: BOX
          Center: "0.0 0.4 0.0"
          Width: 0.89
          Height: 0.2
          Length: 1.0
```

### Mass

The weight of the vehicle in kilograms.

### Continuous collision detection (CCD) <a href="#continuous_collision_detection" id="continuous_collision_detection"></a>

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

### Restitution

When responsive rigid bodies collide, contact forces come into play, altering their velocities. These forces are split into 2 components: restitution and friction.\
\
**Restitution** is a force parallel to the contact normal. Its strength hints at what the bodies might be made out of.

If both bodies were made of hard, springy steel, they might separate without loss of [kinetic energy](https://en.wikipedia.org/wiki/Kinetic\_energy), after undergoing what’s called a _perfectly elastic_ collision. If, on the other hand, both bodies were made of soft, sticky clay, they might cling together, dissipating kinetic energy and undergoing what’s called a _perfectly inelastic_ collision.

In reality, no collision is perfectly elastic. Elasticity is quantified by a _coefficient of restitution_, which ranges from zero (perfectly inelastic) to one (perfectly elastic).

In simulation, collisions are inelastic by default. (We saw this in [HelloRigidBody.java](https://github.com/stephengold/Minie/blob/master/TutorialApps/src/main/java/jme3utilities/tutorial/HelloRigidBody.java).) Each rigid body has a _restitution parameter_, which defaults to zero. For each collision, the coefficient of restitution is calculated by multiplying the parameters of the colliding bodies.

To simulate a perfectly elastic collision, set the restitution parameters of both bodies to one:\
