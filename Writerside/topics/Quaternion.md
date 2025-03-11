# Quaternion

Quaternions are used to represent rotations. Unity internally uses Quaternions to represent all rotations.

They are based on complex number and are not easy to understand intuitively. You almost never access or modify individual Quaternion components, most often you would just take existing rotations and use them to construct new rotations.

The Quaternions functions that you use most of the time are:

* **LookRotation(Vector3 forward, Vector3 upwards?)**, creates a rotation with the specified forward and upwards directions
* **Angle(Quaternion a, Quaternion b)**, returns the angle in degrees between two rotations
* **Euler(float x, float y, float z)**, returns a rotation that rotates z degrees around Z axis, x degrees around X axis and y degrees around Y axis, in that order
* **Slerp(Quaternion a, Quaternion b, float t)**, spherically interpolates between a and b by t. The parameter t is clamped to the range [0, 1]
* **FromToRotation(Vector3 a, Vector3 b)**, creates a rotation which rotates from a to b
* **AngleAxis(float angle, Vector3 axis)**, creates a rotation which rotates angle degrees around axis
* **Identity**, returns the identity rotation for read only