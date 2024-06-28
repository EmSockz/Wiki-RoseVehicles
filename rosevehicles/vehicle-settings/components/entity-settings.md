# Entity Settings

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

**Type** - Entity type. Available variants: `ARMOR_STAND, ITEM_DISPLAY`

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
      Brightness:
        Block_Light: 8
        Sky_Light: 8
    Armor_Stand:
      Marker: true
      Small: false
</code></pre>

Display entities are used to display the model. You can use only the ArmorStand or the ItemDisplay

**Type** - Entity type. Available variants: `ARMOR_STAND, ITEM_DISPLAY`

**Model** - The model used for this entity. The model is taken from [Models](../models.md)

**Rotation** - Default entity rotation. Accepts parameter: `Rotation: "pitch yaw roll"`

\+[ Item Display entity settings](entity-settings.md#item-display-1.19.4)

\+ [Armor Stand entity settings](entity-settings.md#armor-stand)

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

The plugin allows you to create two types of hitboxes per entity. - Interaction and solid. Solid hitboxes are created by creating a boat or a shalker. interaction by creating a new entity in 1.19.4

\+ [Interaction entity settings](entity-settings.md#interaction-1.19.4)

\+ [Solid entity settings](entity-settings.md#solid)

## Entity Settings

### Armor Stand

```yaml
Armor_Stand:
  Marker: true
  Small: false
```

**Marker** - Removes the hitbox from the entity.\
**Small** - The value **true** means that a small ArmorStand is used. **false** - big

### Item Display (1.19.4+)

```yaml
Item_Display:
  Scale: "1.0 1.0 1.0"
  Translation: "0.0 0.0 0.0"
  View_Range: 128
  Shadow_Radius: 4
  Shadow_Strength: 0
  Transform: HEAD
  Interpolation_Duration: 3
  Teleport_Duration: 3
```

**Scale** - ItemDisplay model scale. Scale is not limited. \
accepts this parameter: `Scale: "width heigth length"`

**Translation** - Model offset relative to the entity location.\
accepts this parameter: `Translation: "x y z"`

**View\_Range** - The distance in meters at which the entity can be seen

**Shadow\_Radius** - shadow radius of the shadow that emanates from the entity

**Shadow\_Strength** - the power of the shadow that emanates from the entity. if the value is 0, the shadow does not emanate.

**Transform** - Represents the item model transform to be applied to the displayed item. [Transforms](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/entity/ItemDisplay.ItemDisplayTransform.html)

**Interpolation\_Duration** - Time in ticks for which a smooth change of model rotation occurs.

**Teleport\_Duration** - The time in ticks for which a smooth teleportation of an entity (movement) occurs

### Interaction (1.19.4+)

```yaml
Interaction:
  Width: 1.0
  Height: 2.0
```

Interaction - an entity that was added in snapshot 1.19.4 that is a configurable non-solid hitbox to which you can bind an interaction.

### Solid

In minecraft, there are two entities that have such a hitbox that you can fully stand on - the boat and the shalker. If you put these entities on another entity, it will be possible to use them on fractional coordinates. The plugin provides such an opportunity to create solid hitboxes. That is, the transport will be solid as a block. But in the movement will occur dips under the entity so it will work fully if the transport is not moving.

The plugin provides two types of hitboxes - Slab and Block (Boat and Shalker)

```yaml
Solid:
  Type: BLOCK/SLAB
```
