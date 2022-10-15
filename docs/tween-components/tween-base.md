---
layout: default
title: TweenBase.cs
parent: Classes
grand_parent: Tween Components
---

# TweenBase.cs

## Description:
Base class for all tween components.

## Usage Notes:

Tip: Lowercase fields in the inspector can be set via UnityEvents.
 

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `bool` | tweening | Is the tween allowed to move? | true |
|  `bool` | useFixedUpdate | Check this if you are tweening a rigidbody. | false |
|  `bool` | tweeningAtStart | The starting state of tweening. | false |
|  `bool` | tweenWhenVisible | Only tween if the render is visible to the main camera. | false |
|  `Renderer` | rend | The renderer that if visible allows movement. (also used in material tweening). |  |
|  `Camera` | visibilityCam |  |  |
|  `float` | startDelay | Time in seconds untill the tween starts playing. | 0, Minimum value = 0 |
|  `float` | lerpTime |  | 0 |
|  `AnimationCurve` | curve | | `AnimationCurve.Linear(0, 0, 1, 1)` |
|  `WrapMode` | wrapMode |  | `WrapMode.PingPong` |
|  `UnityEvent` | onTweenComplete | Called each time a tween reaches its current target. |  |
|  `bool` | pauseAtTime | Should this tween pause when lerpTime reaches pauseTime? | false |
|  `float` | pauseTime | The time the next pause will occur. | 0 |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| UpdateTween |  |  | `Void` |
| DelayTween   | Disables movement untill parameter "time" has elapsed. | `float` time | `Void` |
| PauseTweenAtTime | Pauses the tween at the specified time in its curve. | `float` time "The time in the animation curve to stop the tween." | `void` |
| ResetTweenState |  Sets the tweens state back to its initial state with a delay if it has one.  |  | `Void` |
| IsVisibleToMainCamera |   |  | `bool` |
| DebugRootDirection |  |  | `Void` |
| ReverseCurve | Reverses the animation curve |  | `Void` |
| LinearCurve | Sets the tween to use a linear animation curve. |  | `void` |
| FlattenCurve | Sets the tween to use a constant flat animation curve. | `float` value | `void` |
