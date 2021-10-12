# While Loops

Runs while the conditions following “while” are true - possibly forever!

To “break” out of the loop, update a “control variable” in the loop so eventually the conditions will be false

### While loop example

**Processing, Java, C#:**

```java
int count = 0;

while (count < 5) {
    println(count);
    count++;
}
```

**JavaScript and JS libraries:**

```javascript
var count = 0;

while (count < 5) {
    println(count);
    count++;
}
```

Both will print:

> 0\
> 1\
> 2\
> 3\
> 4

Here:

1. Type: while **(line 3)**
2. Initialization: int count = 0; and var count = 0;   **(line 1)**
3. Conditions: (count < 5)  **(line 3)**      (only runs the loop code when the count is 0-4)
4. Update: count++;   **(line 5)**
5. Action: println(count);   **(line 4)**  (prints the current value of count)
