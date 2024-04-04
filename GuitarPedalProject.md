# Guitar Pedal Schematic Research

Bottom line: we need to convert the schematic to some other form, either breadboard, stripboard or PCB

## Breadboard

- Advantage is we can test and troubleshoot the circuit
- Disadvantage is breadboarding introduces problems of its own
- We still need to do a CAD layout of the schematic as the circuit is too complex to do directly on the breadboard

## Stripboard

- Two options 1. breadboard -> stripboard, 2. straight to stripboard
- What kind of stripboard? The one where we have to connect tracks or the one where we have to break tracks?
- Either way we design the layout in CAD software
- If we do 1. we should order or create breadboard-like stripboard, so as not to have to redo the layout.
- If creating, we should use the type where we break tracks

## PCB

We could skip breadboarding and stripboarding and go straight to manufacturing a single PCB. The circuit is already tried and tested, so main points of failure would be 1. human error translating the layout and 2. differences in components. In this case we should simulate as far as possible with SPICE software

What would it cost?

## SPICE simulation

Do we need to simulate the circuit at all?

## KiCad

The steps we should take are?

1. Replicate the guitar pedal schematic in KiCad itself

2. Lay it out as a either as a stripboard layout or PCB

Q: is there a dark-mode for the schematic editor?

https://github.com/pointhi/kicad-color-schemes

### Can KiCad do SPICE simulation?

KiCad supports netlist export, which allows you to export your circuit schematics in a format compatible with various SPICE simulation tools. You can then import this netlist into a separate SPICE simulator for simulation purposes.

Popular SPICE simulators that can be used in conjunction with KiCad include:

ngspice: This is an open-source SPICE simulator that is frequently used with KiCad. It's available for multiple operating systems.

LTspice: While not open-source, LTspice is a free SPICE simulator provided by Analog Devices. Many engineers use LTspice alongside KiCad for circuit simulation.

QUCS (Quite Universal Circuit Simulator): Although not strictly a SPICE simulator, QUCS is another option for simulating electronic circuits and can work in conjunction with KiCad.

### Confusion in the schematic

Q: in the hand drawn schematic i have some connections going to the negative terminal of a 9v battery and some going to a ground symbol. are these basically the same? What do they do in the stripboard circuit we can see?

Q: bottom right there are green tracks that cross, are they connected?

Q: do connections to audio jack go to tip?

Q: why do some black connections go first through the audio jack to get to negative rail of battery? Are these TRS

Q: some black connections cross, coming from 100K resistor to audio jack

To check
- that I got the pinouts of the transistors right
- results from electrical rules checker
- check that it's okay not to have some op amp chip pins connected