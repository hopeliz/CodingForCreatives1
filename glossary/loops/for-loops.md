# For Loops

Combines four parts of a loop into one line:

1. Type
2. Initialization
3. Conditions
4. Update

No need to remember to update or break the loop within the code block!

### For loop example #1

**Processing, Java, C#:**

```java
for (int count = 0; count < 5; count++) {
    println(count);
} 
```

**JavaScript and JS libraries:**

```javascript
for (var count = 0; count < 5; count++) {
    println(count);
}
```

Both will print:

> 0\
> 1\
> 2\
> 3\
> 4

Here:

1. Type: for **(line 1)**
2. Initialization: int count = 0; and var count = 0;   **(line 1)**
3. Conditions: (count < 5)  **(line 1)**      (only runs the loop code when the count is 0-4)
4. Update: count++;   **(line 1)**
5. Action: println(count);   **(line 2)**  (prints the current value of count)

### For loop example #2

**Processing, Java, C#:**

```java
String[] names = { "Fluffy", "Nugget", "Pumpkin" };

for (int i = 0; i < names.length; i++) {
    println(names[i]);
} 
```

**JS libraries:**

```javascript
var names = ["Fluffy", "Nugget", "Pumpkin"];

for (var i = 0; i < names.length; i++) {
    println(names[i]);
}
```

Both will print:

> Fluffy\
> Nugget\
> Pumpkin

Here:

1. Type: for **(line 3)**
2. Initialization: int i = 0; and var i = 0;   **(line 3)**
3. Conditions: (i < names.length)  **(line 3)**      \
   (only runs the loop code when the i variable is one less than the length of the array - keeps the array within bounds)
4. Update: i++;   **(line 3)**
5. Action: println(names\[i]);   **(line 4)**  \
   (prints the current name based on its index (using i to keep track of that number))

{% hint style="info" %}
Note: The variable i is often used, standing for “item” or “index”
{% endhint %}
