# Input Component Setup Examples

## Supplies for All

|  |  |
| :--- | :--- |
| ![](../../.gitbook/assets/image%20%28288%29.png)  | Circuit Board |
| ![](../../.gitbook/assets/image%20%28301%29.png)  | Breadboard |
| ![](../../.gitbook/assets/image%20%28303%29.png)  | Jumper Cables |

## Photoresistor

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
        <img src="../../.gitbook/assets/image (296).png" alt/>
      </td>
      <td style="text-align:left">
        <p>Photoresistor</p>
        <p>(light sensor)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/image (284).png" alt/>
      </td>
      <td style="text-align:left">100 Ohm Resistor</td>
    </tr>
  </tbody>
</table>

### Diagram

![The data \(yellow\) wire is connected to pin A0 \(analog\).](../../.gitbook/assets/image%20%28290%29.png)

### Code

This code will print to the Serial Monitor the amount of light detected by the sensor. 

```cpp
// Sensor pin is connected to pin A0 (analog) on the Arduino circuit board
int sensorPin = 0;

// Define variables
int lightValue;

void setup() {
  // Establish the component connection and its type (output/input)
  pinMode(sensorPin, INPUT);
  
  // Start Serial connection (9600 Baud)
  Serial.begin(9600);
}

void loop() {
  // Read and store light amount
  lightValue = analogRead(sensorPin);

  // Print data to the Serial Monitor every 0.1 seconds
  Serial.print("Light Value: ");
  Serial.println(lightValue);
  delay(100);
}
```

## Ultrasonic Distance Sensor

This sensor works like a bat or a clicker from _The Last of Us_ to detect objects and their distance from the sensor using a soundwave pulse outside of human hearing ranges.

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
        <img src="../../.gitbook/assets/image (294).png" alt/>
      </td>
      <td style="text-align:left">
        <p>Ultrasonic Sensor</p>
        <p>(distant sensor)</p>
      </td>
    </tr>
  </tbody>
</table>

### Diagram

![The Trigger \(yellow\) wire is connected to pin 7 and Echo \(green\) to pin 6.](../../.gitbook/assets/image%20%28287%29.png)

### Code

This code will print to the Serial Monitor the distance of an object in front of the sensor. 

```cpp
// Trigger pin is connected to pin 6 on the Arduino circuit board
int trigPin = 7;

// Echo pin is connected to pin 7 on the Arduino circuit board
int echoPin = 6;

// Define variables
long duration;    // Holds the duration it takes for the sound to bounce back
int distance;     // Hold the calculated distance

void setup() {
  // Establish the component connection and its type (output/input)
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
  
  // Start Serial connection (19200 Baud)
  Serial.begin(19200);
}

void loop() {
  // Clears the trigPin condition (turns it off)
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);

  // Sets the trigPin to HIGH or active for 10 microseconds then off
  // This is like a "ping" it sends out
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(5);
  digitalWrite(trigPin, LOW);
  
  // Reads the echoPin value and returns the 
  // sound wave travel time in microseconds
  duration = pulseIn(echoPin, HIGH);

  // Calculates the distance in inches based on the speed of sound
  distance = duration / 74 / 2;

  // Displays the result in the Serial Monitor
  // Will say it's out of range if zero or more than 400 inches (most likely an error)
  
  if (distance >= 400 || distance <= 0){
    Serial.println("Out of range");
  } else {
    Serial.print("Distance: ");
    Serial.print(distance);
    Serial.println(" in.");
  }
}
```

