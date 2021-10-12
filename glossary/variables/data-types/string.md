# String

## Description

* **Plain text** string
* Needs to be in quotation marks **" "** or **' '**
* Can include spaces
* For quotation marks/apostrophes inside, use a** \\"** or **\\'**
* Lots of uses

**Examples:**

_Processing:_

```java
String greeting = "Hello!";
```

_C#:_

```csharp
string lyric = 'I can\'t get enough';
```

_JavaScript:_

```javascript
var thing = "big airplane";
```

_Python:_

```python
thing = "moo cow"
```

## Shortcut

** **Add easily to an existing string by using **+=**

**Processing example:**

```java
String greeting = "Hello, ";
greeting += "Eric";
greeting += "!";

println(greeting);  // Prints "Hello, Eric!"
```

## Concatenate

* Term for adding strings together
* In Java and C languages, this is often done with plus ( + )
* In PHP and some others, it can be done with a period ( . )

**Processing example:**

```java
String greeting = "Hello, ";
String name = "Eric";
String msg = greeting + name + "!";

println(msg); // Prints “Hello, Eric!”
```

## **Delimitate**

* Using a character as a** delimiter **(where to separate the string into separate parts)
* This is often used to take text from .csv files where spreadsheet-like info is all one lump of text into its parts
* An easy example would be separating a sentence into a list of strings per word using a space as a delimiter

**Processing example:**

```java
String msg = "I'm a banana!";
String[] msgWord = split(msg, " ");

println(msgWord[0]);         // Prints "I'm"
println(msgWord[1]);	       // Prints "a"
println(msgWord[2]);	       // Prints "banana!"
```

## String Functions

Common string functions:

**.substring(index of first letter)**_ - _starts the string with the index/location of the first letter

**.substring(index of first letter, index of limit letter)** - starts the string with the index/location of the first letter and ends on the letter before the limit letter

**nfc(float or integer, number of digits after decimal)** - converts numbers into something more friendly with commas and rounds to the wanted decimal place

**.toUpperCase() **- changes the entire string to uppercase

**.toLowerCase()** - changes the entire string to lowercase

{% hint style="info" %}
.toUpperCase() and .toLowerCase() will come in handy later when comparing user input when users might have a variety of capitalization habits. You can convert their input to something to compare instead of comparing the input to all the possible options.
{% endhint %}

More Processing string functions can be found here: [https://processing.org/reference/String.html](https://processing.org/reference/String.html)

## Notation

Certain notation can be used within strings to accomplish things like creating a new line (equivalent to pressing the enter or return key), inserting an apostrophe when single quotes are used, inserting a tab, etc.

**\n **= new line\
**\r **= carriage return\
**\t **= tab\
**\\' **= apostrophe (to use when single quotes are used for a string)\
**\\"** = quotation marks (to use when double quotes are used for a string)
