
This was a project to build a [Phaser Guitar Pedal from Instructables](https://www.instructables.com/Phaser-Guitar-Pedal/). 

As we attempted the project, we found that the build steps in the photos were incomplete, so it is actually impossible to place all components and make all the solder connections on the protoboard in the same way they did.

Our solution was to attempt to rework a new layout directly from the schematic in KiCad, partly as a learning experience in how to use KiCad at all. This involved:

- recreating the schematic in the schematic editor
- creating a board template in the pcb editor and placing components as similarly as possible to the original project
- routing the rats nest
- using the routings as a template for soldering

- some connections are done with solder bridges, some with wires - the wires are the traces - but how did we do solder bridges again?

The current state of the project is that the circuit doesn't work and we're not sure why. One wire got disconnected so this could help.

A possible next step could be to manufacture a PCB, but we have no guarantee that we routed it correctly or that the project even works in the first place.

So it would be better to go back to first principles to understand the concepts in the circuit