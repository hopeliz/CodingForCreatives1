# Foreach Loops

Runs a block of code for each item of an array or list.

A variable is created after the type of loop to store the current item in an array.

Found in languages like C\# and Python.

Use this kind when you want the same exact action to occur for each item.

### Foreach loop examples

**C\# and Unity:**

```csharp
string[] names = { "Fluffy", "Nugget", "Pumpkin" };

foreach (int item in names) {
    println(item);
} 
```

**Python:**

```python
names = [ "Fluffy", "Nugget", "Pumpkin" ]

for item in names:
    print(item \n)
```

Both will print:

> Fluffy  
> Nugget  
> Pumpkin

Here:

1. Type: foreach or for **\(line 3\)**
2. Initialization: int item and item   **\(line 3\)**
3. Conditions: \(int item in names\) or item in names  **\(line 3\)**       \(only runs the loop code when there is an item to run the code with\)
4. Update: in names   **\(line 3\)**   \(moves to the next item\)
5. Action: println\(item\); or print\(item \n\)   **\(line 4\)**   \(prints the current item based\)

{% hint style="info" %}
Note: \n is another way to do a carriage return \(end the line in the printed message\)
{% endhint %}

