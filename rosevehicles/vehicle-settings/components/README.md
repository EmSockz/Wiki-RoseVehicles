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
          
  Seats:
    example_seat:
      Seat:
        Fix_Player_Rotate: true
        Player_Mount_On_Entity: base
        Exit_Position: "1.0 0.1 0.0"
      Position: <Position>
      Entities: <Entities>
      
  Wheels:
    example_wheel:
      Wheel:
        Rotation:
          Enable: true
        Animation:
          Enable: true
      Position: <Position>
      Entities: <Entities>
      
  Trunks: 
    example_trunk:
      Position: <Position>
      Entities: <Entities>
      
  Fuel_Tanks:
    example_fuel_tank:
      Position: <Position>
      Entities: <Entities>
```

### [position.md](position.md "mention")

### [entity-settings.md](entity-settings.md "mention")

## Seat Component

```yaml
example_seat:
  Seat:
    Fix_Player_Rotate: true
    Player_Mount_On_Entity: base
    Exit_Position: "1.0 0.1 0.0"
```

**Fix Player Rotate** - Fixes visual bug of player's body rotation when the player is sitting in a vehicle

**Player Mount on Entity** - Defines which entity the player will mount to. By the default base (base entity)

**Exit Position** - The position to which the player will be teleported when leaving the transport. The position is relative to the position of the seat and the rotation of the vehicle. Note that if the position will be filled by a block, the player will be in the seat position.                                                                      Accepts parameter: `Exit_Position: "x y z"`

## Wheel Component

```yaml
example_wheel:
  Wheel:
    Rotation:
      Enable: true
    Animation:
      Enable: true
```

### Rotation

**Enable** -Enable or disable wheel rotation display

### Animation

**Enable** - Enable or disable wheel spin animation&#x20;
