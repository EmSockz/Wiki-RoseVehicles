---
description: Setting BoundingBox
---

# BoundingBox

```yaml
example_box:
  Center: "0.0 0.0 0.0"
  Width: 1.0
  Height: 0.5
  Length: 2.0

example_box_two:
  Center: "0.0 0.0 -2.0"
  Min: "-1.0 -0.5 -2.0"
  Max: "1.0 0.5 2.0"
```

Is a virtual box that is used to represent the boundaries of an object's physical body in three-dimensional space. It defines the space occupied by the object and is used for various calculations such as collisions, intersection detection.

### Center

The point that will be considered the center of this BoundingBox.

`Center: "x y z"`

### Width, Height, Length

BoundingBox width height and length.

### Min and Max point

You can use the minimum and maximum points instead of Width, Height, Length to create the BoundingBox.
