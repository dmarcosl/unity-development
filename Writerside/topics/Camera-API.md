# Camera API

A Camera is a device through which the player views the world.

A screen space point is defined in pixels. The bottom left of the screen is (0, 0), the Z position is in world units from the Camera.

A viewport space point is normalized and relative to the Camera. The bottom left of the Camera is (0, 0), the Z position is in world units from the Camera.

A world space point is defined in global coordinates, like the Transition.position.

## ScreenPointToRay

This public method of the Camera API allows return a ray going from camera through a screen point.

That ray is in world space, starting on the near plane of the camera and going through position (x, y) pixel coordinates on the screen, while the z is ignored.

Example:

```C#
Camera cam;

void Start() {
  cam = GetComponent<Camera>();
}

void Update() {
  Ray ray = cam.ScreenPointToRay(new Vector3(200, 200, 0));
  Debug.DrawRay(ray.origin, ray.direction * 10, Color.red);
}
```