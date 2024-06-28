---
description: Setting control for vehicle
---

# Control

```yaml
Control:
  Toggle_Lock:
    Key: Q
    Permission:
      Only_Driver: false
      Only_Owner: false
      Ignore_Driver: true
      Ignore_Owner: true
    Component:
      Click_On_Component: false
      Ignore_Click_On_Component: true
      Components: []
    Seat:
      Seated: true
      Ignore_Seated: false
      Seats:
        - 1
        - 2
  Lock:
    Key: NONE
  Unlock:
    Key: NONE
  Honk:
    Key: NONE
  Place_Vehicle:
    Key: NONE
  Pickup_Vehicle:
    Key: NONE
  Enter_Vehicle:
    Key: NONE
  Open_Trunk:
    Key: NONE
  Refueling_Vehicle:
    Key: NONE
  Change_Seat:
    Key: NONE
  Toggle_Engine:
    Key: NONE
  Start_Engine:
    Key: NONE
  Stop_Engine:
    Key: NONE
  Toggle_Parking_Brake:
    Key: NONE
  Enable_Parking_Brake:
    Key: NONE
  Disable_Parking_Brake:
    Key: NONE
```

In the plugin there are many actions with the vehicle (for example, start the engine, lock the doors, open the trunk) to which it is possible to bind their keys, conditions.

<table><thead><tr><th width="212">Action Name</th><th>Description</th><th data-hidden></th></tr></thead><tbody><tr><td>Toggle Lock</td><td>Switching the lock and unlocking of the doors and trunk (<a href="trunk/open-trunk.md#lockable-lock">optional</a>)</td><td></td></tr><tr><td>Lock</td><td>Locking the doors and trunk (<a href="trunk/open-trunk.md#lockable-lock">optional</a>)</td><td></td></tr><tr><td>Unlock</td><td>Unlocking the doors and trunk (<a href="trunk/open-trunk.md#lockable-lock">optional</a>)</td><td></td></tr><tr><td>Honk</td><td>Played honk. <a href="honk.md">See more</a></td><td></td></tr><tr><td>Place Vehicle</td><td>Place vehicle. (!) <strong>Seats</strong>, <strong>Component</strong> section not work this.</td><td></td></tr><tr><td>Pickup Vehicle</td><td>Pickup vehicle.</td><td></td></tr><tr><td>Enter Vehicle</td><td>Enter the vehicl. (!) <strong>Seats</strong> section not work this</td><td></td></tr><tr><td>Open Trunk</td><td>Open the trunk</td><td></td></tr><tr><td>Refueling Vehicle</td><td>Refueling the vehicle</td><td></td></tr><tr><td>Change Seat</td><td>Switch between vehicle seats</td><td></td></tr><tr><td>Toggle Engine</td><td>Toggle engine, start or stop</td><td></td></tr><tr><td>Start Engine</td><td>Start engine</td><td></td></tr><tr><td>Stop Engine</td><td>Stop engine</td><td></td></tr><tr><td>Toggle Parking Brake</td><td>Toggle parking brake</td><td></td></tr><tr><td>Enable Parking Brake</td><td>Enable parking brake</td><td></td></tr><tr><td>Disable Parking Brake</td><td>Disable parking brake</td><td></td></tr></tbody></table>

###

### Key

```yaml
Example_Action:
  Key: NONE
```

Available keys:&#x20;

<table><thead><tr><th width="158">Key Name</th><th>Description</th><th data-hidden></th></tr></thead><tbody><tr><td>NONE</td><td>Means that this action is disabled</td><td></td></tr><tr><td>F</td><td>Swap hands key</td><td></td></tr><tr><td>Q</td><td>Drop the item (!) Works if the player is holding the item. <a href="../plugin-config.md">See more</a></td><td></td></tr><tr><td>LMB</td><td>Clicking the left mouse button</td><td></td></tr><tr><td>RMB</td><td>Clicking the right mouse button</td><td></td></tr><tr><td>SHIFT_RMB</td><td>Clicking the left mouse button + Press Shift</td><td></td></tr><tr><td>SHIFT_LMB</td><td>Clicking the right mouse button + Press Shift</td><td></td></tr><tr><td>SHIFT_F</td><td>Swap hands key + Press Shift</td><td></td></tr><tr><td>SHIFT_Q</td><td>Drop the item + Press Shift</td><td></td></tr><tr><td><del>SHIFT</del></td><td><del>Press shift</del></td><td></td></tr><tr><td>SPACE</td><td>Press Space (!) Work only if player seated</td><td></td></tr></tbody></table>

###

### Permission

Conditions or permissions that will be checked when the required key is pressed

```yaml
Permission:
  Only_Driver: false
  Only_Owner: false
  Ignore_Driver: true
  Ignore_Owner: true
```

**Only\_Driver** - Only the driver can perform the action

**Only\_Owner** - Only the owner can perform the action

**Ignore\_Driver** - Whether to ignore the parameter `Only_Driver`

**Ignore\_Owner** - Whether to ignore the parameter `Only_Owner`

### Component

Conditions related to components that will be checked when the key is pressed

```yaml
Component:
  Click_On_Component: false
  Ignore_Click_On_Component: true
  Components: []
```

**Click\_On\_Component** - Defines whether binding interaction with the vehicle component is required

**Ignore\_Click\_On\_Component** - Whether to ignore the parameter `Click_On_Component`

**Components** - List of components that need to be interacted with to perform an action. Example:

```yaml
Components:
  - example_seat_1
  - example_seat_2
  - example_seat_3
  - example_seat_4
  
Components: ALL
```

`Components: ALL` - means that all components are used



### Seat

Conditions related to seat that will be checked when the key is pressed

```yaml
Seat:
  Seated: true
  Ignore_Seated: false
  Seats:
    - 1
    - 2
```

**Seated** - Defines whether the player must be sitting in the seat

**Ignore\_Seated** - Whether to ignore the parameter `Seated`

**Seats** - a list of seats consisting of seat numbers that must be interacted with to perform the action. Example:

```yaml
Seats:
  - 1
  - 2
  
Seats: ALL
```

`Seats: ALL` - means that all seats are used
