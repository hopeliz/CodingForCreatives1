# Parameters & Arguments

Parameters and arguments are basically the input required and used by functions.

Think of it this way…

Say you have a bunch of random colored blocks. You don't know how many or what order.

You want to turn the red blocks green.

You can go through each block and use code to say "if red, turn green" but if the code to turn it green is complicated, separate it into a function.

```java
void turnGreen() {
	// code for a block to turn green
}
```

But how does the function know **what block** to turn green?

One way we can say which block is by adding parameters to our function, then using arguments when calling it.

```java
void turnGreen(block blockToChange) {
	// code for blockToChange to turn green
}
```

The parameter **blockToChange** becomes a temporary variable and only can be used for this function.

So when we call it, we can say what block it is by putting it as an argument...

```java
if (block15 is Red) {
		turnGreen(block15);
}
```

block15 is sent to the function, setting **blockToChange** to block15.

Say you want to turn multiple specific blocks to a specific color. You can use parameters and arguments to get information and use it in the function.

```java
void changeColor(block blockToChange, color newColor) {
	// code for blockToChange to change to the new color
}
```

The parameters **blockToChange** and **newColor** become temporary variables and only can be used for this function.

So when we call the function, we can say what block and what color by using arguments...

```java
changeColor(block11, grey);
```

block11 and grey is sent to the function, setting **blockToChange** to block11 and **newColor** to grey so the function knows to set block11 to grey. Then, any other blocks and colors can be used without extra or repeated code.







