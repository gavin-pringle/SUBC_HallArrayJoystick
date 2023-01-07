# SUBC - Hall-Effect Sensor Array Joystick

<img src="https://github.com/gavin-pringle/SUBC_HallArrayJoystick/blob/main/3dImage.png" alt="PCB 3D Render" width="350"/>

## Use Case

- For use in pilot's joystick controlling pitch and yaw for [SUBC](subc.ca)'s 2023 human powered submarine.
- A 3D printed assembly is being designed to house and guide a magnet to travel along the up-down and left-right axes of the PCBA. This magnet is connected to a joystick handle that is contrained to move in these same axes. When the user positions the magnet in a certain direction the magnet activates the hall-effect sensors in that direction. The quad op-amp IC in the center of the PCB produces a weighted average of the hall-effect outputs, weighting the sensor further from the center greater. Each output from the op-amp IC is connected its labelled output pin in the JST connector.
- This design allows for easier waterproofing by excluding the use of potentiometers.

## Technical Specifications

- Two layer PCB, 100x100mm.
- Uses eight [DRV5055 SMD linear hall-effect sensors](https://www.ti.com/lit/ds/symlink/drv5055.pdf).
- Uses an [SMD quad op-amp](https://www.ti.com/lit/ds/symlink/lm2902-n.pdf) to average both hall-effect outputs in each direction (up, down, left, right).
- Single six pin JST connector containing PWR, GND, and analog outputs for each direction.
- Since connector is only through-hole component, entire PCBA can be easily waterproofed with potting compound for use in submarine.