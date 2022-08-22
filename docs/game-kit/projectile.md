---
layout: default
title: Projectile.cs
parent: Classes
grand_parent: Game Kit
---

# Projectile.cs

## Description:
A physics based projectile.

## Usage Notes:
 
Requires that Impact() gets called by the base class onEnter() UnityEvent.

A `Rigidbody` reference is required for the field "rigid" and will be assigned automatically if none is found.

If adding the component via script be sure to call AddImpactListener().
 

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `Rigidbody` | rigid |  |  |
|  `bool` | applyForceOnImpact | Should force be applied to the hit rigidbody? | true |
|  `float` | impactForce | Force applied to the rigidbody of hit colliders. | 1 |
|  `float` | velocity | Initial velocity of the rigidbody. | 500 |
|  `bool` | modifyHealthOnImpact | Should health be modified on impact? | false |
|  `TimedHealthEffect` | healthEffect |  |  |
|  `bool` | disableOnImpact | Should the projectile be disabled on impact? (useful for pooling). | true |
|  `int` | ricochets | How many times should the projectile be allowed to bounce before it can be disabled? | 0, Minimum value = 0 |
|  `bool` | useLifeTime | Should the GameObject be deactivated after lifeTime has elapsed. | true |
|  `float` | lifeTime | How long this projectile will live before being deactivated (in seconds). | 10 |
|  `bool` | seekTarget |  | false |
|  `Transform` | target |  |  |
|  `TargetModes` | targetMode | Determines how a target should be selected if target is not initially defined. | TargetModes.targetFirst |
|  `LayerMask` | layerMask | The layer(s) to search for a target in. |  |
|  `string` | targetTag | The tag required for a GameObject to be set as a target. (leave blank if you don't need this). |  |
|  `float` | searchRange | The range to search for a target in. | 10 |
|  `float` | seekSpeed | The speed at which the projectile will travel to the target. | 10 |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| Impact |  |  | `Void` |
| AddImpactListener   | Call if adding this component via script. |  | `Void` |
| FindBestTarget   | Finds the best target for the projectile to seek to. |  | `Void` |

## Enumerations:

### TargetModes

`{ targetFirst, targetNearest, targetFarthest }`
