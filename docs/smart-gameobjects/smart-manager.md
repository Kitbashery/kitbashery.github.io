---
layout: default
title: SmartManager.cs
parent: Classes
grand_parent: Smart GameObjects
---

# SmartManager.cs

### Namespace:
Kitbashery.SmartGO

## Description:
A component for managing & optimizing SmartGameObjects in the scene. 

## Usage Notes:
 
 * Required for SmartGameObject components to automatically update.

## Properties:

| Type | Property Name | Summary | Default Value |
| --- | --- | --- | --- |
| HideFlags | hideFlags |  | pool.hideFlags |
| `SmartManager` | Singleton |  | this |
| `Single` | currentFPS | The time between the manager's last frame update and the current one. | 0 |
| `Dictionary`2` | delays |  |  |


## Methods:

| Method | Summary | Parameters | Returns |
| --- | --- | --- | --- |
| Register |  | `SmartGameObject` smartGO "The <see cref="SmartGameObject"/> to register." | `Void` |
| Unregister |  | `SmartGameObject` smartGO "The <see cref="SmartGameObject"/> to register." | `Void` |
| RegisterAll |  |  | `Void` |
| PauseSmartGameObjects |  | `Boolean` state "The state to se <see cref="pauseUpdates"/> to." | `Void` |
| TogglePauseSmartGameObjects |  |  | `Void` |
| ThrottleSmartGameObjectUpdates |  | `Boolean` state "The state to se <see cref="pauseUpdates"/> to." | `Void` |
| ToggleSmartGameObjectUpdateThrottle |  |  | `Void` |
| CreatePools |  |  | `Void` |
| ExpandPool |  | `String` prefabName "The name of the pool to increase the amount of (same as the pool's prefab name).", `Int32` amount "The amount to increase the pool's amount by (will only increase to the max amount set in the inspector)." | `Void` |
| DestroyPools |  | `Boolean` omitActive "Preserve pooled GameObjects that are currently active in the scene." | `Void` |
| ActivatePooledObject |  | `String` prefabName "The name of the pool to increase the amount of (same as the pool's prefab name)." | `Void` |
| GetPooledObject |  | `String` prefabName "The name of the pool to increase the amount of (same as the pool's prefab name)." | `GameObject` |
