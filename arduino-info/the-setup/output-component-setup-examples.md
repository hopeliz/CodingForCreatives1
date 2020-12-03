# Output Component Setup Examples

## Supplies for All

|  |  |
| :--- | :--- |
| ![](../../.gitbook/assets/image%20%28288%29.png)  | Circuit Board |
| ![](../../.gitbook/assets/image%20%28303%29.png)  | Breadboard |
| ![](../../.gitbook/assets/image%20%28305%29.png)  | Jumper Cables |

## Buzzer

### Additional Supplies

|  |  |
| :--- | :--- |
| ![](../../.gitbook/assets/image%20%28297%29.png)  | Buzzer |
| ![](../../.gitbook/assets/image%20%28284%29.png)  | 100 Ohm Resistor |

### Diagram

![The data \(yellow\) wire is connected to digital pin 9.](../../.gitbook/assets/image%20%28306%29.png)

### Code

In this example, the buzzer will play a 1KHz tone for 1 second, then silence for 1 second as long as it's plugged in.

```cpp
// Buzzer is connected to pin 9 on the Arduino circuit board
int buzzer = 9;

void setup() {
  // Establish the component connection and its type (output/input)
  pinMode(buzzer, OUTPUT);
}

void loop() {
  tone(buzzer, 1000);   // Plays 1KHz tone
  delay(1000);          // Plays this tone for 1 second
  noTone(buzzer);       // Plays no tone
  delay(1000);          // Plays this tone for 1 second
}
```

## Standalone LED Light

### Additional Supplies

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/image (286).png" alt/>
      </td>
      <td style="text-align:left">
        <p>LED light</p>
        <p>(any color, as long as it has only two connectors)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/image (291).png" alt/>
      </td>
      <td style="text-align:left">220 Ohm Resistor</td>
    </tr>
  </tbody>
</table>

### Diagram

![The data \(yellow\) wire is connected to digital pin 9.](../../.gitbook/assets/image%20%28289%29.png)

### Code

This code will make the LED light up for 1 second and go off for 1 second until it is unplugged.

```cpp
// LED is connected to pin 9 on the Arduino circuit board
int LED = 9;

void setup() {
  // Establish the component connection and its type (output/input)
  pinMode(LED, OUTPUT);
}

void loop() {
  digitalWrite(LED, HIGH);  // Turn light on
  delay(1000);              // Wait 1 second
  digitalWrite(LED, LOW);   // Turn light off
  delay(1000);              // Wait 1 second
}
```

## Multiple LEDs

This example shows using and controlling two separate LEDs as an example of multiple output components.

### Additional Supplies

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/image (286).png" alt/>
      </td>
      <td style="text-align:left">
        <p>2 LED lights</p>
        <p>(any color, as long as it has only two connectors)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/image (291).png" alt/>
      </td>
      <td style="text-align:left">2 - 220 Ohm Resistors</td>
    </tr>
  </tbody>
</table>

### Diagram

![The yellow data wire is connected to digital pin 10 and the orange wire to pin 9.](../../.gitbook/assets/image%20%28281%29.png)

### Code

This code will alternate the lights lighting for 1 second each with a second of darkness in between until the Arduino is unplugged.

```cpp
// 1st LED is connected to pin 10 on the Arduino circuit board
int LED = 10;

// 2nd LED is connected to pin 9 on the Arduino circuit board
int LED2 = 9;

void setup() {
  // Establish the component connection and its type (output/input)
  pinMode(LED, OUTPUT);
  pinMode(LED2, OUTPUT);
}

void loop() {
  digitalWrite(LED, HIGH);  // Turn light on
  delay(1000);              // Wait 1 second
  digitalWrite(LED, LOW);   // Turn light off
  delay(1000);              // Wait 1 second
  digitalWrite(LED2, HIGH);  // Turn light on
  delay(1000);              // Wait 1 second
  digitalWrite(LED2, LOW);   // Turn light off
  delay(1000);              // Wait 1 second
}
```

## RGB LED

This is a special LED that you can use 0-255 color values to get any color of the RGB rainbow.

### Additional Supplies

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/image (280).png" alt/>
      </td>
      <td style="text-align:left">
        <p>2 LED lights</p>
        <p>(any color, as long as it has only two connectors)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/image (291).png" alt/>
      </td>
      <td style="text-align:left">3 - 220 Ohm Resistors</td>
    </tr>
  </tbody>
</table>

### Diagram

Note: This diagram is for a Cathode RGB LED where the 2nd connector is the ground \(negative\) connection.

![The blue wire is connected to pin 9, green to pin 10, and red to pin 11.](../../.gitbook/assets/image%20%28301%29.png)

## Code

This example turns the light cyan using the "simple" way \(setting each color with a line of code\).

```cpp
// Red pin is connected to pin 11 on the Arduino circuit board
int red = 11;

// Green pin is connected to pin 10 on the Arduino circuit board
int green = 10;

// Blue pin is connected to pin 9 on the Arduino circuit board
int blue = 9;

void setup() {
  // Establish the component connection and its type (output/input)
  pinMode(red, OUTPUT);
  pinMode(green, OUTPUT);
  pinMode(blue, OUTPUT);
}

void loop() {
  // Example of Cyan (0, 255, 255)
  analogWrite(red, 0);
  analogWrite(green, 255);
  analogWrite(blue, 255);
  delay(1000);
} 
```

This example shows the same thing, but using a custom function, making color changes take fewer lines of code:

```cpp
// Red pin is connected to pin 11 on the Arduino circuit board
int red = 11;

// Green pin is connected to pin 10 on the Arduino circuit board
int green = 10;

// Blue pin is connected to pin 9 on the Arduino circuit board
int blue = 9;

void setup() {
  // Establish the component connection and its type (output/input)
  pinMode(red, OUTPUT);
  pinMode(green, OUTPUT);
  pinMode(blue, OUTPUT);
}

void loop() {
  // Example of Cyan (0, 255, 255)
  RGB_Color(0, 255, 255);
  delay(1000);
} 

void RGB_Color(int redValue, int greenValue, int blueValue) {
  analogWrite(red, redValue);
  analogWrite(green, greenValue);
  analogWrite(blue, blueValue);
}
```

