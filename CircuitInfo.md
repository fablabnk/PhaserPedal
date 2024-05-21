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