---
description: Pickup vehicle in the game
---

# Pickup

```yaml
Pickup:
  Enable: true # Enable pickup vehicle
  Permission: "" # Permission for pickup vehicle
  Owner_Only: true # Allow only the owner of the vehicle to pick it up
  Events: # Events related to the module
    No_Permission:
      Mechanics: []
    Owner_Only:
      Mechanics: []
    Pickup_Vehicle:
      Mechanics: []
```

## Enable

Enable/Disable this option for vehicle

## Permission

Set an permission to pickup the vehicle

## Owner Only

Allow only the owner of the vehicle to pickup

## Events

Events related to the module.  [Click to get more information about events](../events-mechanics/)

List of events:

* No Permission
* Owner Only
* Pickup Vehicle
