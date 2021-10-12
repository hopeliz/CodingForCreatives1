# Processing Example

This was the example from class than can be reused.

```java
float x = 300;
float y = 300;
float size = 50;
float speed = 5;

void setup() {
    size(600, 600);        // Creates a 600 x 600 canvas
    
    // Change rectMode() to draw the origin (x, y) coordinates in the center of the square
    rectMode(CENTER);
    
    // Draw a black background
    background(0);      // Equivalent to background(0, 0, 0);
    
    // Create a square at the coordinates provided in the variables
    rect(x, y, size, size);    
}

void draw() {
}

void keyPressed() {
  
  // Go up if 'w' or 'W' is pressed
  if (key == 'w' || key == 'W') {
    y -= speed;
  }
  
  // Go down if 's' or 'S' is pressed
  if (key == 's' || key == 'S') {
    y += speed;
  }
  
  // Go left if 'a' or 'A' is pressed
  if (key == 'a' || key == 'A') {
    x -= speed;
  }
  
  // Go right if 'd' or 'D' is pressed
  if (key == 'd' || key == 'D') {
    x += speed;
  }
  
  background(0);
  rect(x, y, size, size);
}
```
