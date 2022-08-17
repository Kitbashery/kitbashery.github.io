---
layout: default
title: HealthZone.cs
parent: Classes
grand_parent: Game Kit
---

# HealthZone.cs

## Description:
Modifies the <see cref="Health"/> components of colliding <see cref="GameObject"/>s.
 
 ## Usage Notes:
 
 -Required to have RegisterTarget() called via its onEnter UnityEvent to function.
 -Required to have UnregisterTarget() called via its onExit UnityEvent to function.
 -Required to have ModifyHealth() called via its onStay UnityEvent to function.
 Call AddListeners() if HealthZone is added to a GameObject during runtime.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:--------------------|:--------------|
|  `HealthModifiers` | modifier | | HealthModifiers.damage |
|  `int` | amount | Amount of health to modify per frame. | 1, Minimum value = 0 |
|  `List<Health>` | targetHP | Health components to apply damage to. |  |
|  `Health` | lastHealth | The last health component registered/unregisterd. |  |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:--------------|:-----------|:--------|
| ModifyHealth | Health change is updated per frame to all `Health` components in the target list. | | `Void` |
| RegisterTarget | Tries to get the `Health` component of the last collider that made contact and add it to the target list.  |  | `Void` |
| UnregisterTarget | Tries to get the `Health` component of the last collider that left contact and removes it from the target list. |  | `Void` |
| AddListeners | Adds the required listeners to the `UnityEvent`s in the base class. Call if adding this component via script. | | `Void` |
