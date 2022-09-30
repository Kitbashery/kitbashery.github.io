---
layout: default
title: ForceField.cs
parent: Classes
grand_parent: Game Kit
---

# ForceField.cs

### Inherits from:
[CollisionEvents.cs](https://kitbashery.com/docs/game-kit/collision-events.html)

## Description:
Applys force to `Rigidbody`s within its bounds.

## Usage Notes:
 
 * Required to have `isTrigger` marked as true and for its collider to be a trigger.
 * Required to have RegisterRigidbody() called via its onEnter UnityEvent to function.
 * Required to have UnregisterRigidbody() called via its onExit UnityEvent to function.

 Call AddListeners() if HealthZone is added to a GameObject during runtime.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:--------------------|:--------------|
|  `List<Rigidbody>` | rigidbodies | |  |
|  `ForceModes` | mode | | ForceTypes.directional |
|  `float` | force |  | 10 |
|  `Vector3` | forceDirection |  | Vector3.forward |
|  `WindZone` | wind | WindZone component that the force field syncs to if set to use the wind ForceMode. |  |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:--------------|:-----------|:--------|
| RegisterRigidbody |   |  | `Void` |
| UnregisterRigidbody |  |  | `Void` |

## Enumerations:

### ForceTypes

`{ wind, directional, explode, implode }`
