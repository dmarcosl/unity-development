# Unity Interface

Scripts, just like other components often have properties that are editable in the inspector, you can allow values in your script to be edited from the Inspector too.

If you declare a public variable within your code, you can manipulate its value in the Inspector.

![](image30.png)

Unity creates the Inspector label by introducing a space wherever a capital letter occurs in the variable name. This is purely for displaying purposes.  
In the script the variable is named as myName, but in the Inspector is displayed as My Name.

In C# you must declare a variable as public to see it in the Inspector.  
In Javascript, the variables are public by default.