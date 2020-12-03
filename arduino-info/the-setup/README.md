# The Setup

With Arduinos, you are setting up a complete circuit that powers the circuit.

## General Setup

### Power Flow

Some ways to think about how power flows through a circuit:

1. Complete ring - if it's not complete, it won't work. Adding things to this ring will be powered if the ring is complete.
2. Computer/power source end of the circuit board as a heart, Arduino processor as the brain, and components are limbs. - Positive charge is like oxygenated blood \(seen as red arteries on diagrams\) comes from the heart/lungs to the limbs for them to work. After supplying oxygen to the limbs, the deoxygenated blood \(seen as blue veins on diagrams\) returns to the heart and the cycle starts again. The brain needs power to work and the wires from components to analog and dialog pins send data to the processor just like the nerves in a limb send information to the brain.

### Completing a Circuit

The order usually goes:

1. Plug in your power source \(computer, wall outlet, or battery component\) using your USB 2.0 cord to the USB port or wall/battery pack power to the power port on the circuit board.  ![](../../.gitbook/assets/image%20%28276%29.png) ![](../../.gitbook/assets/image%20%28282%29.png)   
2. Connect a wire from 3.3V or 5V pin \(i/o hole\) on the circuit board to the red positive rail on the breadboard.
3. Connect an additional wire from the blue negative rail to the ground \(GND\) pin on the circuit board.

![](../../.gitbook/assets/image%20%28300%29.png)

This technically completes the circuit.

### Adding Components

Now you just add components in there.

#### For the positive side

1. Take an additional wire and connect it from the red positive rail on the breadboard to a numbered electrical contact strip on the breadboard.
2. Put the component's positive pin \(often marked with a + or Vcc\) in the same electrical contact strip on the breadboard.

![](../../.gitbook/assets/image%20%28294%29.png)

#### For the negative side

1. The component's negative \(ground or GND or -\) pin will be in a separate numbered electrical contact strip
2. Use an additional wire from the same contact strip as the component's GND pin to the blue negative \(ground\) rail on the breadboard.

![The ground wire is on the right.](../../.gitbook/assets/image%20%28278%29.png)

Because these rails are connected to the circuit board, there is no additional need for connections for power or to complete the circuit.

**Connecting Data Pins**

For components with data pins \(such as "Trig" and "Echo" in the example\), the component's data pins will be in separate electrical contact strips.

Connect these directly to the analog or digital pins on the circuit board.

![The yellow and green wires connect the data pins to the digital pins 6 and 7 on the circuit board.](../../.gitbook/assets/image%20%28287%29.png)

The image above has the same positive and negative \(ground\) connections but is shown using the rail on the other side of the breadboard.

### Other Way to Complete a Circuit

Some simple setups don't need a positive wire. The data connection also serves as the positive charge.

![](../../.gitbook/assets/image%20%28307%29.png)

Notice that only the negative rail is created here and the positive charge is coming through the connection from the positive side of the LED component to pin 9 on the circuit board. This connection completes the circuit AND controls the component.

#### Resistors

Resisters change the amount of power going through and in these simple circuits, they can be connected between the component and the GND or between the positive line and the component. The diagrams on this Gitbook will have them on the positive end.

![These two are the most common for beginners.](../../.gitbook/assets/image%20%28283%29.png)



