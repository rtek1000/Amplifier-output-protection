# Amplifier-output-protection
Thermal protection for class AB amplifier output transistors

- Most class AB amplifiers built with NPN and PNP transistors are very poor in protection.
- - Some designs put a simple current limiter, but this does not guarantee the thermal protection of the transistor.

The partial scheme of an amplifier can be seen below,
- Where there is the current limiting transistor (T10),
- The resistor 0R33 (R37) serves as a reference to monitor the current of the output transistor (T16).
- The other output transistors (T18, T20) are not monitored.

![img](https://raw.githubusercontent.com/rtek1000/Amplifier-output-protection/main/Doc/Amp_schematic.png)


The circuit of Thermal protection is based on the TL431 which is widely used in switching power supplies, this IC is very reliable.
- Each output transistor must have a 10k B3950 NTC sensor.
- The relay output can be used to jumper the signal input.
- - Some amplifier manufacturers use a fixed mechanical thermostat of about 100°C against the heatsink.

![img](https://raw.githubusercontent.com/rtek1000/Amplifier-output-protection/main/Doc/Basic_schematic.png)

The main schematic shows several blocks "NTC_sensor" so that each transistor can be monitored independently:
- If the amplifier has 20 output transistors, 20 blocks are needed.

![img](https://raw.githubusercontent.com/rtek1000/Amplifier-output-protection/main/Doc/Main_schematic.png)

## Licence:
- Hardware:

Released under CERN OHL 1.2: https://ohwr.org/cernohl

- This library is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
