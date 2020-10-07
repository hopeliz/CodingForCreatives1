# Casting a Variable

Sometimes, you can use a variable in multiple ways:

* Float as a integer
* Integer as a float
* "" can be false or 0
  * This is called an **empty string**

Other times, the variable has to be **cast** into another type using an extra step.

This varies widely among languages, so it's best to look it up.

**Examples:**

_Processing example:_

```java
float amount = 1.0;
int amountAsInt = int(amount);

// now amountAsInt can be used where an integer is needed
```

_C\# example:_

```csharp
int count = 3;
string countAsString = count.ToString();

// now countAsString can be used where a string is needed
```

_Python example:_

```python
count = 3
countAsFloat = float(count)

# now countAsFloat can be used where a float is needed
```

