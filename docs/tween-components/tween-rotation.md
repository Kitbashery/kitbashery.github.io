---
layout: default
title: TweenRotation.cs
parent: Classes
grand_parent: Tween Components
---

# TweenRotation.cs

### Inherits from:
[TweenBase.cs](https://kitbashery.com/docs/tween-components/tween-base.html)

## Description:
Rotates to a destination rotation following a `AnimationCurve`.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `Vector3` | target | The index of the material of `TweenBase.rend` to tween from. | 0, Minimum Value = 0 |
|  `bool` | spin | Spin around target axis. | false |
|  `float` | spinSpeed |  | 1f, Range = 1-360 |
|  `Quaternion` | nextRot | The next rotation the transform will be at (usefull for networking/physics). |  |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| UpdateTween |  |  | `override Void` |
| RotateToTarget |  |  | `Void` |
| RotateToInitialPos |  |  | `Void` |
| SetTransformTarget |  | `Transform` t | `Void` |
| SetRotationTarget |  | `Quaternion` t | `Void` |
| ResetToInitial |  |  | `Void` |
