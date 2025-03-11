# DeltaTime

DeltaTime is the time in seconds it took to complete the last frame. With this, we make the game frame rate independent.

By default, if you update the position of an object in the Update method by, for example, 10 meters, the object will move 10 meters per frame.

```C#
void Update() {  
  transform.position = transform.position + new Vector3(0, 0, 10);  
}
```

With DeltaTime, we can make the object be moved 10 meters per second

```C#
void Update() {  
  Vector3 positionDelta = new Vector3(0, 0, 10 * Time.deltaTime);  
  transform.position = transform.position + positionDelta;  
}
```