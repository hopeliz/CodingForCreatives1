# Assigning Values to Arrays

## Assigning Values

After being created/declared, access and element or “slot” of the array variable by its index.

Picture an array like a numbered list starting at zero...

| shoppingList |  |
| :--- | :--- |
| 0 | "milk" |
| 1 | "bread" |
| 2 | "eggs" |
| 3 | "bottled water"                                                                                                                                              |
| 4 | "soda" |

| ages |  |
| :--- | :--- |
| 0 | 12 |
| 1 | 31 |
| 2 | 7 |
| 3 | 80                                                                                                                                              |
| 4 | 45 |
| 5 | 50 |
| 6 | 51 |
| 7 | 50 |

**Example Code:**

_Processing:_

```java
shoppingList[0] = "milk";
shoppingList[1] = "bread";
shoppingList[2] = "eggs";
shoppingList[3] = "bottled water";
shoppingList[4] = "soda";
```

```java
ages[0] = 12;
ages[1] = 31;
ages[2] = 7;
ages[3] = 80;
ages[4] = 45;
ages[5] = 50;
ages[6] = 51;
ages[7] = 50;
```

{% hint style="info" %}
This is advanced! This will make more sense in Week 5
{% endhint %}

```java
for (int i = 0; i < randNums.length(); i++) {
	randNums[i] = random(0, 5);
}
```

Equivalent to:

```java
randNums[0] = random(0, 5);
randNums[1] = random(0, 5);
randNums[2] = random(0, 5);
```

