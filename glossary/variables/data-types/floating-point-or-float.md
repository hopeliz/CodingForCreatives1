# Floating Point or Float

## Description

* Number with a decimal point
* Used for precision
* Used for percentages, but between 0 and 1 (0 and 100%)
* Used for time

**Examples:**

_Processing:_

```java
float speed = 2.5;
```

_JavaScript:_

```javascript
var percentage = 0.25;
```

_Python:_

```python
percentage = 0.25
```

{% hint style="info" %}
Some languages have multiple types with decimal points

Example: a float in C# or Unity will need an F after the number in the code to tell it is a float and not something else**. **See the example below.
{% endhint %}

```csharp
float speed = 2.5F;
```

^ This is one of the more common errors - forgetting that F.

{% hint style="warning" %}
Do not use commas in your numbers!
{% endhint %}

## Shortcuts (Assignment Operators)

### Quick Math

**+=** means “add this”

**-=** means “subtract this”

**\*=** means “multiply it by this”

**/=** means “divide it by this”

{% hint style="warning" %}
This updates the variable when used
{% endhint %}

**Example:  **    

_Processing, Java-based, and C-based:_

```java
float opacity = 0.5;

println(opacity);        // Prints "0.5"

opacity += 0.15;

println(opacity);        // Prints "0.65"
```

_Python:_

```python
opacity = 0.5

print(opacity)        # Prints "0.5"

opacity += 0.15

print(opacity)        # Prints "0.65"
```

###   
