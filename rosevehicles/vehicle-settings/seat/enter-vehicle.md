---
description: Configuring enter in to vehicle
---

# Enter Vehicle

```yaml
Enter_Vehicle:
  Sit_Seat_Clicked: true # Enable/Disable sit seat clicked
  Events: # Events
    Vehicle_Is_Locked:
      Mechanics: []
    Seat_Is_Taken:
      Mechanics: []
    Enter_Vehicle:
      Mechanics: []
```

## Sit Seat Clicked

**True** - the player sits on the seat he clicked\
False - the player sits on an free seat

## Events

Events related to the module.  [Click to get more information about events](../../events-mechanics/)

List of events:

* Vehicle\_Is\_Locked
* Seat\_Is\_Taken
* Enter\_Vehicle
