# Multi-Dimensional Arrays

## Multi-Dimensional Arrays

Arrays inside arrays (array-ception or “Yo, Dawg, I heard you like arrays, so I put an array inside your array” array)

Think of these like tables or matrices with multiple columns.

They have two indices per element (like coordinates - row, column)

## Creating Two-Dimensional Arrays

Two-Dimensional arrays can be created with sets of initial values listed within curly brackets **{ }**, then list these sets within outer curly brackets **{ }**

Double square brackets **\[ ]\[ ]** are placed right after the data type for all the elements of an array to signify it as a two-dimensional array.

Examples:

_Processing:_

```java
// First and Last name and of 5 people
String[][] people = { 
    { "Charles", "Stanton" }, 
    { "Eric", "Straub" }, 
    { "Ellie", "Aderyn" },
    { "Betty", "Dean" },
    { "Alex", "Heber" }
};
```

How to picture it:

| people | 0              | 1                                                                                                                               |
| ------ | -------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| 0      | "Charles"      | "Stanton"                                                                                                                       |
| 1      | "Eric"         | "Straub"                                                                                                                        |
| 2      | "Ellie"        | "Aderyn"                                                                                                                        |
| 3      | "Betty"        | "Dean"                                                                                                                          |
| 4      | "Alex"         | "Heber"                                                                                                                         |

## Using Two-Dimensional Arrays

Now, the elements can be accessed by their indices using both row and column.

Examples:

_Processing:_

```java
println(people[0][0] + " " + people[0][1]);
 
// Prints "Charles Stanton"
```

## Updating Two-Dimensional Arrays

Each “cell” can be updated individually like any other variable.

Examples:

_Processing:_

```java
people[0][0] = "Charlie";

println(people[0][0] + " " + people[0][1]);
 
// Prints "Charlie Stanton"

```

