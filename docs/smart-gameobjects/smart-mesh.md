---
layout: default
title: SmartMesh.cs
parent: Classes
grand_parent: Smart GameObjects
---

# SmartMesh.cs

### Namespace:
Kitbashery.SmartGO

## Description:
A parametric mesh generator.

## Properties:

| Type | Property Name | Summary | Default Value |
| --- | --- | --- | --- |
| `MeshFilter` | meshfilter |  | GetComponent<MeshFilter>() |
| `MeshTypes` | meshType |  | MeshTypes.Asset |
| `Mesh` | assetMesh |  |  |
| `Int32` | subdivisions |  | 1 |
| `Single` | height |  | 1 |
| `Single` | width |  | 1 |
| `Single` | depth |  | 1 |
| `Single` | radius |  | 1 |
| `Single` | start |  | 0 |
| `Int32` | heightSegments |  | 2 |
| `Int32` | widthSegments |  | 2 |
| `Int32` | depthSegments |  | 2 |
| `Int32` | radialSegments |  | 3 |
| `Vector3[]` | customVertices |  |  |
| `Int32[]` | customTriangles |  |  |
| `Boolean` | top |  | true |
| `Boolean` | bottom |  | true |
| `Boolean` | leftSide |  | true |
| `Boolean` | rightSide |  | true |
| `Boolean` | frontSide |  | true |
| `Boolean` | backSide |  | true |
| `Vector3` | topUVOffset |  |  |
| `Vector3` | bottomUVOffset |  |  |
| `Vector3` | leftUVOffset |  |  |
| `Vector3` | rightUVOffset |  |  |
| `Vector3` | frontUVOffset |  |  |
| `Vector3` | backUVOffset |  |  |
| `Vector3` | vertexOffset |  |  |
| `Vector3` | vertexRotation |  |  |
| `Vector3` | vertexScale |  | Vector3.one |
| `Single` | noiseStrength |  | 0 |
| `Vector2` | xBounds |  |  |
| `Vector2` | yBounds |  |  |
| `Vector2` | zBounds |  |  |
| `Boolean` | sphereify |  | false |
| `Single` | sphereifyRadius |  | 1 |
| `UVProjections` | unwrapMode |  | UVProjections.Original |
| `Vector3[]` | vertices |  | assetMesh.vertices |
| `Int32[]` | triangles |  | assetMesh.triangles |
| `Vector3[]` | normals |  | assetMesh.normals |
| `Vector2[]` | uv |  | assetMesh.uv |
| `Color[]` | vertexColors |  | assetMesh.colors |
| `Color` | vertexColor |  |  |
| `Single` | uvRotation |  |  |
| `Vector2` | tiling |  | Vector2.one |
| `Boolean` | uvPreview |  | false |
| `Mesh` | mesh |  |  |
| `Boolean` | wireframe |  | false |


## Methods:

| Method | Summary | Parameters | Returns |
| --- | --- | --- | --- |
| BuildMesh |  |  | `Void` |
| PolarProject |  | `Vector2[]&` uvs, `Vector3[]` points | `Void` |
| SphericalProject |  | `Vector2[]&` uvs, `Vector3[]` points, `Boolean` normalize | `Void` |
| CylindricalProject |  | `Vector2[]&` uvs, `Vector3[]` points | `Void` |
| ConicalProject |  | `Vector2[]&` uvs, `Vector3[]` points | `Void` |
| PlanarProject |  | `Vector2[]&` uvs, `Vector3[]` points, `Vector3` direction | `Void` |
| BoxProject |  | `Vector2[]&` uvs, `Vector3[]` norms, `Vector3[]` verts | `Void` |
