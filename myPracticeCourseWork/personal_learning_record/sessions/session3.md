[Personal Learning Record](../../personal_learning_record/personal_learning_record.md) | [Session Notes](../sessions/README.md) 

# Session 3

## Topics covered
*What topics were covered in this session*
ARCHITECTURE
How a CPU could be constructed using logic gates.
How to zoom back out and look at how a computer like the Raspberry PI communicates with outside world.
Diagram illustrating peripherals architecture on PI
PI3 Broadacom BCM2837 chip.
Processing unit (GPU)
Driver for USB, Ethernet and general purpose IO (GPIO) peripherals.
Raspberry PI
Use of application called (Node RED)
Raspberry PI labrary called (WiringPi) to manipulate the GPIO and control ecternal LED ligths.
Programming the GPIO directly using assembler language and C

this section is about hands-on activities using the Raspberry Pi’s GPIO (General Purpose Input/Output) pins to understand how the Pi communicates with the outside world.To move beyond CPU architecture and explore how a computer like the Raspberry Pi interacts with external devices.

The GPIO pins allow you to connect LEDs, sensors, motors, and other peripherals, making the Pi a flexible platform for experimentation.These exercises help you see how low-level hardware control links to higher-level programming tools.


Using the 40-pin GPIO connector:

Internally mapped as GPIO 0–25 (though pin mapping varies between Pi versions).

Pins can be programmed as INPUTs (to read signals) or OUTPUTs (to send signals).

Some pins can also act as serial ports or clocks for external devices.

Node-RED: A flow-based programming tool that lets you visually connect logic blocks to control GPIO pins.

WiringPi library: A C-based library that simplifies GPIO programming.

Traffic Lights:

Guest lecturer Bob Potter provided a simple traffic light circuit using LEDs and Node-RED.

This can be built with discrete components on a breadboard or using the Gertboard, a Pi add-on board designed for GPIO experiments.

The traffic light flow works both with standalone LEDs and with the Gertboard’s built-in components.


Through these experiments, you learn:

How to configure GPIO pins as inputs/outputs.

How to control external hardware (like LEDs) using software.

How tools like Node-RED and WiringPi abstract away complexity, making GPIO programming more accessible.

How hardware experiments connect to system-level concepts like interrupts, timing, and peripheral drivers.

This section is about getting practical experience with Raspberry Pi IO. By wiring up LEDs or using the Gertboard, and controlling them with Node-RED or WiringPi, you see how software directly manipulates hardware. These experiments bridge the gap between abstract CPU architecture and real-world device control.



## Personal Notes and research following this session
*Which class sessions and personal research refers to technology in this proposal. Link to examples.

NODE-RED
Low code programming tool developed by IBM that connects hardware devices,APIS and online service together
installing NODE RED on Rasberry PI
Installing NODE RED commands
node -red- start # to start
node-red-stop # to stop
Simple Node Red Traffic light
Traffic light sequence
RED
RED and AMBER
GREEN
AMBER
RED
WIRING CIRCUIT FLOWS
Getting Gertboard to work with the PI and wiring PI library
Assembled gertboard schamatics
gertboard user manual
Getboard Overview
Simplefied Getboard setup
TEST input and output using wiring PI
WiringPi Test scripts




## Exercises and results
*What exercises did you complete. What results. Screen shots and notes*
INSTALL NODE RED ON RASPBERRY PI
This will show you how to a scprit to install NODE RED
Accept the default for the configuration scripts
Accept the installer option to install standard GPIO library
Traffic light switching 

The sequence length ( T seconds) last for 15 seconds before it repeat,This timing is carried out by the inject nodes 2 off switching light on and  2 off for switching light off all 4 for being set to an interval of 15 seconds.
The phase of the lights between the north bound traffic and the south bound traffic is achiecved by a second set of inject nodes being delayed from startup by T/2 seconds.
The individual switching off the light of is controlled by judiciously placing delay nodes at the required interval 16 in total note that the sequence delay must remain synchronised otherwise there could be slip that wouuld be disasterous over time node red inject node timings is ganged to the internal real time clock of the host processor so this should not be a problem.

## Summary of learning
*What did you learn through these exercises*
The art science of designing and constructing building other structure,blending creativity with technical knowledge to create functional safe device in environment.
A primary goal to create spaces that are purposeful and work well for their intended use.
It invovles more than one just the physical creation compossing the planning, design and engineerihg of everything from considering factors like funtionality,sustainability context.
The desigen framework of a computer system by defining how its hardware components like the CPU memory and input/output devices interact to execute instructions.
