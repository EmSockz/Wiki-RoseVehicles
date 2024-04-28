---
description: Setting seat for you vehicle
---

# Seat

```yaml
Seat:
  Eject_Spectators: true #Eject Spectators
  Enter_Vehicle:
    Sit_Seat_Clicked: true
    Events:
      Vehicle_Is_Locked:
        Mechanics: []
      Seat_Is_Taken:
        Mechanics: []
      Enter_Vehicle:
        Mechanics: []
        
  Leave_Vehicle:
    Events:
      Leave_Vehicle:
        Mechanics: []
        
  Change_Seat:
    Enable: true
    Cooldown: 1000 #mils
    Permission: ""
    Change_The_Driver_Seat: false
    Driver_Change_Seat: false
    Events:
      No_Permission:
        Mechanics: []
      Cooldown:
        Mechanics: []
      No_Free_Seat:
        Mechanics: []
      Changed_Seat:
        Mechanics: []
```

## Eject Spectators

Whether to eject players who go into Spectator GameMode

## [Enter Vehicle](enter-vehicle.md)

## [Leave Vehicle](leave-vehicle.md)

## [Change Seat](change-seat.md)
