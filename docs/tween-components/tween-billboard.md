---
layout: default
title: TweenBillboard.cs
parent: Classes
grand_parent: Tween Components
---

# TweenBillboard.cs

### Inherits from:
[TweenBase.cs](https://kitbashery.com/docs/tween-components/tween-base.html)

## Description:
 Rotates the transform so its forward direction faces a target `Transform`.

## Usage Notes:
 
AnimationCurves do not have an effect on the billboard.
 

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `Transform` | lookAtTarget | The transform to look at, leave blank to default to main camera. |  |
|  `bool` | horizontalAxis |  | false |
|  `bool` | directLook |  | true |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| UpdateTween |  |  | `override Void` |
