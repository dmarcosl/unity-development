# GameObject

We can access to the properties of a component from inside a Script. To do so we need to use the following function:

```C#
// GetComponent<Type>()

Transform trans = GetComponent<Transform>();
Trans.position = new Vector3(1, 1, 1);
```