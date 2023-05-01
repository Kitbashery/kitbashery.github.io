---
layout: default
title: SmartGameObject.cs
parent: Classes
grand_parent: Smart GameObjects
---

# SmartGameObject.cs

### Namespace:
Kitbashery.SmartGO

## Description:
A component for managing logic, interaction and motion of a GameObject.

## Usage Notes:
 
 * Requires a GameObject with a SmartManager component to be present in the scene.

## Properties:

| Type | Property Name | Summary | Default Value |
| :--- | :--- | :--- | :--- |
| Int32 | currentBehavior |  | 0 |
| Int32 | pathProgress |  | 0 |
| Boolean | translating |  | false |
| Boolean | translationPaused |  | true |
| Vector3 | nextPosition |  |  |
| Boolean | rotating |  | false |
| Boolean | rotationPaused |  | true |
| Quaternion | nextRotation |  |  |
| Boolean | scaling |  | true |
| Boolean | scalingPaused |  | true |
| Vector3 | nextScale |  |  |
| Single | translationTime |  | 0 |
| Single | rotationTime |  | 0 |
| Single | scaleTime |  | 0 |
| `Transform` | myTransform |  | transform |
| `Dictionary`2` | floatVariableLookup |  |  |
| `Dictionary`2` | booleanVariableLookup |  |  |
| `List`1` | floatVariables |  |  |
| `List`1` | booleanVariables |  |  |
| `SmartGameObject` | focusTarget | The SmartGameObject that is being focused on. | null |
| `List`1` | targets | Other smart GameObjects this one is aware of. |  |
| `SmartGameObject` | lastTargeted |  | lastContact.gameObject.GetComponent<SmartGameObject>() |
| `SmartGameObject` | nearestTarget |  | null |
| `SmartGameObject` | farthestTarget |  | null |
| `Rigidbody` | rigid |  | GetComponent<Rigidbody>() |
| `Collider` | col |  | GetComponent<Collider>() |
| `Boolean` | isTrigger | If the SmartGameObject has a collider marked as trigger this should be true. | true |
| `Int32` | maxCollisions | The max amount of collisions to happen during a frame before collisions stop being detected. | 50 |
| `List`1` | requiredTags | Tags a collider must have in order for it to be detected. |  |
| `List`1` | ignoredColliders | Colliders to ignore (Only supported in Unity 5.5.0b3 and later). |  |
| `List`1` | colliders | All colliders currently interacting with the interaction collider. |  |
| `Collider` | lastContact | The collider that last interacted with the interaction collider. | other |
| `Collision` | lastCollision |  | collision |
| `UnityEvent` | onTriggerStay |  |  |
| `UnityEvent` | onCollisionStay |  |  |
| `UnityEvent` | onEnable |  |  |
| `UnityEvent` | onDisable |  |  |
| `RaycastHit[]` | hits |  | Physics.RaycastAll(tempRay) |
| `Int32` | rayCount | The amount of rays to cast. | 1 |
| `Single` | maxRayDistance | The length of a raycast. | 1000 |
| `Single` | raySpacing | Spacing for grid, line and circle raycast types & the size for sphere, capsule and box casts. | 1f |
| `Single` | verticalScatter | The vertical range when invoking the scatter raycast action. | 45 |
| `Single` | horizontalScatter | The horizontal range when invoking the scatter raycast action. | 45 |
| `LayerMask` | layerMask | The layer mask that the next raycast will detect objects in. | 1 |
| `QueryTriggerInteraction` | triggerInteraction | How raycasts and colliders interact with colliders marked as triggers. | QueryTriggerInteraction.Ignore |
| `NavMeshAgent` | agent | The NavMeshAgent determining motion. | GetComponent<NavMeshAgent>() |
| `Animator` | animator | The Animator determining motion. |  |
| `List`1` | splines |  |  |
| `List`1` | path |  |  |
| `Boolean` | useLocalSpace | If enabled the path will follow the GameObject in local space (this GameObject won't be allowed to follow its own path). | false |
| `Boolean` | useFocusTargetPath |  | false |
| `Boolean` | usePath | If enabled the SmartGameObject will translate along its path of splines (disabled for its own local space paths). | false |
| `Boolean` | lookAtPath | If enabled a SmartGameObject will look at the next path segment while following a path. | false |
| `AnimationCurve` | pathCurve |  | action.curve |
| `AnimationCurve` | translationCurve |  | action.curve |
| `Vector3` | translationTarget | The position to translate to during a translation tween. (world space) | action.customVector |
| `AnimationCurve` | rotationCurve |  | action.curve |
| `Quaternion` | rotationTarget | The target to rotate to during a rotation tween. | Quaternion.identity |
| `Boolean` | spin | If enabled rotation will spin around the target rotation. | false |
| `AnimationCurve` | scaleCurve |  | action.curve |
| `Vector3` | scaleTarget | The target to scale to during a scale tween. | Vector3.one |
| `Boolean` | snappyScale | If enabled scale will be rounded so the scale snaps between increments. | false |
| `Transform` | lookAtTarget | The transform to rotate toward (overrides other rotation tweens). | focusTarget.myTransform |
| `Boolean` | horizontalLook | If enabled the billboard be constrained to only looking horizontally. | false |
| `Boolean` | directLook | If enabled the billboard look directly at the target. | true |
| `AudioSource` | audioSrc |  | GetComponent<AudioSource>() |
| `GameObject` | lastSpawned |  |  |
| `RaycastTypes` | raycastDebug | Visualize approximations of raycasts based on the current raycast settings. | RaycastTypes.None |
| `Int32` | conditionType |  |  |
| `Int32` | actionType |  | 0 |

## Methods:

| Method | Summary | Parameters | Returns |
| --- | --- | --- | --- |
| get_currentBehavior |  |  | `Int32` |
| get_pathProgress |  |  | `Int32` |
| get_translating |  |  | `Boolean` |
| get_translationPaused |  |  | `Boolean` |
| get_nextPosition |  |  | `Vector3` |
| get_rotating |  |  | `Boolean` |
| get_rotationPaused |  |  | `Boolean` |
| get_nextRotation |  |  | `Quaternion` |
| get_scaling |  |  | `Boolean` |
| get_scalingPaused |  |  | `Boolean` |
| get_nextScale |  |  | `Vector3` |
| get_translationTime |  |  | `Single` |
| get_rotationTime |  |  | `Single` |
| get_scaleTime |  |  | `Single` |
| UpdateSmartGameObject |  |  | `Void` |
| EvaluateBehavior |  | `SmartBehavior` behavior "The behavior to evaluate." | `Void` |
| EvaluateDelayedBehavior |  | `SmartBehavior` behavior "The behavior to evaluate." | `IEnumerator` |
| InvokeSmartAction |  | `Action` action | `Void` |
| InvokeBooleanAction |  | `Action` action, `String` behaviorName | `Void` |
| InvokeNumericalAction |  | `Action` action, `String` behaviorName | `Void` |
| EvaluateCondition |  | `Condition` condition | `Boolean` |
| GetComponentFloatValue |  | `Int32` index, `String` variableName = , `Int32` variableID = 0 | `Single` |
| GetComponentBooleanValue |  | `Int32` index, `String` variableName = , `Int32` variableID = 0 | `Boolean` |
| PerformBooleanOperation |  | `Boolean&` leftSide, `BooleanComparisons` booleanComparison, `Boolean` rightSide | `Void` |
| PerformNumericalOperation |  | `Single&` leftSide, `NumericalOperators` numericalOperator, `Single` rightSide | `Void` |
| DisableBehavior |  | `Int32` index | `Void` |
| EnableBehavior |  | `Int32` index | `Void` |
| EnableAllBehaviors |  |  | `Void` |
| AddBehavior |  | `SmartBehavior` behavior "The behavior to evaluate." | `Void` |
| AddBehavior |  | `SmartBehaviorScriptableObject` behaviorSO | `Void` |
| GetBehavior |  | `Int32` index | `SmartBehavior` |
| SetBehavior |  | `Int32` index, `SmartBehavior` behavior "The behavior to evaluate." | `Void` |
| SetBehavior |  | `Int32` index, `SmartBehaviorScriptableObject` behaviorSO | `Void` |
| AddFloatVariable |  | `String` varName, `Single` initialValue | `Void` |
| GetFloatVariableValueByName |  | `String` name | `Single` |
| SetFloatVariableByName |  | `String` name, `Single` value | `Void` |
| ResetAllFloatVariableValues |  |  | `Void` |
| ResetAllBooleanVariableValues |  |  | `Void` |
| IgnoreColliders |  | `Collider]` ignoreList "Colliders to ignore/detect.", `Boolean` ignore "Should the colliders in the ignore list be ignored or detected? (true/false)" | `Void` |
| TargetLastContact |  |  | `Void` |
| TargetLastCollision |  |  | `Void` |
| TargetColliders |  |  | `Void` |
| RemoveNullTargets |  |  | `Void` |
| TargetCollidersWithTag |  | `String` requiredTag | `Void` |
| TargetRaycastHitsWithTag |  | `String` requiredTag | `Void` |
| TargetRaycastHits |  |  | `Void` |
| FocusOnSmartGameObject |  | `SmartGameObject` smartGO | `Void` |
| TargetSmartGameObject |  | `SmartGameObject` smartGO | `Void` |
| GetNearestTarget |  |  | `Void` |
| GetNearestTargetWithTag |  | `String` tag | `Void` |
| GetFarthestTarget |  |  | `Void` |
| GetFarthestTargetWithTag |  | `String` tag | `Void` |
| Richochet |  |  | `Void` |
| Seek |  | `Transform` target, `Single` speed | `Void` |
| UpdateRaycastHitCache |  |  | `Void` |
| RaycastSingle |  |  | `Void` |
| RaycastAll |  |  | `Void` |
| SphereCast |  |  | `Void` |
| SphereCastAll |  |  | `Void` |
| BoxCastAll |  |  | `Void` |
| BoxCast |  |  | `Void` |
| CapsuleCast |  |  | `Void` |
| LineCast |  |  | `Void` |
| RaycastScatter |  |  | `Void` |
| RaycastRow |  |  | `Void` |
| RaycastGrid |  |  | `Void` |
| RaycastCircle |  |  | `Void` |
| RaycastFan |  |  | `Void` |
| ClearTransformValues |  |  | `Void` |
| SetTransformValuesToInitial |  |  | `Void` |
| StartTranslation |  |  | `Void` |
| PauseTranslation |  |  | `Void` |
| ResumeTranslation |  |  | `Void` |
| StopTranslation |  |  | `Void` |
| StartRotation |  |  | `Void` |
| PauseRotation |  |  | `Void` |
| ResumeRotation |  |  | `Void` |
| StopRotation |  |  | `Void` |
| StartScale |  |  | `Void` |
| PauseScale |  |  | `Void` |
| ResumeScale |  |  | `Void` |
| StopScale |  |  | `Void` |
| StartPathTranslation |  |  | `Void` |
| StopPathTranslation |  |  | `Void` |
| RecalculatePath |  |  | `Void` |
| SetTranslationTarget |  | `Vector3` v3 | `Void` |
| UpdatePathPosition |  |  | `Void` |
| AIWander |  | `Single` wanderRange | `Void` |
| AIFleeFocusTarget |  | `Single` fleeDistance | `Void` |
| AIIdle |  |  | `Void` |
| AIFollowFocusTarget |  | `Single` followDistance | `Void` |
| AIFollowPath |  |  | `Void` |
| AIFollowFocusTargetPath |  |  | `Void` |
| SpawnAtTransform |  | `Transform` t, `String` poolName | `Void` |
| SpawnAtRaycastHit |  | `RaycastHit` hit, `String` poolName | `Void` |
| SpawnAtRaycastHits |  | `String` poolName | `Void` |
| SpawnAtColliders |  | `String` poolName | `Void` |
| SpawnAtTargets |  | `String` poolName | `Void` |
| DebugRootDirection |  |  | `Void` |
| DebugCurrentBehavior |  |  | `Void` |
| DebugBehavior |  | `SmartBehavior` behavior "The behavior to evaluate." | `Void` |
