---
description: Setting fuel system
---

# Fuel

```yaml
Fuel:
  Enable: true
  Type: example_fuel
  Consumption: 1.5
  Fuel_Tank_Size: 50.0
  Start_Fuel: 20.0
  Refueling:
    Permission: ""
    Owner_Only: true
  Events:
    No_Permission:
      Mechanics: []
    Owner_Only:
      Mechanics: []
    Refueling:
      Mechanics: []
```

## Enable

Enable/Disable this option for vehicle

## Type

Type of vehicle fuel. See [fuel-settings.md](../../fuel-settings.md "mention")

## Consumption

Fuel consumption per 1,000 blocks. In liters

## Fuel Tank Size

The maximum amount of fuel that can be stored in the vehicle.

## Start Fuel

The starting amount of fuel a vehicle has when it is created.

## Events

Events related to the module.  [Click to get more information about events](../../events-mechanics/)

List of events:

* No permission
* Owner only
* Refueling



## [refueling.md](refueling.md "mention")
