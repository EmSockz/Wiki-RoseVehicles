---
description: Place vehicle in game
---

# Place

```yaml
Place:
  Enable: true # Enable place vehicle
  Permission: "" # Permission allow place vehicle
  Events: # Events
    No_Permission:
      Mechanics: []
    Place_Vehicle:
      Mechanics: []
  Blocks: 
    Enable: false # Enable filter blocks
    Type: WHITELIST # Type list (WHITELIST or BLACKLIST)
    White_List: # Block list
      - GRASS
    Black_List: # Block list
      - STONE
    Events: # Events
      Block_In_Whitelist:
        Mechanics: []
      No_Block_In_Whitelist:
        Mechanics: []
      Block_In_Blacklist:
        Mechanics: []
      No_Block_In_Blacklist:
        Mechanics: []
```

## Enable

Enable/Disable this option for vehicle

## Permission

Allows you to set an permission to place the vehicle\


## Events

Events related to the module.  [Click to get more information about events](../../events-mechanics/)

List of events:

* No\_Permission
* Place\_Vehicle

## Blocks

Use the [Blocks ](blocks.md)wiki page.



