---
layout: default
title: PatrolRoute.cs
parent: Classes
grand_parent: Modular AI
---

# PatrolRoute.cs

## Description:
Defines a patrol route relative to its parent `Transform`.

## Usage Notes:

An AI agent's behaviour loop is updated by an instance of `AIManager` if a manager instance is not found one will be created.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `Vector3[]` | waypoints | Waypoints that define a patrol route in the order they should be navigated to. Note: waypoints are fixed positions in world space. |  |
|  `Vector3[]` | route | The patrol route relative to it's transform (waypoints in local space). Note: route move with the transform. |  |
|  `RaycastHit[]` | hits | Hits chached when randomizing waypoints. |  |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| RefreshPatrolRoute | Refreshes the patrol route based on the current waypoint and transform position. |  | `Void` |
| RandomizeWaypoints | `float` radius, `float` maxDistance, `LayerMask` mask, `QueryTriggerInteraction` triggerInteraction |  | `Void` |

## Enumerations:

### PatrolTypes

`{ loop, pingPong, randomize }`

## Gizmo Preview:

![](../../assets/images/kitbashery-patrol-route-gizmo.jpg)
