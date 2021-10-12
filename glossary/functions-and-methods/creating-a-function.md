# Creating a Function

## Parts of Creating a Function

1. Keyword that says the code block is a function
2. Function name
3. Parameters or “input” information
4. Actions to take
5. Return or “output” information 

### 1. Keyword to say it’s a function

* If explicit languages, it’s often **void** or the **type** of returned info/output expected
* For implicit languages, it’s usually **function** or **def.**

### 2. Name of the Function

* Naming a function is similar to naming a variable - they have NO SPACES.
* The names are often a verb or action  .
* As for casing, it depends on the language but will work with any.

### 3. Parameters / Input

* Parameters are pieces of information needed for the work to be done inside the function.
* The names of the arguments serve as temporary variables usable only within the function.
* They are separated by commas   and listed inside the parentheses ()  .
* Like other variables, might need associated data types   if the language is explicit.

### 4. Actions to Take

Just like other blocks of code, the code that should run should be put inside curly brackets { }

### 5. Return or Output

* In explicit languages - especially if the function code starts with a data type - that data type must be “**returned**.”
* Use a line of code in the curly brackets:   `return value;  `
* The value should match the data type
* For some languages, void functions require `return none;`

## Examples

**Processing, Java, and C#:**

```java
// Function adds 3.5 to a provided number

float addThreeAndAHalf(float startNum) {
    return startnum + 3.5;
}

// Function prints "1, 2, 3"

void countToThree() {
    println("1, 2, 3");
}
```

**JavaScript:**

```javascript
// Function adds 3.5 to a provided number

function addThreeAndAHalf(startNum) {
    return startnum + 3.5;
}

// Function prints "1, 2, 3"

function countToThree() {
    document.write("1, 2, 3");
}
```

**Python:**

```python
# Function adds 3.5 to a provided number

def addThreeAndAHalf(float startNum):
    return startnum + 3.5
    
# Function prints "1, 2, 3"

def countToThree():
    println("1, 2, 3")
```
