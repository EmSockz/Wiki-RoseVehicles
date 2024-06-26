---
description: Configuring vehicle entities (components)
---

# Components

```yaml
Components:
  Skin:
    example_entity_skin:
      Position:
        Use_Smooth_Yaw: false
        Offset:
          Offset: "x y z"
          Base_Offset: "x y z"
      Entities:
        Base: <Entity>
        Displays: <Display Entities>
        Hitboxes:
          Interactions: <Interact Entities>
          Solid: <Solid Entities>
  Wheels: <Components>
  Trunks: <Components>
  Fuel_Tanks: <Components>
```

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

## Base

```yaml
Base:
  Type: ITEM_DISPLAY/ARMOR_STAND
  Item_Display:
    Scale: "1.0 1.0 1.0"
    Translation: "0.0 0.0 0.0"
    View_Range: 128
    Shadow_Radius: 4
    Shadow_Strength: 0
    Transform: HEAD
    Interpolation_Duration: 3
    Teleport_Duration: 3
  Armor_Stand:
    Marker: true
    Small: false
```

An entity that functions as a base for other sub-entities. It is used by other entities as passengers. This technique is necessary to optimize process and to fix the ItemDisplay feature. If no base entity is specified, the base entity will be redefined to another entity

## Displays

<pre class="language-yaml"><code class="lang-yaml"><strong># Example Display Entity
</strong>Displays:
<strong>  example_display_entity:
</strong>    Type: ITEM_DISPLAY/ARMOR_STAND
    Model: example_model
    Rotation: "0.0 0.0 0.0"
    Item_Display:
      Scale: "1.0 1.0 1.0"
      Translation: "0.0 0.0 0.0"
      View_Range: 128
      Shadow_Radius: 4
      Shadow_Strength: 0
      Transform: HEAD
      Interpolation_Duration: 3
      Teleport_Duration: 3
    Armor_Stand:
      Marker: true
      Small: false
</code></pre>

Display entities are used to display the model. You can use only the armorstand or the display entity



## Hitboxes

```yaml
HitBoxes:
  Solids:
    example_solid:
      Type: BLOCK/SLAB
  Interactions:
    example_hitbox:
      Width: 1.0
      Height: 2.0
```
