---
description: Settings physics for vehicle
---

# Physics

```yaml
Physics:
  Sleep:
    Enable: true
    Sleeping_Start_Time: 2.0
    Sleeping_Thresholds: #Порог после которого активируется физика.
      Linear: 3.8
      Angular: 3.1
  Body:
    Mass: 1550.0 #КГ.
    Collision:
      CCD_Motion_Threshold: 0.5
      CCD_Swept_Sphere_Radius: 0.8
      Restitution: 0.1 #Прыгучесть
      Friction:
        Friction: 1.0
        Rolling: 1.06
        Spinning: 1.05
      Factor:
        Angular: 0.10 #Ускорение угловой скорости
      Damping:
        Linear: 0.003 #Замедление линейной скорости
        Angular: 0.20 #Замедление угловой скорости
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
