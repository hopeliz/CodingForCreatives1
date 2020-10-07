# Creating Arrays

## Creating Arrays

Create arrays similarly to variables, but with a little extra.

**Two ways in Processing…**

1. Using the **new** keyword and square brackets **\[ \]**
2. Using square **\[ \]** and curly **{ }** brackets

## Method 1: The new Keyword

The **new** keyword is used to tell the program there will be a new specific type of data.

Square brackets **\[ \]** are placed right after the data type for all the elements of an array.

The number of elements \(if known\) should be listed within the type following the **new** keyword.

Then, assign each element individually.

**Examples:**

_Processing:_

```java
// Shopping list with 5 elements (slots)
String[] shoppingList = new String[5];

// Ages of 8 people (slots for 8 ages)
int[] ages = new int[8];

// List of 3 random numbers (slots for them)
float[] randNums = new float[3];
```

## Method 2: Using Brackets and Initial Values

Arrays can be created with initial values listed all at once within curly brackets **{ }.**

Square brackets **\[ \]** are placed right after the data type for all the elements of an array to signify it as an array.

**Examples:**

_Processing:_

```java
// Shopping list with 5 elements (slots)
String[] shoppingList = { "milk", "bread", "eggs", "bottled water", "soda" };

// Ages of 8 people (slots for 8 ages)
int[] ages = { 12, 31, 7, 80, 45, 50, 51, 50 };

// List of 3 random numbers (slots for them)
float[] randNums = { random(0, 5), random(0, 5), random(0, 5) };
```





