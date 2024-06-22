---
description: Allows you to make a list of banned/allowed blocks for vehicle place
---

# Blocks

```yaml
Place:
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

## Type

Type of list. BLACKLIST or WHITELIST

## White\_List, Black\_List

List of blocks

## Events

Events related to the module. [Click to get more information about events](../../events-mechanics/)

List of events:

* Block in whitelist
* No block in whitelist
* Block in blacklist
* No block in blacklist

