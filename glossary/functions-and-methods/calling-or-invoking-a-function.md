# Calling or Invoking a Function

## Parts of Calling or Invoking a Function

1. Function name
2. Arguments / Input 

Example:

```java
FunctionName(); // No arguments
FunctionName(x, y, size); // 3 arguments
```

## Arguments when calling

When calling a function with parameters/arguments, use values or variables that are currently being used NOT the names of the parameters unless they match for some reason.

The data types of the arguments should match the parameters of the function and appear in the same order.

Just like when creating the function, arguments should be separated by commas and be inside the parentheses \(\).

## **Other Use**

For functions that return information, the name of the function can be used as a variable.

Example:

```java
float num = 1;

...

	if (AddThree(num) < 5) {			// Sees if the resulting number is less than 5
		print(AddThree(num);				// Prints the resulting number
	}

...

// Creating the function can come after its use
float AddThree(float startNum) {
	return startNum + 3;
}


```

