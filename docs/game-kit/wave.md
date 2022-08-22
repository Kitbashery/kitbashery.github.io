---
layout: default
title: Wave
parent: Structs
grand_parent: Game Kit
---

# `[Serializable]` Wave

## Part of Spawner.cs

### Public Properties:

| Type        | Name | Description | Default Value |
|:------------|:----|:-------------|:--------------|
|  `float` | interval | Time in seconds between spawns. | Minumum value = 0 |
|  `UnityEvent` | onSpawn |  |  |
|  `UnityEvent` | onWaveComplete |  |  |
|  `List<PoolID>` | poolIdentifiers | Defines the prefabs to enable from a pool during this wave. |  |
|  `bool` | randomizeWaves | Should spawns be randomized? (used instead of poolIdentifiers). |  |
|  `int` | spawnAmount | The amount of spawns in this wave. |  |
|  `List<int>` | randomPools | Pool indices to select spawns from. |  |
