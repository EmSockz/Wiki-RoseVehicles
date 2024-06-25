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
    Suspension: #Подвеска
      Max_Force: 5000.0 #Сила подвески
      Rest_Length: 0.4 #Длина подвески
      Stiffness: 2.3 #Жесткость подвески.
      Max_Travel: 1400.0 #Максимальный ход подвески в см.
      Direction: "0.0 -1.0 0.0" #Направление подвески
      Damping: #демпфирование подвески колеса
        Compression: 0.5 #Демпфирование колеса при сжатии подвески
        Relaxation: 0.4 #Демпфирование колеса при расширении подвески
    Rotate: #Поворот колеса
      Enable: false #Включен ли поворот колеса
      Speed: 0.0 #deg/sec Скорость поворота
      Speed_Reset: 0.0 #deg/sec Скорость возвращения колеса
      Max_Angle: 0.0 #deg Максимальный поворот

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

Set the physical parameters of each wheel. Default Settings are the settings that will be applied to the wheel if these parameters are missing. Each wheel must have the same name as in [Components](../components.md)

## Radius, Model Radius, Width

Setting the radius of the wheel. In the realities of minecraft it should be a bit larger than in the real world, simply because the world of minecraft is made of cubes. Model Radius should specify the radius of the wheel in the context of the model, you need this parameter to correctly calculate the wheel animation

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

