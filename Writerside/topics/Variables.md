# Variables

A variable is nothing but a name given to a value that our program can manipulate.

In C#, the declaration of a variable is

```C#
// <data type> <variable name> = <value>;  
int height = 25;  
float width = 22.5f;  
string text = "hello";  
bool isSelected = true;
```

In Javascript, the declaration of a variable is

```JavaScript
// var <variable name> = <value>;  
var height = 25;  
var width = 22.5;  
var text = "hello";  
var isSelected = true;
```

If a valor is not given, the null value is assigned by default.

In Javascript, a variable can change its data type, in C# cannot.  
In C#, at operate with variable of different data types, the more affordable is assigned to the result:

- int + float = float
- int + string = string
- bool + string = string

### Vector3

Vector3 is a representation of 3D vectors and points.

The structure is used throughout Unity to pass 3D positions and directions around, it also contains function for doing common vector operations.

The syntax is

```C#
Vector3(X, Y, Z)
```

We can access to the axis of the Vector3 by calling them:

```C#
Vector3 vector = new Vector3(1.0f, 1.0f, 1.0f);  
float x = vector.x;  
float y = vector.y;  
float z = vector.z;
```