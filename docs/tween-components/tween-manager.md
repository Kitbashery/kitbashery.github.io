---
layout: default
title: TweenManager.cs
parent: Classes
grand_parent: Tween Components
---

# TweenManager.cs

## Description:
Consolidates `TweenBase` update loops improving performance.

## Usage Notes:
 
* Lowercase fields in the inspector can be set via UnityEvents.
 

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `static TweenManager` | Instance |  |  |
|  `bool` | pauseTweens | Pauses all tweens. | false |
|  `List<TweenBase>` | tweens |  | true |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| Move |  | `TweenBase` tween | `Void` |
| Register |  | `TweenBase` tween | `Void` |
| Unregister |  | `TweenBase` tween | `Void` |
