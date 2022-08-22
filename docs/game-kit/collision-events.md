---
layout: default
title: CollisionEvents.cs
parent: Classes
grand_parent: Game Kit
---

# CollisionEvents.cs

## Description:
A wrapper for `MonoBehaviour`'s built-in physics methods adding conditional constrains and events.

## Usage Notes:
 
Ignoring colliders is only Supported in Unity 5.5.0b3 and later.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `bool` | isTrigger | Use trigger events (true/false). | `true` |
|  `int` | maxCollisions | Events will not be invoked if there are more collisions taking place than the maximum. | 50, Minimum value = 1 |
|  `List<string>` | requiredTags | Tags a collider must have in order for events to be invoked. |  |
|  `List<Collider>` | ignoredColliders | Colliders to ignore when the script is intialized (Only Supported in Unity 5.5.0b3 and later). |  |
|  `UnityEvent` | enterEvent |  |  |
|  `UnityEvent` | exitEvent |  |  |
|  `UnityEvent` | stayEvent |  |  |
|  `Collider` | lastContact | The collider that last interacted with the event collider. |  |
|  `Collision` | lastCollision | The last collision that occured. |  |
|  `List<Collider>` | colliders | All colliders currently interacting with the collision event collider. |  |
|  `Collider` | eventCollider | The collider used to detect collision events (Found when Awake() is called). |  |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| IgnoreColliders | Tells the physics engine to ignore/detect collisions between a list of colliders and the `eventCollider`. | List<Collider> ignoreList "Colliders to ignore/detect.", bool ignore "Should the colliders in the ignore list be ignored or detected? (true/false)" | `Void` |
| EventContainsListenerWithMethod | Used in the Unity editor to check if a `UnityEvent` contains a listener with a certain method.  | UnityEvent uEvent "The `UnityEvent` to check for a listener in.", string methodName "The name of the method to check for." | `bool` "true if an event contains a listener with methodName". |
| DebugCollisionCount   |  |  | `Void` |
| DebugLastCollision   |  |  | `Void` |
