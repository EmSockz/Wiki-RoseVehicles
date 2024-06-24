---
description: Setting deactivation physics
---

# Sleep

```yaml
Sleep:
  Enable: true
  Sleeping_Start_Time: 2.0
  Sleeping_Thresholds:
    Linear: 0.8
    Angular: 1.0
```

Deactivation of vehicle physics is necessary for optimization. Vehicles stop calculating physics if they don't have collisions for some time. The physics will be activated if the vehicle has collisions again

## Enable

Enable/Disable this option

## Sleeping Start Time

Time in seconds before physics deactivation starts

## Sleeping Thresholds

The threshold after which physics is activated.
