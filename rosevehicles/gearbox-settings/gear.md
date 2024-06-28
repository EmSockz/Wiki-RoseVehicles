# Gear

```yaml
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
```

Title sections _(exmp -  reverse, low, 5th)_ are not used in the code. Neutral gear is not specified in the config

### ID

The gear number used to identify the vehicle's current gear. This parameter determines which gear the vehicle is in and can be used for various functions, such as changing the driving mode.

### Name

Display name of the gear. Used for placeholder work

### Speed

**Downshift** - The speed at which the gear reduction is performed.\
**Upshift** - The speed at which the gears are increased.\
**Redline** - The maximum speed for a given gear after which the engine operates at maximum speed.
