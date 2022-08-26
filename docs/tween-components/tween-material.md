---
layout: default
title: TweenMaterial.cs
parent: Classes
grand_parent: Tween Components
---

# TweenMaterial.cs

### Inherits from:
[TweenBase.cs](https://kitbashery.com/docs/tween-components/tween-base.html)

## Description:
Interpolates between two `Material`s following a `AnimationCurve`.

## Usage Notes:
 
AnimationCurves do not have an effect on the billboard.
 

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `int` | index | The index of the material of `TweenBase.rend` to tween from. | 0, Minimum Value = 0 |
|  `Material` | initialMaterial | The starting material. |  |
|  `Material` | targetMaterial | The target material to tween to. (Call UpdateTargetMaterial to change during runtime). |  |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| UpdateTween |  |  | `override Void` |
| UpdateTargetMaterial |  |  | `Void` |
| ResetToInitial |  |  | `Void` |
