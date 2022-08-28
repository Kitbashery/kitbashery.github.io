---
layout: default
title: Game Kit PDF
nav_exclude: true
---

# GameKit

## Description:
GameKit contains feature rich systems and components commonly used in games. Designed with 3D games in mind, however some components may function in 2D as well.

### Namespace:
Kitbashery.Gameplay

## Features:

#### Object pooling:
* Improves game performace
* Sequencial naming
* Hide pooled GameObjects in the inspector
* Expandable pools.

#### Spawner:
* Forward & offset spawn direction
* Integrated object pooling
* Spawn events
* Wave system
* Random spawns

#### Health:
* Invinsibility
* Multiple healthbars
* Passive regenration
* Damage/healing
* Stackable effects over time
* Damage/heal/death Events
* Area of effect zones
* Healthbar UI support

#### Projectiles:
* Impact force
* Seeking
* Ricochets
* Integrated with health system
* Integrated object pooling

#### Event Systems:
* Dynamic collision events
* Dynamic activation events
* Integrated with health system
* Integrated with projectiles


# CLASSES:


# ActivationEvents.cs

## Description:
Exposes `UnityEvent`s to the inspector that are invoked during their corralating activation messages.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `UnityEvent` | onAwake | Called when a script instance is being loaded. |  |
|  `UnityEvent` | onStart | Called before the first frame update. |  |
|  `UnityEvent` | onEnable | Called when the object becomes active and enabled. |  |
|  `UnityEvent` | onDisable | Called when the object becomes disabled or inactive. |  |
|  `UnityEvent` | onDestroy | Called when the MonoBehaviour will be destroyed. |  |



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
  
  
# Health.cs

## Description:
Tracks "hit points" and invokes events based on the current amount or state.

## Usage Notes:

Bonus Health should not be set to its own `health` component.

Tip: Lowercase fields in the inspector can be set via UnityEvents.
 

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `bool` | invinsible |  | `false` |
|  `Health` | bonusHealth | If assigned the hitpoints of the bonus health will need to be depleted before damage can be applied to this health component. |  |
|  `int` | hitPoints | The hitpoints to start with, it isn't recommended to modify this value directly during runtime, use ModifyHealth() instead. | 100, Minimum value = 0 |
|  `bool` | overhealExpand | Should the maximum hit points be expanded if healed beyond maxHitPoints? | false |
|  `bool` | canRegen | Enables passive health regeneration. | false |
|  `int` | regenPoints | Hitpoints to regenerate. | 1, Minimum value = 1 |
|  `float` | regenRate | Time between regenerating hitpoints (in seconds). | 0.1, Minimum value = 0.01 |
|  `UnityEvent` | onReceivedDamage |  |  |
|  `UnityEvent` | onHealed |  |  |
|  `UnityEvent` | onDead |  |  |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| ModifyHealth |  | HealthModifiers modifier, int amount | `Void` |
| ModifyHealthOverTime   | Starts a `TimedHealthEffect` that will modify health over time. | `TimedHealthEffect` effect | `Void` |
| StopTimedEffectsWithModifier |  Stops all timed health effects that use a specific health modifier.  | `HealthModifiers` modifier | `Void` |
| StopTimedHealthEffect | Stops a specific health effect by its `TimedHealthEffect` name.  | `string` effectName | `Void` |
| StopAllTimedHealthEffects |  |  | `Void` |
| ApplyDamage | Applies damage, if there is bonus health damage will be applied to that component first. | `int` amount "The amount of damage to apply". | `Void` |
| ClearRegenCooldown | Instantly regenerates hitpoints if canRegen is true. |  | `void` |
| Heal | Instantly heals the specified amount of hitpoints. | `int` amount "The amount of hitpoints to heal". | `void` |
| ResetHealth | Resets the hitpoints of all health and (optionally) all bonus health components in the chain to their original values. Useful for pooling. | `bool` resetBonusHealth "If true will reset the bonus health recursively until no bonus health is found." Default value = `false` | `Void` |
| SetMaxHitpoints | Overrides the initial hitpoint value and adjusts the current hitpoints to fit within the new range. | `int` amount "The new max value of hitpoints". | `void` |
| IsLessThanHalfHealth | Checks if the amount of hitpoints is below 50% of the intial value. | | `bool` "true if hitpoints are below 50%". |
| TimedEffectsPlaying | Checks if there are any heal/damage over time effects being apllied. |  | `bool` "true if there are effect playing". |
| HasTimedHealthEffect | Checks if there is a specific timed health effect playing. | `string` effectName "The name of the effect to check for". | `bool` "true if an effect is found". |
| DebugTimedEffectCount |  |  | `void` |
| DebugCurrentHealth |  |  | `void` |


## Structs:

### `[Serializable]` TimedHealthEffect
#### Public Properties:

| Type        | Name | Description | Default Value |
|:------------|:----|:-------------|:--------------|
|  `string` | name | The name of the effect, used for stopping effects with this name. |  |
|  `int` | amount | The amount of healing or damage to apply. | Minumum value = 1 |
|  `int` | times | The amount of times to modify health. | Minumum value = 1 |
|  `float` | interval | Time interval in seconds between modifying health. | Minumum value = 0 |

## Enumerations:

### HealthModifiers

`{ damage, heal }`
  
# HealthZone.cs

