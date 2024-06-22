---
description: Setting trunk system
---

# Trunk

```yaml
Trunk:
  Enable: true
  Size: 20
  Open:
    Cooldown: 1000 #mils
    Permission: ""
    Lockable: true
    Owner_Only: true
    Events:
      No_Permission:
        Mechanics: []
      Cooldown:
        Mechanics: []
      Owner_Only:
        Mechanics: []
      Open_Trunk:
        Mechanics: []
      Trunk_Is_Locked:
        Mechanics: []
  Inventory:
    Title: "&0Trunk | 20 Slots"
    Barriers:
      Enable: true
      Item:
        Material: BARRIER
        Name: "&7Unavailable slot"
        Lore: []
        Hide_Flags: true
        Stackable: true
```

## Enable

Enable/Disable this option for vehicle

## Size

The size of the trunk of the vehicle. The size can be a maximum of 54 (double trunk). If the size is not a multiple of 9, the extra slots will be blocked by a barrier



## [open-trunk.md](open-trunk.md "mention")

## [inventory-trunk.md](inventory-trunk.md "mention")
