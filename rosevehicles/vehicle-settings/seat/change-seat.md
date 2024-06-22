---
description: Configuring change seat in to vehicle
---

# Change Seat

```yaml
Change_Seat:
  Enable: true # Enable/Disable change seat
  Cooldown: 1000 # Cooldown (Milliseconds)
  Permission: "" # Permission
  Change_On_The_Driver_Seat: false # Enable change on the driver seat
  Driver_Allow_Change_Seat: false # Enable Driver allow change seat
  Events: # Events
    No_Permission:
      Mechanics:
    Cooldown:
      Mechanics: []
    No_Free_Seat:
      Mechanics: []
    Changed_Seat:
      Mechanics: []
```

## Enable

Enable/Disable change seats on vehicle

## Cooldown

Delay to prevent spamming by change seat in vehicle

## Permission

Set an permission to change seat in vehicle

## Change on the driver seat

Enable change on the driver seat

## Driver allow change seat

Allow driver change seat

## Events

Events related to the module.  [Click to get more information about events](../../events-mechanics/)

List of events:

* No permission
* Cooldown
* No free seats
* Changed seat
