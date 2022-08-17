---
layout: default
title: Pool
parent: Structs
grand_parent: Game Kit
---

# `[Serializable]` Pool

## Part of ObjectPools.cs

### Public Properties:

| Type        | Name | Description | Default Value |
|:------------|:----|:-------------|:--------------|
|  `GameObject` | prefab | The GameObject to pool. |  |
|  `int` | amount | The initial amount of GameObjects to instantiate. | Minumum value = 1 |
|  `HideFlags` | hideFlags | HideFlags for prefabs instantiated via the pooling system. Useful for hiding pooled objects in the heirarchy. |  |
|  `bool` | sequencialNaming | Use numbered names for GameObjects instead of name(clone). | false |
|  `List<GameObject>` | pooledObjects | The GameObjects currently pooled. |  |
