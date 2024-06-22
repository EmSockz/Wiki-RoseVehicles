---
description: Setting Engine Sound
---

# Engine Sound

```yaml
Sound:
  Enable: true
  Volume:
    Max_Volume: 2.5
    Min_Volume: 0.5
  Range:
    Default_Range: 40
    Min_Range_Mult: 1.0
    Max_Range_Mult: 3.0
  Pitch:
    Min_Pitch: 1.0
    Max_Pitch: 1.2
  Max_Sub_Sound: 100
  Sound:
    Name: "vehicle.engine."
    Category: AMBIENT
    Duration: 190
```

## Enable

Enable/Disable use engine sound

## Volume

Setting the volume of the sound. The higher the engine rpm, the higher the sound volume

## Range

Setting the range of the sound. The higher the engine rpm, the more far away the sound is hearable.

### &#x20;   Default Range

&#x20;    Default sound range at minimum rpm

## Pitch

Setting the pitch of the sound. The higher the engine speed, the higher the pitch of the sound. Note that in Minecraft the maximum sound pitch is 2.0. [Read more about pitch](https://minecraft.wiki/w/Commands/playsound)

## Max Sub Sound

Maximum number of special vehicle engine sounds

Due to the peculiarity of minecraft, the plugin can not stop the player a specific engine sound that comes from a specific vehicle. The plugin offers to create identical sounds in the sounds.json file, which will differ by the number at the end (id).

```json
"vehicle.engine.0":               {"sounds": ["vehicles/engine"]},
"vehicle.engine.1":               {"sounds": ["vehicles/engine"]},
"vehicle.engine.2":               {"sounds": ["vehicles/engine"]},
"vehicle.engine.3":               {"sounds": ["vehicles/engine"]},
"vehicle.engine.4":               {"sounds": ["vehicles/engine"]},
```

## Sound

### &#x20;   Name

&#x20;    Sound name from sounds.json

### &#x20;   Category

&#x20;    Sound Category. [Available categories of sounds](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/SoundCategory.html)

### &#x20;   Duration

&#x20;    Sound duration in milliseconds
