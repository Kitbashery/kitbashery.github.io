---
layout: default
title: TweenTranslate.cs
parent: Classes
grand_parent: Tween Components
---

# TweenTranslate.cs

### Inherits from:
[TweenBase.cs](https://kitbashery.com/docs/tween-components/tween-base.html)

## Description:
Translates to a destination point following a 'AnimationCurve'.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `Vector3` | target |  | `Vector3.forward` |
|  `Vector3` | nextPos | The next position the transform will be at (useful for networking/physics). |  |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| UpdateTween |  |  | `override Void` |
| MoveToTarget |  |  | `Void` |
| MoveToInitialPos |  |  | `Void` |
| SetTransformTarget |  | `Transform` t | `Void` |
| SetPositionTarget |  | `Vector3` t | `Void` |
| ResetToInitial |  |  | `Void` |
