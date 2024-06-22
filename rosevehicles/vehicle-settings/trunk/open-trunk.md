---
description: Setting open system
---

# Open Trunk

```yaml
Open:
  Cooldown: 1000
  Permission: ""
  Lockable: true
  Owner_Only: true
  Events:
    No_Permission:
      Mechanics: []
    Cooldown:
      Mechanics: []
    Owner_Only:
      Mechanics: []
    Open_Trunk:
      Mechanics: []
    Trunk_Is_Locked:
      Mechanics: []
```

## Cooldown

Delay to prevent spamming by opening/closing trunk

## Permission

Set an permission to open trunk the vehicle

## Lockable ([Lock](../lock.md))

Whether to close the trunk together with the vehicle doors

## Owner Only

Allow only the owner of the vehicle to open trunk



## Events

Events related to the module.  [Click to get more information about events](../../events-mechanics/)

List of events:

* No permission
* Cooldown
* Owner only
* Open trunk
* Trunk is locked
