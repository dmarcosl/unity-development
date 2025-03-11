# Models

A model file can contain a 3D model, such a character, a building or a piece of furniture. The model is imported as multiple Assets. In the Project view, the main imported object is a model Prefab.

We can import a model by two ways:

* Right click on Project view → Import New Asset
* Asset menu of the top navbar → Import New Asset

## Exported 3D files

This files are smaller and have a modular design.  
At make a change to the file, the time to re-import or export the model is slower than the proprietary files.

The supported formats are:

* .FBX
* .dae (Collada)
* .3DS
* .dxf
* .obj

## Proprietary formats

Any change in the file will be reflected quickly in Unity, which make faster iterations in development.  
Are bloated with unnecessary data.

Through conversion, can support this formats:

* Max
* Maya
* Blender
* Cinema4D
* Modo
* Lightwave
* Cheeta3D
* Sketchup

## Contents of an FBX

A FBX file can content

* **Meshes**
* **Animation**
* **Blend Shapes**, deformations of the mesh to achieve several shapes, like facial expressions
* **Textures/Materials**
* **Smoothing Groups**, soft or hard the edges of the model