---
description: GearBoxes settings
---

# 📟 Gearbox Settings

```yaml
example_car_gearbox:
  Name: "Example Car Gearbox"
  Forward_Gears: 5
  Reverse_Gears: 1
  Gears:
    reverse:
      ID: -1
      Name: "-1"
      Speed:
        Downshift: 0.0
        Upshift: -35.0
        Redline: -40.0
    low:
      ID: 1
      Name: "1"
      Speed:
        Downshift: 0.0
        Upshift: 15.0
        Redline: 20.0
    2nd:
      ID: 2
      Name: "2"
      Speed:
        Downshift: 5.0
        Upshift: 30.0
        Redline: 35.0
    3rd:
      ID: 3
      Name: "3"
      Speed:
        Downshift: 25.0
        Upshift: 50.0
        Redline: 65.0
    4th:
      ID: 4
      Name: "4"
      Speed:
        Downshift: 45.0
        Upshift: 70.0
        Redline: 85.0
    5th:
      ID: 5
      Name: "5"
      Speed:
        Downshift: 65.0
        Upshift: 90.0
        Redline: 105.0
```

### Name

Displayed name of the gearbox in placeholders

### Forward and Reverse Gears

Number of forward and reverse gears

### Gears

Setting the gears. Title sections _(exmp -  reverse, low, 5th)_ are not used in the code.

[Gear Settings](gear.md)
