# Position

## Position

```yaml
Position:
  Use_Smooth_Yaw: false
  Offset:
    Offset: "x y z"
    Base_Offset: "x y z"
```

### Use Smooth Yaw

True value specifies that the entity will rotate around its yaw axis (Just as the player rotates around     himself), instead of rotating the armorstand head or display item. In some cases this may smooth out the yaw rotation

### Offset

The offset of an element relative to the vehicle position, measured in three-dimensional coordinates (x, y, z). If the offset is set incorrectly, the element may not be positioned correctly, which can lead to problems with the function and appearance of the vehicle.

#### Base Offset

The base offset of the element, which is applied at the end of the calculation and is independent of vehicle rotation, also measured in three-dimensional coordinates (x, y, z). If the base offset is set incorrectly, the element may not be placed correctly in the final position, regardless of the rotation of the vehicle.
