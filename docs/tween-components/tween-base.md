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
| UpdateTween |  |  | `Void` |
| DelayTween   | Disables movement untill parameter "time" has elapsed. | `float` time | `Void` |
| ResetTweenState |  Sets the tweens state back to its initial state with a delay if it has one.  |  | `Void` |
| IsVisibleToMainCamera |   |  | `bool` |
| DebugRootDirection |  |  | `Void` |
| ReverseCurve | Reverses the animation curve |  | `Void` |
| LinearCurve | Sets the tween to use a linear animation curve. |  | `void` |
| FlattenCurve | Sets the tween to use a constant flat animation curve. | `float` value | `void` |