### Inherits from:
[CollisionEvents.cs](https://kitbashery.com/docs/game-kit/collision-events.html)

## Description:
Modifies the `Health`components of colliding `GameObject`s.

## Usage Notes:
 
 * Required to have RegisterTarget() called via its onEnter UnityEvent to function.
 * Required to have UnregisterTarget() called via its onExit UnityEvent to function.
 * Required to have ModifyHealth() called via its onStay UnityEvent to function.

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
  

# ObjectPools.cs

## Description:
A singleton class for managing multiple pools of GameObjects.


## Usage Examples:

From external script you can get a GameObject from the pool via a prefab name or a known index of ObjectPool.pools

 ```csharp
public void Spawn()
{
     GameObject go = ObjectPools.Instance.GetPooledObject("MyPrefabName");
     go.transform.position = Vector3.Zero;
     //Do other things to the GameObject...
     go.SetActive(true);
}
 ```
 Alternatively:
  ```csharp
public void Spawn()
{
     ObjectPools.Instance.ActivatePooledObject("MyPrefabName");
}
 ```
 
 
## Usage Notes:
 
It is recommended to access the ObjectPool instance after Awake() is called, 
otherwise modify the script execution order so your script is loaded after ObjectPool.cs
 

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `public static ObjectPool` | Instance |  |  |
|  `public List<Pool>` | pools | A non-reorderable list of Pools. |  |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| CreatePools |  | | `Void` |
| PopulatePools   |   |  | `Void` |
| ExpandPools      |    | `Pool pool, int amount` | `Void` |
| DestroyPools | Destroys all objects in all pools.  | `bool omitActive` "Preserve pooled GameObjects that are currently active in the scene". | `Void` |
| ActivatePooledObject |  | `int index` | `Void` |
| ActivatePooledObject |  | `string prefabName` | `Void` |
| GetPooledObject | Gets a pooled GameObject by the index of its pool. | `int index` "The index of a pool in pools". | `GameObject` "The first inactive prefab instance". |
| GetPooledObject | Gets a pooled GameObject by its prefab name. | `string prefabName` "The name of the prefab to get an instance of". | `GameObject` "The first inactive prefab instance". |
| CreatePools |  |  | `Void` |


## Structs:

### `[Serializable]` Pool
#### Public Properties:

| Type        | Name | Description | Default Value |
|:------------|:----|:-------------|:--------------|
|  `GameObject` | prefab | The GameObject to pool. |  |
|  `int` | amount | The initial amount of GameObjects to instantiate. | Minumum value = 1 |
|  `HideFlags` | hideFlags | HideFlags for prefabs instantiated via the pooling system. Useful for hiding pooled objects in the heirarchy. |  |
|  `bool` | sequencialNaming | Use numbered names for GameObjects instead of name(clone). | false |
|  `List<GameObject>` | pooledObjects | The GameObjects currently pooled. |  |


### `[Serializable]` PoolID
#### Public Properties:

| Type        | Name | Description | Default Value |
|:------------|:-----|:----------- |:--------------|
|  `int` | poolIndex | The index of a pool in the ObjectPools instance pool list. | Minumum value = 0 |
|  `string` | prefabName | If specified the spawner will try to get GameObjects from the pool by the prefab name instead of index. | |
  
# Projectile.cs

### Inherits from:
[CollisionEvents.cs](https://kitbashery.com/docs/game-kit/collision-events.html)

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
|  `QueryTriggerInteraction` | triggerInteraction | How should the projectile interact with trigger colliders? | QueryTriggerInteraction.Ignore |
|  `RaycastHit[]` | hits | Raycast hits collected when the projectile searches for targets to seek. |  |
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
  
# Spawner.cs

## Description:
Enables `GameObjects` pooled by `ObjectPools` in sequential waves.

## Usage Notes:
 
Tip: Lowercase fields in the inspector can be set via UnityEvents.
 

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `bool` | canSpawn |  | `false` |
|  `bool` | spawnForward | Spawned GameObjects will be positioned in the direction the spawner is facing. | `false` |
|  `float` | forwardDistance | How far forward to spawn a GameObject (if Spawn Forward is checked). | 0 |
|  `Vector3` | spawnOffset |  |  |
|  `List<Wave>` | waves | Sequential information on what pool to spawn GameObjects from, how often and how many. |  |
|  `GameObject` | lastSpawned |  |  |
|  `int` | currentWave | | 0, Minimum value = 0 |
|  `int` | currentWaveSpawns | | 0, Minimum value = 0 |
|  `UnityEvent` | onHealed |  |  |
|  `UnityEvent` | onDead |  |  |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| DelaySpawn |  | `float` time | `Void` |
| SetWave   |  | `int` wave | `Void` |
| RandomizeWave |  Randomizes the spawns of a wave.  | `Wave` wave "The wave to randomize". | `Wave` "The wave with randomized spawns". |
| RandomizeWaves | Randomizes all waves that have randomWaves set to true.  |  | `Void` |
| DebugCurrentWave |  |  | `Void` |
| RandomizeSpawnOffset |  | `float` radius | `Void` |

## Structs:

### `[Serializable]` Wave
#### Public Properties:

| Type        | Name | Description | Default Value |
|:------------|:----|:-------------|:--------------|
|  `float` | interval | Time in seconds between spawns. | Minumum value = 0 |
|  `UnityEvent` | onSpawn |  |  |
|  `UnityEvent` | onWaveComplete |  |  |
|  `List<PoolID>` | poolIdentifiers | Defines the prefabs to enable from a pool during this wave. |  |
|  `bool` | randomizeWaves | Should spawns be randomized? (used instead of poolIdentifiers). |  |
|  `int` | spawnAmount | The amount of spawns in this wave. |  |
|  `List<int>` | randomPools | Pool indices to select spawns from. |  |
