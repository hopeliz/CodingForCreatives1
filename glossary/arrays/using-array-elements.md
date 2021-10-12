# Using Array Elements

## Using Array Elements

Now, the elements can be accessed by their **indices** (plural of index).

**Examples:**

_Processing:_

```java
println(shoppingList); 	// Prints full array

println("My shopping list includes: " + shoppingList[0] + ", " + shoppingList[1] + 
", " + shoppingList[2] + ", " + shoppingList[3] + ", and " + shoppingList[4] + 
".");
 
// Prints "My shopping list includes: milk, bread, eggs, bottled water, and soda."
```

## Adding Elements to an Array

Sometimes you need to add elements to an array. Often, you’ll get an error if you try to assign a value to a non-existent “slot” or reference an index outside of what is available.

Most languages use a function such as **.append()** or **.expand()** or **.push()** or **.add()**

Examples:

_Processing:_

```java
shoppingList = append(shoppingList, "toothpicks");
 
ages = append(ages, 63);
```

## Removing Elements from an Array

Making an index / element empty does not remove the element.

To remove the element, use a function such as **.shorten()** (Processing) or **.Remove()** (Unity/C#).

Examples:

_Processing:_

```java
shoppingList = shorten(shoppingList);
 
ages = shorten(ages);
```

## Sorting Arrays

To sort an array use a function such as **.sort()** for alphabetical OR **.reverse()** for the opposite.

Examples:

_Processing:_

```java
shoppingList = sort(shoppingList);
println(shoppingList);
// Prints "bottled water bread eggs milk soda"

ages = sort(ages);
println(ages);
// Prints in this order: 7, 12, 31, 45, 50, 50, 51, 80

shoppingList = reverse(shoppingList);
println(shoppingList);
// Prints "soda milk eggs bread bottled water"
 
ages = reverse(ages);
println(ages);
// Prints in this order: 80, 51, 50, 50, 45, 31, 12, 7
```
