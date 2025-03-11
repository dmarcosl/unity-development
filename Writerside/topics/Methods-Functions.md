# Methods / Functions

Methods and functions are code blocks that contains a series of statements. A program causes the statements to be executed by calling the method or function and specifying any required argument.

The difference between a method or function is that a function will return a value, while the method not.

The syntax of a method is:

```C#
// void <method name> ([<data type> <arg name>]) {  
//   ...
// }
  
void printMessage() {  
  print("hello");  
}
```

The syntax of a function is:  

```C#
// <data type> <method name> ([<data type> <arg name>]) {
//   ...
//   return <data type>
// }

float square (float x) {  
  return x * x;  
}
```