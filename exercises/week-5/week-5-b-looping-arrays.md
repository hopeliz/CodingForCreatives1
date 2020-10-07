# Week 5-B Looping Arrays

Arrays are one of the common ways loops are utilized.

Why? 

1. Array values are conveniently accessed by an index - an integer
2. Arrays vary in sizes and can be quite long
3. A loop to display or run code per item in ONE frame is easier than using the same code repeatedly

## Step 1: Displaying Text in Processing

Displaying text is similar to displaying a shape.

Start by giving the text a color, then use text\(\) to provide the message and where to put it.

```java
void setup() {
  // Creates a canvas 600 pixels by 600 pixels
  size(600, 600);
}

void draw() {
  background(0);      // Black
  fill(247, 231, 206);      // Champagne color
  noStroke();      // No outline color
  
  // Sets a size for the text
  textSize(20);
  
  // Draws the text at (50, 50)
  text("This is text!", 50, 50);
}
```

Output when played:

![](../../.gitbook/assets/image%20%2817%29.png)

## Step 2: Create an Array and Display Each Item

Println\(\) will separate lines in a console, but in the canvas, we need to change the y value to create space between each text\(\) object.

```java
String[] pets = { "dog", "igauna", "hamster" };

void setup() {
  // Creates a canvas 600 pixels by 600 pixels
  size(600, 600);
}

void draw() {
  background(0);      // Black
  fill(247, 231, 206);      // Champagne color
  noStroke();      // No outline color
  
  // Sets a size for the text
  textSize(20);
  
  // Draws the text at (50, 50)
  text(pets[0], 50, 50);
  
  // Draws the text at (50, 75)
  text(pets[1], 50, 75);
  
  // Draws the text at (50, 100)
  text(pets[2], 50, 100);
}
```

Output when played:

![](../../.gitbook/assets/image%20%2822%29.png)

## Step 3: Moving the Array into a For Loop

As you can see, the full array appears, but only because we have 3 lines of code in our draw\(\).

Every time we update this array, we would need to add or remove these lines.

INSTEAD, we can use a for loop to always display the number of items in the array no matter its length.

First, let's put the changing y coordinate into its own variable.

In this example, the y increases by 25 each time. We can put that into a variable called spacing.

```java
float y = 50;
float spacing = 25;
```

For loops use control variables - an integer - that updates at the end of each run of the loop. For arrays, the variable i is often used to stand for "index" or "item" of the array.

One of the neat things about arrays is their "length" property. It provides the count of items in an array.

Since the array index starts with zero, the index will never go higher than the length of an array minus one \(or array.length - 1\).

To move to the next item in the array, we want the control variable _i_ to increase by 1. The shortcut for this is i++.

Putting the control variable, the loop's limits, and a way to update it looks like this:

```java
for (int i = 0; i < pets.length; i++)
```

Add curly backets { } to this for loop and put what you want to happen inside them.

```java
{
    text(pets[i], 50, y);
    y += spacing;
}
```

We initialize i and later, it resets to 0 with the loop, BUT we don't reset the y value, so it continues to add the spacing value. So the array appears to display really fast and go off the bottom of the canvas.

Add a line of code before the end curly bracket } of draw\(\) so it resets for each frame.

```java
y = 50;
```

Here is our full code:

```java
String[] pets = { "dog", "igauna", "hamster" };
float y = 50;
float spacing = 25;

void setup() {
  // Creates a canvas 600 pixels by 600 pixels
  size(600, 600);
}

void draw() {
  background(0);      // Black
  fill(247, 231, 206);      // Champagne color
  noStroke();      // No outline color
  
  // Sets a size for the text
  textSize(20);
  
  for (int i = 0; i < pets.length; i++) {
    text(pets[i], 50, y);
    y += spacing;
  }
  
  y = 50;
}
```

Output when played:

![](../../.gitbook/assets/image%20%2893%29.png)

Now, you can add and remove items from the array without having to change any other code:

```java
String[] pets = { "dog", "igauna", "hamster", "parrot", "goldfish" };
float y = 50;
float spacing = 25;

void setup() {
  // Creates a canvas 600 pixels by 600 pixels
  size(600, 600);
}

void draw() {
  background(0);      // Black
  fill(247, 231, 206);      // Champagne color
  noStroke();      // No outline color
  
  // Sets a size for the text
  textSize(20);
  
  for (int i = 0; i < pets.length; i++) {
    text(pets[i], 50, y);
    y += spacing;
  }
  
  y = 50;
}
```

Output when played:

![](../../.gitbook/assets/image%20%2819%29.png)

