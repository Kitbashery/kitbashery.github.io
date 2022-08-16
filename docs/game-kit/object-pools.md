---
layout: default
title: ObjectPools.cs
parent: Classes
grand_parent: Game Kit
---

# ObjectPools.cs

## Description:
A singleton class for managing multiple pools of GameObjects.

## Usage Examples:
 ```csharp
//From external script you can get a GameObject from the pool via a prefab name or a known index of ObjectPool.pools
public void Spawn()
{
    GameObject go = ObjectPools.Instance.GetPooledObject("MyPrefabName");
    go.transform.position = Vector3.Zero;
    go.SetActive(true);
  
    //Alternatively:
    ObjectPools.Instance.ActivatePooledObject("MyPrefabName");
}
 ```
 
 ## Usage Notes:
 It is recommended to access the ObjectPool instance after Awake() is called, 
 otherwise modify the script execution order so your script is loaded after ObjectPool.cs
 

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `public static ObjectPool` | Instance |  |  |
|  `public List<Pool>` | pools | A non-reorderable list of Pools. |  |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| CreatePools |  | | `Void` |
| PopulatePools   |   |  | `Void` |
| ExpandPools      |    | `Pool pool, int amount` | `Void` |
| DestroyPools | Destroys all objects in all pools.  | `bool omitActive`: "Preserve pooled GameObjects that are currently active in the scene". | `Void` |
| ActivatePooledObject |  | `int index` | `Void` |
| ActivatePooledObject |  | `string prefabName` | `Void` |
| GetPooledObject | Gets a pooled GameObject by the index of its pool. | `int index` "The index of a pool in pools". | `GameObject` "The first inactive prefab instance". |
| GetPooledObject | Gets a pooled GameObject by its prefab name. | `string prefabName` "The name of the prefab to get an instance of". | `GameObject` "The first inactive prefab instance". |
| CreatePools |  |  | `Void` |


## Structs:

### Pool [Serializable]

### Public Properties:
| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `GameObject` | prefab | The GameObject to pool. |  |
|  `int` | amount | The initial amount of GameObjects to instantiate. | Minumum value = 1 |
|  `HideFlags` | hideFlags | HideFlags for prefabs instantiated via the pooling system. Useful for hiding pooled objects in the heirarchy. |  |
|  `bool` | sequencialNaming | Use numbered names for GameObjects instead of name(clone). | false |
|  `List<GameObject>` | pooledObjects | The GameObjects currently pooled. |  |

### PoolID [Serializable]

### Public Properties:
| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `int` | poolIndex | The index of a pool in the ObjectPools instance pool list. | Minumum value = 0 |
|  `string` | prefabName | If specified the spawner will try to get GameObjects from the pool by the prefab name instead of index. | |
