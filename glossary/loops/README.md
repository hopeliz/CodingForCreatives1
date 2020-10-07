# Loops

Loops are a way of making code appear "cleaner" and more efficient when repeated code is used.

## Parts of a Loop

1. Kind of loop     \(e.g. while, for, foreach\)
2. Initialization of a **control variable**       \(e.g. int count = 1; int i = 0; etc.\) A **control variable** is a temporary variable used to iterate \(increase or decrease\) to limit the number of times a loop code runs.
3. Test conditions     \(What needs to be true?\)
4. Update the control variable      \(e.g. i++; i -= 5; etc.\)
5. Action to take      \(What is in the code block\) 

## Types of Loops

[While loops](while-loops.md)

[For loops](for-loops.md)

[Foreach loops](foreach-loops.md)

## Nested Loops

A loop INSIDE a loop? ? Heck, yeah!

The loops work the same inside other loops, BUT a different control variable will need to be used.

Generally, since i is often used, nested loops continue the alphabet: j, then k, then l...

Example:

```java
String[] names = { "Fluffy", "Nugget", "Pumpkin" };

for (int i = 0; i < names.length; i++) {
	for (int j = 0; j < 3; j++) {
		println(names[i]);
	}
}
```

Prints:

> Fluffy  
> Fluffy  
> Fluffy  
> Nugget  
> Nugget  
> Nugget  
> Pumpkin  
> Pumpkin  
> Pumpkin

