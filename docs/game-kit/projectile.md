---
layout: default
title: Projectile.cs
parent: Classes
grand_parent: Game Kit
---

# Projectile.cs

## Description:
Tracks "hit points" and invokes events based on the current amount or state.

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
|  `bool` | useLifeTime | Should the GameObject be deactivated after lifeTime has elapsed. | true |
|  `float` | lifeTime | How long this projectile will live before being deactivated (in seconds). | 10 |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| Impact |  |  | `Void` |
| AddImpactListener   | Call if adding this component via script. |  | `Void` |
