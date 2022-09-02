---
layout: default
title: SensorModule.cs
parent: Classes
grand_parent: Modular AI
---

# SensorModule.cs

### Inherits from:
[AIModule.cs](https://kitbashery.com/docs/modular-ai/ai-module.html)

## Description:
This module defines actions and conditions for a `AIAgent` to be able to detect `GameObject`s in the environment.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `bool` | debugMode | Toggles debug mode for displaying gizmos when the agent is selected. | false |
|  `Transform` | eyes | Where to start the ray from when scanning via raycasts. |  |
|  `MemoryModule` | memory |  |  |
|  `LayerMask` | layerMask | Layers to scan for objects on. | -1 |
|  `QueryTriggerInteraction` | triggerInteraction | Should trigger colliders be ignored? See QueryTriggerInteraction in the Unity Manual. | QueryTriggerInteraction.Ignore |
|  `SensorTypes` | sensorType |  | SensorTypes.sphere |
|  `float` | scanRange | The scan range or bounds of the AI's sensor; A minium of twice the NavMeshAgent's height is recommended. | 4 |
|  `float` | scanInterval | Determines the delay between scans. | 0 |
|  `List<string>` | searchFilterTags | Scans of the environment will only add GameObjects with these tags to memory. |  |
|  `bool` | clearOldMemory | Determines if any existing memory should be cleared before each new scan. (may increase performance, but be careful that clearing memory doesn't impact gameplay) | false |



## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| Scan | Scans for `GameObject`s in the scene. | `ScanTypes` scanType | `Void` |


## Enumerations:

### SensorTypes

`{ sphere, box, ray, _2D_circle, _2D_box, _2D_line }`

### ScanTypes

`{ environment, players, agents, environmentFiltered }`
