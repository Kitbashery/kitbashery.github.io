---
layout: default
title: TimedHealthEffect
parent: Structs
grand_parent: Game Kit
---

# `[Serializable]` TimedHealthEffect

## Part of Health.cs

### Public Properties:

| Type        | Name | Description | Default Value |
|:------------|:----|:-------------|:--------------|
|  `string` | name | The name of the effect, used for stopping effects with this name. |  |
|  `int` | amount | The amount of healing or damage to apply. | Minumum value = 1 |
|  `int` | times | The amount of times to modify health. | Minumum value = 1 |
|  `float` | interval | Time interval in seconds between modifying health. | Minumum value = 0 |
