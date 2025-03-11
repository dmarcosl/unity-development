# Colliders

## Mesh Collider

Mesh Collider builds its collision representation from the Mesh attached to the GameObject, and reads the properties of the attached Transform to set its position and scale.

![](image73.png)

* **Is Trigger**, if enabled, the collider is used for triggering events
* **Material**, reference to the physics material that determines how interacts with other colliders
* **Mesh**, reference to the mesh to use for collisions
* **Convex**, if enabled this mesh collider collides with other mesh colliders

## Character Collider

![](image57.png)

The traditional first person controls are not physically realistic. It is simply a capsule shaped collider which can be told to move in some direction from a script.

![](image49.png)

* **Slope Limit**, limits the collider to only cimb slopes that are less steep in degrees than the indicated value
* **Step Offset**, the character will step up a stair only if it is closer to the ground than the indicated value
* **Skin width**, two colliders can penetrate each other as deep as their skin width. Larger values reduce jitter, lows can cause the character to get stuck
* **Min Move Distance**, if the character tries to move below the value, it will not move
* **Center**, This will offset the capsule collider in world space
* **Radius**, length of the capsule collider radius
* **Height**, the capsule collider height

## Box Collider

Box colliders are obviously useful for anything roughly box-shaped, such as crates or chests.

![](image39.png)

* **Center**, the position of the collider in the objects local space
* **Size**, the size of the collider in the X, Y, Z directions

## Capsule Collider

![](image17.png)

* **Direction**, the axis of the capsule lengthwise orientation in the object local space

## Sphere Collider

![](image5.png)