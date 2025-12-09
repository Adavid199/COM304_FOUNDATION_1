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

 Introduction to computer systems architecture and 
programming is a ‘100’ course offered on the Economics, Management, 
Finance and the Social Sciences (EMFSS) suite of programmes.
 The computer has become an integral part of our lives. Apart from the 
computer you use to write your coursework and to communicate with 
friends, there is the computer technology embedded in your coffee maker 
that detects how hot to brew your coffee, in your mobile telephone, in the 
ticket reader that deducts your bus fare directly from your bus pass, in the 
ATM (automatic teller machine) that disposes your money for the week, etc. 
The list is huge and is getting longer each day.
 However, most of the users of these technologies have little or no 
knowledge of the history of this phenomenal development and little 
understanding of how a computer works. For most, the computer remains a 
black box that magically runs software applications. In this course you will 
learn how a computer’s architecture provides for the computer services we 
have become so accustomed to using.

this section is about mapping your academic learning and personal research directly to the technologies you are recommending in your IT modernization proposal. It ensures that your proposal is not just opinion-based but grounded in evidence from coursework and external study.To show the origin of your knowledge: which class sessions introduced the concepts, and which personal research expanded them.

To link theory to practice: demonstrating how classroom exercises (e.g., CPUlator, Raspberry Pi GPIO experiments) connect to real-world workplace technologies (e.g., hot desking, cloud desktops, hybrid work infrastructure).

To strengthen credibility: by citing examples, guides, or specifications that support your proposal.

CPU Architecture: Learning how a CPU is built from logic gates and how registers, stacks, and interrupts work.

Connection: Helps explain how modern operating systems manage multitasking and process scheduling.High-Level Languages: Understanding interpreted vs compiled languages.

Connection: Informs organizational choices between scripting tools (Python, Node-RED) and compiled systems (C/C++).

Raspberry Pi IO Experiments: Using Node-RED and WiringPi to control LEDs and peripherals.

Connection: Demonstrates how low-level hardware control links to automation and IoT in workplace technology.

Node-RED: A low-code programming tool developed by IBM, useful for connecting hardware, APIs, and online services.

Example: Installing Node-RED on Raspberry Pi and building a traffic light sequence flow.WiringPi: A C-based library for GPIO programming.

Example: Testing input/output with scripts and observing results.

Open vs Closed Source: Research into Linux and gcc as open-source tools versus proprietary platforms.

This section demonstrates that your proposal is evidence-based.

It shows that you are not just recommending technologies (like cloud desktops or hot desking) in isolation, but grounding them in academic learning outcomes and practical experiments.

Linking to examples (like Node-RED traffic light flows or WiringPi test scripts) provides artifacts that make your proposal more credible and professional.


This section is about tracing the roots of your proposal technologies back to your learning and research. By explicitly linking class sessions and personal study to your recommendations, you show that your proposal is well-founded, academically supported, and practically tested.

[J. Matravers 2011, Introduction to computer systems architecture and programming, Course notes LSE](https://www.london.ac.uk/sites/default/files/uploads/is1168-introduction-computer-systems-architecture-programming-study-guide.pdf)

[Node Red Documentation Accessed 2025](J[. Matravers](https://nodered.org/docs/))

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

To document the exercises you performed (e.g., programming GPIO pins, building traffic light flows, testing WiringPi scripts).

To record the results of those exercises (e.g., LEDs switching correctly, timing sequences working, GPIO responding to input/output).To include screenshots of your Raspberry Pi or CPUlator outputs as proof of completion.

To add notes and reflections that explain what happened, what you observed, and how it connects to the theory.

Installing Node-RED on Raspberry Pi

Accepting default configuration scripts and enabling GPIO library.

Traffic Light Switching Flow

Using inject nodes to control LED timing (15-second sequence).

Synchronizing northbound and southbound traffic lights with delay nodes.WiringPi Test Scripts

Running input/output tests to confirm GPIO pin control.

Gertboard Setup

Wiring LEDs and testing with simplified schematics.

Node-RED successfully controlled LEDs in the correct traffic light sequence.

Delay nodes kept timing synchronized without drift.

WiringPi scripts confirmed GPIO pins could be toggled between input/output states.

Screenshots of Node-RED flows and terminal outputs validated the experiments.This section provides evidence of hands-on learning.

Screenshots and notes make your record credible and traceable.

Documenting results helps you reflect on what worked, what didn’t, and why.

It bridges the gap between abstract CPU architecture and real-world device control.





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
this section is meant to capture your reflections and insights after completing the practical work with the Raspberry Pi and its GPIO experiments. It goes beyond listing tasks or results — it asks you to articulate what understanding you gained and how the exercises connect to broader concepts in computer systems architecture.To demonstrate learning outcomes, not just activity logs.

To show how hands-on experiments (Node-RED flows, WiringPi scripts, traffic light circuits) helped you understand how software and hardware interact.

To bridge the gap between abstract CPU architecture and real-world device control.

How GPIO pins work: Configuring them as inputs or outputs, and how they can control external devices like LEDs.

Software-to-hardware interaction: How Node-RED and WiringPi abstract away complexity, letting you manipulate hardware with higher-level tools.Timing and synchronization: Using inject and delay nodes in Node-RED to keep traffic light sequences aligned, and why synchronization matters to avoid drift or errors.

Peripheral drivers and interrupts: How hardware experiments connect to system-level concepts such as timing, interrupts, and peripheral management.Practical debugging skills: Observing results, adjusting flows or scripts, and ensuring the hardware responds correctly.

Link to architecture concepts: Seeing how CPU design (registers, memory, I/O mapping) underpins the ability to control external devices.

This reflection shows that you are not just following instructions but developing reasoning skills about code and systems.

It connects your lab work to proposal technologies (e.g., automation, IoT, open-source tools).

It demonstrates growth in your ability to explain how and why things work, which is essential for debugging, teaching, and professional IT practice.

This section is about turning practice into understanding. You capture the concepts and skills gained — such as hardware control, timing, abstraction, and system-level connections — and explain how these exercises deepened your knowledge of computer systems and their application in real-world technology.
