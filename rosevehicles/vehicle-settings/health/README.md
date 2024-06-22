---
description: Setting health system vehicle
---

# Health

```yaml
Health:
  Enable: true
  Max_Health: 250.0
  Start_Health: 250.0
  Events:
    Explosive:
      Mechanics:
        - RemoveVehicle{delay="0", conditions=[]}
    Damage_Vehicle:    
      Mechanics: []
  Damage:
    Push_Vehicle:
      Enable: true
      Relative_Damage: false
      Coefficient: 0.05
  Regeneration:
    Enable: true
    HP_Per_Regen: 1.0
    Ticks_Between_Regen: 20
    Ticks_Before_Start: 600
    Events:
      Regeneration:
        Mechanics: []
```

## Enable

Enable or Disable this option for vehicle

## Max Health

The amount of maximum HP a vehicle can have

## Start Health

The starting amount of HP a vehicle has when it is created.

## Events

Events related to the module.  [Click to get more information about events](../../events-mechanics/)

List of events:

* Explosive
* Damage vehicle



## [damage.md](damage.md "mention")

## [regeneration.md](regeneration.md "mention")
