---
description: Setting Movement for vehicle
---

# Movement

```yaml
Movement:
  Lock_The_Camera: <Lock Camera Settings>
  Physics: <Physics Settings>
  Wheels: <Wheel Settings>
  Events:
    Engine:
      Enable: false
      Repeat_Every_Ticks: 10
      Mechanics: []
    Engine_Start:
      Mechanics:
        - CustomSound{sound="vehicle.engine.start", volume="1.0", min_volume="0.0", range="32.0", pitch="0.1", noise="0.1", category=PLAYERS, delay="0", conditions=[], listener=Location}
    Engine_Stop:
      Mechanics:
        - CustomSound{sound="vehicle.engine.stop", volume="1.0", min_volume="0.0", range="16.0", pitch="0.1", noise="0.1", category=PLAYERS, delay="0", conditions=[], listener=Location}
    Vehicle_Sunken:
      Mechanics:
        - SetEngine{enable_engine=false}
        - RemovePassengers{}
    Vehicle_UnSunken:
      Mechanics: []
    Collision_Upside_Down:
      Mechanics:
        - RemovePassengers{}
        - CustomSound{sound="vehicle.damage", volume="1.0", min_volume="0.0", range="32.0", pitch="0.1", noise="0.1", category=PLAYERS, delay="0", conditions=[], listener=Location}
    Collision_Upside_Up:
      Mechanics: []
    Collision_Hit:
      Mechanics:
        - CustomSound{sound="vehicle.damage", volume="1.0", min_volume="0.0", range="32.0", pitch="0.1", noise="0.1", category=PLAYERS, delay="0", conditions=[], listener=Location}
```
