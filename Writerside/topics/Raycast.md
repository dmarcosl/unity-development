# Raycast

Raycasting is the process of shooting an invisible ray from a point, in a specified direction to detect whether any colliders lay in the path of the ray.

It projects a line until it hits something, then it returns that point.

This is useful with side scrolling shooters, FPS, third person shooters, etc. Being able to trace where a bullet or laser is going to travel from the start to finish means that we know exactly how it should behave.

Raycasting in Unity3D is broken down into two distinct parts, 2D and 3D. Both of which are physics objects.

```C#
Public static bool Raycast(
  Vector3 origin,
  Vector3 direction,
  float maxDistance  
  Int layerMask,
  QueryTriggerInteraction queryTriggerInteraction)
```

* **origin**, starting point of the ray in world coordinates
* **direction**, direction of the ray
* **maxDistance**, max distance the ray should check for collisions, default infinity
* **layerMask**, a layer mask that is used to selectively ignore Colliders in the selected layers when casting a ray. The value assignment is int layerMask = 1 << 12, where 12 is the number of the layer selected to collide
* **queryTriggerInteraction**, specifies whether this query should hit triggers, default global

Casts a ray, from point origin, in direction direction, of length maxDistance, against all colliders in the scene.