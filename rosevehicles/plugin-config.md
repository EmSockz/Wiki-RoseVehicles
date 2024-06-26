---
description: Plugin configuration file
---

# ⚙️ Plugin Config

```yaml
General: # General settings
  Lang: "en" # Plugin language
  Сreate_Default_Files: true # Enable/Disable create default files

Vehicle: # Vehicle settings
  Tick_Rate: 20 # The number of ticks for vehicles.

World: # World Settings
  Pickup_Items_In_Vehicles: false # Enable/Disable pickup items from ground in vehicle
  Unload_Vehicles: # Auto unload Vehicle settings
    Enable: false # Enable/Disable
    Check_Rate: 10 # Check rate (seconds)
    No_Players_in_Range: 128 # Meters
  Clear_Vehicles: # Cler vehicles settings
    Max_Removal_Radius: 2048.0 # Max Radius
  Load_Vehicles: # Load vehicles settings
    Check_Entities_In_Radius: 8.0 # Radius check sub-entities
    Use_Old_Chunk_System: false # Old chunk system (Spigot)
  Disabled_Worlds: # disabled worlds for vehicles
    - 'world1'
    - 'world2'
    - 'world3'

Entity: # Entity vehicle settings
  Hitbox_Entity: # Solid Hitbox entity
    Boat_Type: OAK # Type of boat
    Shulker_Color: RED # Color of shulker

Control: # Control settings
  F_Key: # F Key (swap hands)
    Enable: true # Enable/Disable
    Disable_Event: false # Enable/Disable event cancel
    Disable_Event_Only_In_Vehicle: true
  Q_Key: # Q Key (drop items)
    Enable: true # Enable/Disable
    Disable_Event: false # Enable/Disable event cancel
    Disable_Event_Only_In_Vehicle: true # Enable/Disable event cancel
    Fake_Item: # Fake item to send the key to server
      Material: EMERALD
      Name: ""
      Lore: []
      Stackable: false
      Custom_Model_Data: 0
      Unbreakable: true
      Hide_Flags: true
```

## General

```yaml
General: # General settings
  Lang: "en" # Plugin language
  Сreate_Default_Files: true # Enable/Disable create default files
```

**Lang** - Plugin language used (Available en, uk)\
**Сreate\_Default\_Files** - Whether to create default plugin files. Examples of vehicles, gearbox, fuel, engine. The resourcepack is always created without depending on this option
