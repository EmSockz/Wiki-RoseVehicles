---
description: Configuring vehicle entities (components)
---

# Components

```yaml
Components:
  Skin:
    example_entity:
      Position:
        Use_Smooth_Yaw: false
        Offset:
          Offset: "x y z"
          Base_Offset: "x y z"
        Entities:
          example_entity: <Entity>
          example_entity_base:
            Type: ARMOR_STAND
            Armor_Stand:
              Small: true
              Marker: true
          example_entity_hitbox:
            Solids:
              solid:
                Type: BLOCK
  Seats: <Components>
  Wheels: <Components>
  Trunks: <Components>
  Fuel_Tanks: <Components>
```

