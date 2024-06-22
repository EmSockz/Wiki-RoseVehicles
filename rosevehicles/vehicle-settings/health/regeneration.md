---
description: Setting vehicle regeneration system
---

# Regeneration

```yaml
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

## HP Per Regeneration

The amount of added HP  per regen

## Ticks Between Regen

Time between regenerations _(in ticks)_

## Ticks Before Start

The time that must have elapsed since the last time the vehicles took damage to start regenerating\
&#x20;_(in ticks)_



## Events

Events related to the module.  [Click to get more information about events](../../events-mechanics/)

List of events:

* Regeneration
