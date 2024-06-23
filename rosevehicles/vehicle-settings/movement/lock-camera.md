---
description: Settings camera for passengers
---

# Lock the Camera

Passenger camera settings. The plugin allows you to lock the camera in a specific position relative to the vehicle or limit its rotation.

```yaml
Lock_The_Camera:
  Enable: true
  Seats:
    seat_1:
      Start_Rotation: "0.0 0.0"
      Min_Rotation: "0.0 -115.0"
      Max_Rotation: "0.0 115.0"
    seat_2:
      Start_Rotation: "0.0 0.0"
      Min_Rotation: "0.0 0.0"
      Max_Rotation: "0.0 0.0"
    seat_3:
      Start_Rotation: "0.0 0.0"
      Min_Rotation: "0.0 0.0"
      Max_Rotation: "0.0 0.0"
    seat_4:
      Start_Rotation: "0.0 0.0"
      Min_Rotation: "0.0 0.0"
      Max_Rotation: "0.0 0.0"
  Look_Camera:
    Enable: true
  Interpolation:
    Enable: true
    Amount: 1.0
```

## Enable

Enable/Disable this option

## Seats

Setting up each seat. <mark style="color:yellow;">**Notice**</mark> that the seat must match the name of the seat in [Components](../components.md)

### &#x20;   Start Rotation

&#x20;    The starting position of the camera.\
&#x20;    `Start_Rotation: "pitch yaw"`

### &#x20;   Min Rotation

&#x20;    Minimum allowed angle of rotation of the camera.\
&#x20;    `Min_Rotation: "pitch yaw"`

### &#x20;   Max Rotation

&#x20;    Maximum allowed angle of rotation of the camera.\
&#x20;    `Max_Rotation: "pitch yaw"`

## Lock Camera

Lock the rotation of the camera in relation to the rotation of the vehicle

## Interpolation

Camera rotation smoothing.
