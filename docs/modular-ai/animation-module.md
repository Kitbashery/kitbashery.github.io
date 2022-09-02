---
layout: default
title: AnimationModuleModule.cs
parent: Classes
grand_parent: Modular AI
---

# AnimationModule.cs

### Inherits from:
[AIModule.cs](https://kitbashery.com/docs/modular-ai/ai-module.html)

## Description:
This module contains actions and condtions to play animations via Unity's `Animator` component.

## Usage Notes:

The tags "Player" and "Agent" are used by this module by default make sure they exist in your project settings if you use them.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `UnityEvent` | animationEvents |  |  |
|  `Animator` | anim | The `Animator` component. |  |
|  `List<GameObject>` | players |  |  |
|  `string` | idleState |  |  |
|  `string` | walkState |  |  |
|  `string` | runState |  |  |
|  `string` | jumpState |  |  |
|  `string[]` | deathStates |  |  |
|  `int` | currentDeathState |  | -1 |
|  `string[]` | attackStates |  |  |
|  `int` | currentAttackState |  | -1 |
|  `string[]` | hitReactionStates |  |  |
|  `int` | currentHitReactionState |  | -1 |


## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| Idle |  | | `Void` |
| Walk |  | | `Void` |
| Run |  | | `Void` |
| Jump |  | | `Void` |
| Die |  | `StateOptions` option | `Void` |
| Attack |  | `StateOptions` option | `Void` |
| HitReaction |  | `StateOptions` option | `Void` |


## Enumerations:

### FocusModes

`{ Nearest, Farthest, Random, First, Last }`
