---
description: Settings physics wheels for vehicle
---

# Wheels

```yaml
Wheels:
  Default_Settings:
    Radius: 0.8
    Model_Radius: 0.35
    Width: 0.3
    Axle_Direction: "-1 0 0"
    Steering: UNUSED
    Engine_Fraction: 0.2
    Friction_Slip: 1.0
    Roll_Influence: 0.5
    Brake: 1000
    Skid:
      Start_When: 0.1
      Particles:
        - "CAMPFIRE_SIGNAL_SMOKE 3 0.0 0.0 0.0 0.0"
    Suspension:
      Max_Force: 5000.0
      Rest_Length: 0.4
      Stiffness: 2.3
      Max_Travel: 1400.0
      Direction: "0.0 -1.0 0.0"
      Damping:
        Compression: 0.5
        Relaxation: 0.4
    Rotate:
      Enable: false
      Speed: 0.0
      Speed_Reset: 0.0
      Max_Angle: 0.0

  wheel_1:
    Offset: "0.86 0.0 1.75"
    Steering: UNUSED
    Brake: 500
    Rotate:
      Enable: true
      Max_Angle: 38.0

  wheel_2:
    Offset: "-0.86 0.0 1.75"
    Steering: UNUSED
    Brake: 500
    Rotate:
      Enable: true
      Max_Angle: 38.0

  wheel_3:
    Offset: "0.86 0.0 -1.75"
    Brake: 1000
    Steering: DIRECT

  wheel_4:
    Offset: "-0.86 0.0 -1.75"
    Brake: 1000
    Steering: DIRECT
```

Set the physical parameters of each wheel. Default Settings are the settings that will be applied to the wheel if these parameters are missing. Each wheel must have the same name as in [Components](../components/)

## Radius, Model Radius, Width

Setting the radius of the wheel. In the realities of minecraft it should be a bit larger than in the real world, simply because the world of minecraft is made of cubes. Model Radius should specify the radius of the wheel in the context of the model, you need this parameter to correctly calculate the wheel animation

## Offset

The offset of the wheel relative to the center of the vehicle, measured in three-dimensional coordinates (x, y, z). If the offset is set incorrectly, the wheel may not be positioned correctly, which can lead to problems with vehicle handling and stability.

## Axle Direction

The axis direction (in chassis coordinates, not null, unaffected, typically right/-1,0,0)

## Steering

Setting wheel type. Types:\
\
**DIRECT -** steering left turns the wheel leftward (and vice versa), for example the front wheels of most passenger cars

**FLIPPED** - steering left turns the wheel rightward (and vice versa), for example in active 4-wheel steering systems

**UNUSED -** the wheel isn't steered, for example the rear wheels of most passenger cars

## Engine Fraction

How much the engine affects the wheel. Useful for setting up the vehicle drive system

## Friction Slip

The _`friction slip`_ parameter quantifies how much traction a tire has. Its effect is most noticeable when the vehicle is braking.

Too much traction could cause a vehicle to flip over if it braked hard. Too little traction would make braking ineffective, as if the tires were bald or the supporting surface were icy.

The default value for friction slip is `10.5`

## Roll influence

The _roll-influence factor_ reduces (or magnifies) torques that tend to cause vehicles to roll over.

The default value of 0.5 yields realistic behavior. Reducing this parameter will improve stability, but it’s a bit of a hack; use it only as a last resort.

## Brake

Setting the braking force of the wheel

## Skid Marks

Setting the appearance of smoke from the wheels. Start When: \[0.0-1.0] Smoke threshold, this specifies the level of wheel skid in percent.\
\
**Particles:**

[Particle Serialize](../../serializers/particle-serializer.md)

## Suspension

Setting the suspension of the vehicle.

### Maximum Force

A vehicle’s _suspension_ connects its wheels to its chassis and supports the weight of the chassis. If the maximum suspension force is set too low, the suspension will collapse, causing the chassis to scrape the ground.

The default maximum suspension force is 6000 per wheel. For a vehicle with 4 wheels and a mass of 3000, the default is inadequate for a gravitational acceleration of 8 or more, even if the weight of the chassis is distributed evenly among the wheels.

If the weight is distributed unevenly, some of the maxima might need to be increased even more.

### Rest Length

_Rest length_ is the length of a spring when no force is applied to it. If the suspension’s rest lengths are too large, the chassis will seem to be jacked up on stilts and the vehicle will be prone to tipping, even when not moving.

### Stiffness

_Stiffness_ is the force exerted by a spring divided by its change in length. If the suspension is too stiff, a small bump could cause the vehicle to bounce violently. If it isn’t stiff enough, a large bump could cause the chassis to "bottom out".

### Max Travel

The desired maximum amount the suspension can be compressed or expanded, relative to its rest length (in hundredths of a physics-space unit, Default value - 500 cm)

### Direction

Suspension direction. default is down (0 -1 0). Format - `Direction: "x y z"`

### Damping

Each wheel has 2 suspension damping parameters, one for expansion and one for compression. The range of plausible values depends on the suspension stiffness, according to the formula in the javadoc:

```java
damping = 2 * k * FastMath.sqrt(stiffness);
```

where k is the suspension’s _damping ratio_:

* k = 0: undamped and bouncy.
* k = 1: critically damped.

Good values of k are between 0.1 and 0.3.

The default damping parameters of 0.83 and 0.88 are suitable for a chassis with the default stiffness of 5.88 (k=0.171 and 0.181, respectively). If you override the default stiffness, you should override the damping parameters as well.

## Rotate

Setting the wheel rotation

### Enable

Option that specifies whether wheel rotation is enabled. Default value: `false`

### Rotate Speed

The rate at which the wheel rotates, measured in degrees per second (deg/sec). If the rotation speed is set too low, the wheel will rotate slowly or not at all. Default value: `0.0`

### Rotate Speed Reset

The speed at which the wheel returns to the starting position, measured in degrees per second (deg/sec). If the return speed is set too low, the wheel will return to the starting position slowly, which may affect the handling of the vehicle. Default value: `0.0`

### Max Angle

The maximum steering angle of the wheel, measured in degrees (deg). If the maximum steering angle is set too low, it will be difficult for the wheel to turn enough to steer the vehicle effectively. Default value: `0.0`
