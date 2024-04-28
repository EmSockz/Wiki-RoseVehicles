---
description: Closing and opening your vehicle
---

# Lock

```yaml
Lock:
  Enable: true # Enable/Disable lock vehicle
  Cooldown: 1000 # Cooldown (Milliseconds)
  Permission: "" # Permission
  Events: # Events
    No_Permission:
      Mechanics: []
    Cooldown:
      Mechanics: []
    Lock:
      Mechanics: []
    Unlock:
      Mechanics: []
```

## Enable

Enable or Disable this option for vehicle

## Cooldown

Delay to prevent spamming by closing/opening vehicle

## Permission

Set an permission to lock the vehicle

## Events

Events related to the module.  [Click to get more information about events](../events-mechanics/)

List of events:

* No\_Permission
* Cooldown
* Lock
* Unlock
