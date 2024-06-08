# V1.1

Aims:
- get it working with original BOM

Tasks:
- DONE: get schematic to pass ERC check
- mount to the case using tape etc. Case spec: HA29830PSLA: 120x95x34mm
- Audio In, Audio Out, 2 x pots, Footswitch and 9V battery will all be point-to-point wired
- DONE: use DPDT footswitch instead of SPST: it's the only footswitch we have
    - when closed, clean signal only makes it to output. when open, phased signal allowed through to be mixed with clean signal
    - we will wire only one pole and one throw of the DPDT, the other will remain disconnected
    - we presume pin 2 is connected to pin 1 when switch is in up position (clean) so will wire our phaser to pin 3 (wet)
- optimise component placement
- does jack wiring make sense? tip to ground etc?
- route it using ground plane - does power plane make sense?

# Lasercut Layout Test Notes

inline transistor footprints would have been fine!
we have no:     
    - 43K resistor:  33K + 10K
    - 3.9K resistor: 3.3K + 68
    - 39K resistor: 33K + 5.1K
    - 510K resistor: 470K + 47K (or use chunky brown one)
    - we have 510, 390, and 130's in brown chunky type
154s are too small, need to use a longer footprint 0.9mm between

# Workflow

- rework the schematic - modular with labels - more clarity
- simulate the circuit so we can test the different stages
     - preamp
     - all-pass
     - LFO
     - foot switch
- eliminate weird resistor values from circuit
- decide on PCB size
- layout PCB according to 5 sections
- route ground plane (back)
- route signal plane (front)
- send for manufacture

# Understanding the Circuit

5 x LM741 - op amps
4 x 2N5457 FET transistors
3 x 2N3904 transistor

1. Input
    - Guitar preamp
    - 1 x 2N3904 transistor
    - Clean signal to output jack
    - Clean signal to phasers shifter

2. Phaser Shifter
    - AKA an all-pass filter
    - consists of 4x LM741 op amps
    - shifts the phase based on signal from the LFO

3. LFO 
    - outputs a CV to the all-pass filter
    - consists of an LM741 op-amp, 50K pot and 4 x 2N5457 transistors

4. Output
    - Output of phaser shifter goes to foot switch
    - When switch is open only the clean signal passes through to output
    - When switch is closed the phase shifted signal passes through a 50K pot, which determines how much of it is mixed with the clean signal
    - what is purpose of trimpot?

5. Power    
    - drops voltage from 9V battery: first to 7V then 4V (using 2 x 2N3904 transistors)
    - 7V goes to guitar preamp transistor
    - 5V goes to all-pass filter 4 x 2N5457 transistors, then to LM741's

# PCB Size

mount points

# 