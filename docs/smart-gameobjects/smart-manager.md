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
| Boolean | useGUILayout |  |  |
| Boolean | runInEditMode |  |  |
| Boolean | allowPrefabModeInPlayMode |  |  |
| Boolean | enabled |  |  |
| Boolean | isActiveAndEnabled |  |  |
| Transform | transform |  |  |
| GameObject | gameObject |  |  |
| String | tag |  |  |
| Component | rigidbody |  |  |
| Component | rigidbody2D |  |  |
| Component | camera |  |  |
| Component | light |  |  |
| Component | animation |  |  |
| Component | constantForce |  |  |
| Component | renderer |  |  |
| Component | audio |  |  |
| Component | networkView |  |  |
| Component | collider |  |  |
| Component | collider2D |  |  |
| Component | hingeJoint |  |  |
| Component | particleSystem |  |  |
| String | name |  |  |
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
| IsInvoking |  |  | `Boolean` |
| CancelInvoke |  |  | `Void` |
| Invoke |  | `String` methodName, `Single` time | `Void` |
| InvokeRepeating |  | `String` methodName, `Single` time, `Single` repeatRate | `Void` |
| CancelInvoke |  | `String` methodName | `Void` |
| IsInvoking |  | `String` methodName | `Boolean` |
| StartCoroutine |  | `String` methodName | `Coroutine` |
| StartCoroutine |  | `String` methodName, `Object` value | `Coroutine` |
| StartCoroutine |  | `IEnumerator` routine | `Coroutine` |
| StartCoroutine_Auto |  | `IEnumerator` routine | `Coroutine` |
| StopCoroutine |  | `IEnumerator` routine | `Void` |
| StopCoroutine |  | `Coroutine` routine | `Void` |
| StopCoroutine |  | `String` methodName | `Void` |
| StopAllCoroutines |  |  | `Void` |
| get_useGUILayout |  |  | `Boolean` |
| set_useGUILayout |  | `Boolean` value | `Void` |
| get_runInEditMode |  |  | `Boolean` |
| set_runInEditMode |  | `Boolean` value | `Void` |
| get_enabled |  |  | `Boolean` |
| set_enabled |  | `Boolean` value | `Void` |
| get_isActiveAndEnabled |  |  | `Boolean` |
| get_transform |  |  | `Transform` |
| get_gameObject |  |  | `GameObject` |
| GetComponent |  | `Type` type | `Component` |
| GetComponent |  |  | `T` |
| TryGetComponent |  | `Type` type, `Component&` component | `Boolean` |
| TryGetComponent |  | `T&` component | `Boolean` |
| GetComponent |  | `String` type | `Component` |
| GetComponentInChildren |  | `Type` t, `Boolean` includeInactive | `Component` |
| GetComponentInChildren |  | `Type` t | `Component` |
| GetComponentInChildren |  | `Boolean` includeInactive | `T` |
| GetComponentInChildren |  |  | `T` |
| GetComponentsInChildren |  | `Type` t, `Boolean` includeInactive | `Component[]` |
| GetComponentsInChildren |  | `Type` t | `Component[]` |
| GetComponentsInChildren |  | `Boolean` includeInactive | `T[]` |
| GetComponentsInChildren |  | `Boolean` includeInactive, `List`1[T]` result | `Void` |
| GetComponentsInChildren |  |  | `T[]` |
| GetComponentsInChildren |  | `List`1[T]` results | `Void` |
| GetComponentInParent |  | `Type` t, `Boolean` includeInactive | `Component` |
| GetComponentInParent |  | `Type` t | `Component` |
| GetComponentInParent |  | `Boolean` includeInactive | `T` |
| GetComponentInParent |  |  | `T` |
| GetComponentsInParent |  | `Type` t, `Boolean` includeInactive | `Component[]` |
| GetComponentsInParent |  | `Type` t | `Component[]` |
| GetComponentsInParent |  | `Boolean` includeInactive | `T[]` |
| GetComponentsInParent |  | `Boolean` includeInactive, `List`1[T]` results | `Void` |
| GetComponentsInParent |  |  | `T[]` |
| GetComponents |  | `Type` type | `Component[]` |
| GetComponents |  | `Type` type, `Component]` results | `Void` |
| GetComponents |  | `List`1[T]` results | `Void` |
| get_tag |  |  | `String` |
| set_tag |  | `String` value | `Void` |
| GetComponents |  |  | `T[]` |
| CompareTag |  | `String` tag | `Boolean` |
| SendMessageUpwards |  | `String` methodName, `Object` value, `SendMessageOptions` options | `Void` |
| SendMessageUpwards |  | `String` methodName, `Object` value | `Void` |
| SendMessageUpwards |  | `String` methodName | `Void` |
| SendMessageUpwards |  | `String` methodName, `SendMessageOptions` options | `Void` |
| SendMessage |  | `String` methodName, `Object` value | `Void` |
| SendMessage |  | `String` methodName | `Void` |
| SendMessage |  | `String` methodName, `Object` value, `SendMessageOptions` options | `Void` |
| SendMessage |  | `String` methodName, `SendMessageOptions` options | `Void` |
| BroadcastMessage |  | `String` methodName, `Object` parameter, `SendMessageOptions` options | `Void` |
| BroadcastMessage |  | `String` methodName, `Object` parameter | `Void` |
| BroadcastMessage |  | `String` methodName | `Void` |
| BroadcastMessage |  | `String` methodName, `SendMessageOptions` options | `Void` |
| get_rigidbody |  |  | `Component` |
| get_rigidbody2D |  |  | `Component` |
| get_camera |  |  | `Component` |
| get_light |  |  | `Component` |
| get_animation |  |  | `Component` |
| get_constantForce |  |  | `Component` |
| get_renderer |  |  | `Component` |
| get_audio |  |  | `Component` |
| get_networkView |  |  | `Component` |
| get_collider |  |  | `Component` |
| get_collider2D |  |  | `Component` |
| get_hingeJoint |  |  | `Component` |
| get_particleSystem |  |  | `Component` |
| GetInstanceID |  |  | `Int32` |
| GetHashCode |  |  | `Int32` |
| Equals |  | `Object` other | `Boolean` |
| get_name |  |  | `String` |
| set_name |  | `String` value | `Void` |
| get_hideFlags |  |  | `HideFlags` |
| set_hideFlags |  | `HideFlags` value | `Void` |
| ToString |  |  | `String` |
| GetType |  |  | `Type` |

