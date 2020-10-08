# Objects, Classes & Libraries

## Objects

When a programmer calls something an "object," it is usually talking about a self-contained set of code, usually its own file with specific features and actions that is accessible by other objects and code.

Sometimes it's abstract - like a "book" in a text adventure game where only some options work for when the user has a book. The chapters would be part of the book object. It could have functions like opening, closing, turning pages, etc.

Sometimes, you can see it - like a sphere or cube in Unity or a square in Processing. In Unity, you can see, add, and update components \(scripts\).

Separating code into reusable objects allows the objects to take care of their own code. Usually, there's a main object/set of code that helps keep track of information the objects need. This way, a program can be more efficient and organized than having one giant file with code.

## Classes

Classes are sets of code that control something specific - an example would be the Input class in Unity that holds all the information dealing with getting what buttons are being pressed on the keyboard, mouse, and controllers. It converts it into values, variables, and functions to be easily used by custom scripts.

Classes can exist within classes that provide information about how the classes work with each other. MonoBehaviour is an example of a base class in Unity and allows the programmer to use the Start\(\) and Update\(\) functions as well as the collider and trigger functions.

## Libraries

Libraries are collections of code that have a specific purpose and are often used as a resource to make coding easier. These are usually **imported** into projects with keywords like **include** and **using.** Because of this, sometimes, you'll hear them called "includes."

Example in Unity:

```csharp
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
```

Usually, UnityEngine is the one you need.

Another popular Unity one is for user interface access:

```csharp
using UnityEngine.UI;
```

Other examples would be:

* P5.js
* ThreeJS
* jQuery
* chart.js

^ All libraries of JavaScript. You could do all that they do with just JavaScript, but it would take ages and a lot of code. Libraries make it so you can use simplified code and built-in functions and features to meet your coding goals.

