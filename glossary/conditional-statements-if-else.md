# Conditional Statements \(If/Else\)

## If Statements

**If statements** only run code within a coding block when certain conditions are true.

**Format:**

_Almost everything but Python:_

```java
if (test) {
    // Run this code if test is true
}
```

**Example:**

```java
if (num < 4) {
    println("This number is less than 4!");
}
```

_Python:_

{% hint style="danger" %}
Indentation is the only way Python recognizes the code block. Double-check the number of indents if the code has errors or does not work.
{% endhint %}

```python
if test:
    # Run this code if test is true
```

**Example:**

```python
if num < 4:
    println("This number is less than 4!")
```

## If/Else Statement

**If/else statements** only run code within a coding block when certain conditions are true, otherwise the else statement block of code will run.

**Format:**

_Almost everything but Python:_

```java
if (test) {
    // Run this code if test is true
}
else {
    // Otherwise run this code
}
```

**Example:**

```java
if (num < 4) {
    println("This number is less than 4!");
}
else {
    println("This number is 4 or higher ... or not a number at all!");
}
```

_Python:_

{% hint style="danger" %}
Indentation is the only way Python recognizes the code block. Double-check the number of indents if the code has errors or does not work.
{% endhint %}

```python
if test:
    # Run this code if test is true
else:
    # Otherwise run this code
```

**Example:**

```python
if num < 4:
    println("This number is less than 4!")
else:
    println("This number is 4 or higher ... or not a number at all!")
```

## If/Else If/Else Statement

**If/else if/else statements** only run code within a coding block when certain conditions are true, otherwise the else statement block of code will run.

Else if statement blocks go between if and the else blocks to provide more options.

These are good for multiple specific choices.

**Format:**

_Almost everything but Python:_

```java
if (test) {
    // Run this code if test is true
}
else if (test2) {
    // Run this code if the past tests are false and this test is true
}
else {
    // Otherwise run this code
}
```

**Example:**

```java
if (num < 4) {
    println("This number is less than 4!");
}
else if (num > 7) {
    println("This number is greater than 7!");
}
else {
    println("This number is 4 or higher ... or not a number at all!");
}
```

_Python:_

{% hint style="danger" %}
Indentation is the only way Python recognizes the code block. Double-check the number of indents if the code has errors or does not work.
{% endhint %}

```python
if test:
    # Run this code if test is true
elif test2:
    # Run this code if the past tests are false and this test is true
else:
    # Otherwise run this code
```

**Example:**

```python
if num < 4:
    println("This number is less than 4!")
elif num > 7:
    println("This number is greater than 7!")
else:
    println("This number is 4 or higher ... or not a number at all!")
```

## Switch/Case Statement

{% hint style="warning" %}
This doesn't exist in certain languages.
{% endhint %}

**Switch/case statements** replace else if statements when equivalents are being tested.

Instead of testing in the parentheses, the parentheses hold the first value, then each “case” is what the variable is compared with. If the variable matches the case, the corresponding code block runs.

Each case needs a “break” to move on.

Each switch/case code block should have a default case serving as an else statement. Programmers often use the default case to test if the block ran, but had no equivalents \(a form of error catching\)

**Format:**

_Almost everything but Python:_

```java
switch (variable) {
    case caseValue:
        // runs if the case is equivalent to caseValue
        break;
    case caseValue2:
        // runs if the case is equivalent to caseValue2
        break;
    default:
        // runs if all caseValues are not true
        break;
}
```

**Example:**

```java
String name = "Nina";

switch (name) {
    case "Andrew":
        println("Andrew has three cats.");
        break;
    case "Nina":
        println("Dina dances.");
        break;
    default:
        println("Please choose either 'Andrew' or 'Dina'.");
        break;
}
```



