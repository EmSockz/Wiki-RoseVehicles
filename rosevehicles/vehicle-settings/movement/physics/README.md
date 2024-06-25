---
description: Settings physics for vehicle
---

# Physics

```yaml
Physics:
  Sleep:
    Enable: true
    Sleeping_Start_Time: 2.0
    Sleeping_Thresholds:
      Linear: 0.8
      Angular: 1.0
  Body:
    Mass: 1550.0
    Collision:
      CCD_Motion_Threshold: 0.5
      CCD_Swept_Sphere_Radius: 0.8
      Restitution: 0.1
      Friction:
        Friction: 1.0
        Rolling: 1.06
        Spinning: 1.05
      Factor:
        Angular: 0.10
        Linear: 0.0
      Damping:
        Linear: 0.003
        Angular: 0.20
      Bounding_Boxes:
        box1:
          Type: BOX
          Center: "0.0 0.4 0.0"
          Width: 0.9
          Height: 0.1
          Length: 2.3
        box2:
          Type: BOX
          Center: "0.0 0.4 0.0"
          Width: 0.89
          Height: 0.2
          Length: 1.0
```



## [sleep.md](sleep.md "mention")

## [body.md](body.md "mention")
