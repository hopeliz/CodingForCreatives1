# The Setup

With Arduinos, you are setting up a complete circuit that powers the circuit.

## General Setup

### Power Flow

Some ways to think about how power flows through a circuit:

1. Complete ring - if it's not complete, it won't work. Adding things to this ring will be powered if the ring is complete.
2. Computer/power source end of the circuit board as a heart, Arduino processor as the brain, and components are limbs. - Positive charge is like oxygenated blood \(seen as red arteries on diagrams\) comes from the heart/lungs to the limbs for them to work. After supplying oxygen to the limbs, the deoxygenated blood \(seen as blue veins on diagrams\) returns to the heart and the cycle starts again. The brain needs power to work and the wires from components to analog and dialog pins send data to the processor just like the nerves in a limb send information to the brain.

### The Order

The order usually goes:

1. Power source \(computer, wall outlet, or battery component\) to USB 2.0 connection or power port on circuit board
2. Wire from 3.3V or 5V pin \(i/o hole\) on the circuit board to the red positive rail on the breadboard
3. Second wire from red positive rail on the breadboard to a numbered electrical contact strip on the breadboard \(see note on number 5\)
4. Component's positive pin \(often marked with a + or Vcc\) in the same electrical contact strip on the breadboard \(see note on number 5\)
5. Component's data pins \(this will either get or send data\) in separate electrical contact strips
   1. **Note:** this data connection sometimes replaces the positive pins/wire connection \(please see diagrams\)
6. Component's negative \(ground or GND or -\) pin in a separate electrical contact strip
7. Third wire from the same contact strip as the component's GND pin to the blue negative \(ground\) rail on the breadboard
8. Fourth wire from the blue negative \(ground\) rail on the breadboard to the gound \(GND\) pin \(i/o hole\) on the circuit board.



#### Data Pins on Components

For the components with data pins, connect an additional pin from the same electrical contact strip as the data pin on the breadboard to the analog or digital pins \(i/o holes\) on the circuit boards.

#### Data From Components Without Data Pins

For those without data pins, but controlled with or capturing data, connect an additional wire from the same electrical contact strip as the component's positive pin on the breadboard to an analog or digital pin \(i/o hole\) on the circuit board. This takes can take the place of the wire connecting the positive rail to the component.

#### Resistors

Resisters change the amount of power going through and in these simple circuits, they can be connected between the component and the GND or between the positive line and the component.

## Example Component Setups

This section will be completed soon.



