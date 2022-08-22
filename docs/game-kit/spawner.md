---
layout: default
title: Spawner.cs
parent: Classes
grand_parent: Game Kit
---

# Spawner.cs

## Description:
Enables `GameObjects` pooled by `ObjectPools` in sequential waves.

## Usage Notes:
 
Tip: Lowercase fields in the inspector can be set via UnityEvents.
 

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `bool` | canSpawn |  | `false` |
|  `bool` | spawnForward | Spawned GameObjects will be positioned in the direction the spawner is facing. | `false` |
|  `float` | forwardDistance | How far forward to spawn a GameObject (if Spawn Forward is checked). | 0 |
|  `Vector3` | spawnOffset |  |  |
|  `List<Wave>` | waves | Sequential information on what pool to spawn GameObjects from, how often and how many. |  |
|  `GameObject` | lastSpawned |  |  |
|  `int` | currentWave | | 0, Minimum value = 0 |
|  `int` | currentWaveSpawns | | 0, Minimum value = 0 |
|  `UnityEvent` | onHealed |  |  |
|  `UnityEvent` | onDead |  |  |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| DelaySpawn |  | `float` time | `Void` |
| SetWave   |  | `int` wave | `Void` |
| RandomizeWave |  Randomizes the spawns of a wave.  | `Wave` wave "The wave to randomize". | `Wave` "The wave with randomized spawns". |
| RandomizeWaves | Randomizes all waves that have randomWaves set to true.  |  | `Void` |
| DebugCurrentWave |  |  | `Void` |
| RandomizeSpawnOffset |  | `float` radius | `Void` |

## Structs:

### `[Serializable]` Wave
#### Public Properties:

| Type        | Name | Description | Default Value |
|:------------|:----|:-------------|:--------------|
|  `float` | interval | Time in seconds between spawns. | Minumum value = 0 |
|  `UnityEvent` | onSpawn |  |  |
|  `UnityEvent` | onWaveComplete |  |  |
|  `List<PoolID>` | poolIdentifiers | Defines the prefabs to enable from a pool during this wave. |  |
|  `bool` | randomizeWaves | Should spawns be randomized? (used instead of poolIdentifiers). |  |
|  `int` | spawnAmount | The amount of spawns in this wave. |  |
|  `List<int>` | randomPools | Pool indices to select spawns from. |  |
