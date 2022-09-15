---
layout: default
title: 3D Pixel Graphics Toolkit
nav_order: 6
has_children: false
permalink: /docs/3d-pixel-graphics-toolkit
---

# 3D Pixel Graphics Toolkit
[Download Dev Kit](https://github.com/Kitbashery/3D-Pixel-Graphics-Toolkit/releases/download/Development-Package/Kitbashery_3D_Pixel_Graphics_Toolkit.unitypackage){: .btn }
[Unity Asset Store](https://assetstore.unity.com/packages/slug/233054){: .btn }
[Kitbashery Store](https://kitbashery.com/coming-soon){: .btn }
[Older Versions](https://github.com/Kitbashery/3D-Pixel-Graphics-Toolkit/releases){: .btn }

## Description:

HDRP shader graphs for creating pixel-style graphics in Unity 3D.

[![Youtube](https://img.youtube.com/vi/wWMcH4FSE44/0.jpg)](https://www.youtube.com/watch?v=wWMcH4FSE44)

## Features:

* Pixelate Shader
* Pixel Cloud Shader
* Pixel Fluid Shader
* Pixel Triplanar Shader

### Pixel-Perfect Primitives:
Meshes with UVs optimized for pixel rendering.

* Cube
* Cylinder
* Ramp
* Sphere
* Dome

## Getting Started:

1. Import the package.
2. Import the demo scene found under the samples section in the package manager. (this will include the meshes).

Other things you may wish to do for a pixel-style project is to add an Import preset so imported textures have their import setting automatically set to:
* Max size set to "32".
* Filter Mode set to "Point (no filter)".
* Compression set to "none".
This will save a lot of time messing with the import settings.

It is also good to note that for 16x16 textures that one pixel in world units scale is `0.0625` and that magic number helps when snapping scale values acheive a uniform look.

It should also be noted that although primitive meshes such as the ramp, dome and sphere have UVs optimized for pixel perfect rendering there is geometric limitations that will still result in stretching. It is best to keep those meshes scaled uniformly, however checking `sloped surface` in the triplanar shader's material properties may help with some cases.

Also if you notice textures are not tiling then try using material instancing instead of static batching.
