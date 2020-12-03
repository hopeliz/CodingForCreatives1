# Using the Serial Connection

The Serial connection provides a way for you to upload your code to your Arduino as well as see the data coming in from sensors and other input components.

## Setup

### For Uploading to your Arduino

In the Arduino program, set up your serial connection.

Go to Tools &gt; Board &gt; Arduino AVR Boards &gt; Arduino Uno \(or whatever you have\)

![](../../.gitbook/assets/image%20%28304%29.png)

![](../../.gitbook/assets/image%20%28299%29.png)

Once you have the Arduino connected via USB, you can find and select the port that is needed under Tools &gt;  Port &gt; COM\(whatever number shows the connection\)

![](../../.gitbook/assets/image%20%28299%29.png)

## Viewing the Info

In your code, in the setup\(\) function, use Serial.begin\(\) to establish a connection. In the parentheses, put your baud rate \(it has something to do with the connection speed\). The most common is 9600.

```cpp
void setup() {
    Serial.begin(9600);   // Start Serial connection
}
```

As long as the Arduino is connected via USB you your computer, you can see this info two ways:

### Serial Monitor

This is like a Console that you can print messages to using Serial.print\(\) and Serial.println\(\).

### Serial Plotter

This is a line graph that will interpret numbers in anything printed to the Serial monitor.

