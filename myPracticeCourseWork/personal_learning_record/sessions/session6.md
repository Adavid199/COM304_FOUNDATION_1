[Personal Learning Record](../../personal_learning_record/personal_learning_record.md) | [Session Notes](../sessions/README.md) 

# Session 6

## Topics covered
*What topics were covered in this session*
Introduction to operating systems, playing with linux

This line labels a practical class session: an introductory lecture on operating systems followed by a hands‑on lab where students “play with Linux.” The session combines core OS concepts with guided, experiential work in a Linux environment so learners can apply theory to real systems.Understand fundamental OS concepts: processes, scheduling, memory management, file systems, and permissions.Develop troubleshooting skills: inspecting processes, monitoring resources, and reading system logs.

Gain basic command‑line proficiency: navigation, file manipulation, text tools, and editors.Learn system administration primitives: user/group management, services, package management, and logs.Possible checkpoints: successful VM build, working script, or solved troubleshooting scenario.

Provides operational skills needed to manage cloud hosts, virtual desktop backends, or thin‑client images referenced elsewhere on the page.Familiarity with Linux improves troubleshooting of network, virtualization, and container issues highlighted in the technical feasibility and pilot sections.Skills learned reduce vendor lock‑in risk by enabling in‑house management of open‑source components and cost‑effective operational support.

This line describes the planned progression in a practical module: students will extend their low‑level programming work by first experimenting with Assembly and C using the CPUlator (a CPU emulator), then move to running equivalent Assembly and C code on real hardware (a Raspberry Pi). The surrounding page’s emphasis on hands‑on foundations and systems skills makes this a staged bridge from safe, observable experimentation to real‑world hardware behaviour.Understand CPU fundamentals by observing instruction execution, registers, and memory behaviour in a controlled emulator.

Translate concepts between levels by writing the same routines in Assembly and C and seeing how high‑level constructs map to machine instructions.Develop practical toolchain skills (assemblers, linkers, cross‑compilation) that are essential for building system images and low‑level utilities.Observe real hardware effects (timing, I/O, peripheral behaviour) that differ from emulator expectations when code runs on a Raspberry Pi.





## Personal Notes and research following this session
*Which class sessions and personal research refers to technology in this proposal. Link to examples.*

Introduction to operating systems, playing with Linux and Assembler/C on CPUlator → Raspberry Pi.Proposal technologies like cloud desktops, virtualization, authentication, booking systems, and monitoring.Operating systems & Linux labs → connects to skills in managing VDI hosts, troubleshooting shared endpoints, and scripting automation.Assembler & C progression (CPUlator → Raspberry Pi) → connects to understanding low‑level system behaviour, toolchains, and performance issues relevant to endpoint images.

connects theory to practice: linking OS fundamentals, low‑level programming, and cloud/VDI concepts to real workplace IT modernization. This section needs to clearly demonstrate how the data will be gathered and analyzed in a systematic and academically sound manner. Here you need to demonstrate that the conclusions of your research will be both valid and reliable. Common points discussed in the research design and methods section include highlighting the research paradigm, methodologies, intended population or sample to be studied, data collection techniques, and data analysis procedures.Toward the end of this section, you are encouraged to also address ethical considerations and limitations of the research process, but also to explain why you chose your research design and how you are mitigating the identified risks and limitations.

The study of operating systems forms an important and essential 
part of computer science students’ education [3,4] and as a result 
many degree level courses offer study modules on the internals of 
operating systems at introductory and at advanced levels. 
The author has been responsible for designing and delivering two 
modules on computer architecture and operating systems at 
undergraduate degree level for the past seven years. The 
Permission to make digital or hard copies of all or part of this work for 
personal or classroom use is granted without fee provided that copies are 
not made or distributed for profit or commercial advantage and that 
copies bear this notice and the full citation on the first page. To copy 
otherwise, or republish, to post on servers or to redistribute to lists, 
requires prior specific permission and/or a fee. The CPU simulator simulates the hardware functionality of a 
fictitious, but highly realistic, CPU based on RISC type 
architecture. It incorporates a five-stage pipeline simulator and 
both data and instruction cache simulators. The CPU simulator 
can execute instructions either generated by the integrated 
compiler from high-level source code or manually entered by the 
students. Multiple CPU simulations are supported and can be used 
to simulate parallel processors. The OS simulator is designed to support two main aspects of a 
computer system’s resource management: process management 
and memory management. The CPU code is visible to the OS 
simulator which is able to create multiple instances of the code as 
separate processes. The process scheduler includes support for 
scheduling policies including priority-based, pre-emptive and 
round-robin scheduling with selectable time slots. Virtual 
resources can be allocated and de-allocated to processes allowing 
demonstration of deadlocks associated with resources and 
investigation of deadlock prevention, detection and resolution 
techniques. Threads are supported via special teaching language 
constructs which allow parts of program code to be executed as 
threads and process synchronization concepts to be explored. An important area of modern computer organization and 
architecture is the operating system the internals of which is 
normally inaccessible for teaching and learning purposes. This 
proposal describes an educational operating system simulator that is 
part of an integrated set of simulators designed to support students 
of computer architecture and operating systems. Examples of 
classroom assignments are presented demonstrating the 
simulator’s support for a wide range of practical experiments. The 
pedagogical value of the simulator is assessed in terms of the 
educational impact of its visualization features and its functional 
capabilities for supporting students at different levels of learning. 
Finally, the preliminary results of the evaluation of the simulator 
that provide an indication of its value as a teaching and learning 
resource are presented.


https://dl.acm.org/doi/pdf/10.1145/2047594.2047650

## Exercises and results
*What exercises did you complete. What results. Screen shots and notes*

The line “CPUlator Seven Segment Displays” refers to a practical exercise described in the session materials on the GitHub page you’re viewing. It highlights how students use the CPUlator emulator to learn Assembly and C programming by manipulating a simulated seven‑segment display.A simple electronic display made up of seven LEDs arranged in a figure‑8 pattern.

By turning segments on or off, you can represent digits (0–9) and some letters.

Commonly used in calculators, clocks, and embedded systems.

CPUlator provides a virtual environment where students can write Assembly or C code to control the segments.

Code interacts with memory‑mapped I/O registers that represent the display hardware.

Students can experiment with setting bits in registers to light up specific segments, thereby forming numbers or patterns.

The emulator shows the output visually, so learners can immediately see the effect of their code.

Hands‑on learning: Reinforces how low‑level code interacts with hardware devices, bridging theory from operating system structure to practice.

Assembler and C integration: Demonstrates how both languages can manipulate the same hardware registers, showing the relationship between high‑level and low‑level programming.Preparation for Raspberry Pi work: Builds skills in controlling peripherals via code, which is directly transferable when moving from CPUlator to real hardware experiments on the Raspberry Pi.

Systems understanding: Helps students grasp concepts like memory‑mapped I/O, bitwise operations, and device drivers—core topics in operating systems and embedded programming.

“CPUlator Seven Segment Displays” is the lab exercise where students practice writing Assembly and C code to control a simulated hardware display in CPUlator, giving them a safe, visual way to understand how software drives hardware before applying those skills on real devices like the Raspberry Pi.

## Summary of learning
*What did you learn through these exercises*
Writing Assembly and C code in CPUlator showed how instructions execute step by step, how registers change, and how memory is manipulated.Comparing Assembly and C demonstrated how high‑level constructs map to machine instructions.Controlling the seven‑segment display taught how software drives hardware through memory‑mapped I/O.

This reinforced concepts like bitwise operations and device drivers, which are core to operating systems and embedded programming.Exercises bridged theory (OS structure: processes, scheduling, memory management) with practice on simulated and real hardware.

Running code on the Raspberry Pi revealed differences between emulator behaviour and real hardware (timing, I/O, peripheral control).Experience with assemblers, compilers, linkers, and cross‑compilation built practical skills for creating system images and utilities.Inspecting processes, monitoring resources, and reading logs in Linux labs improved your ability to diagnose and resolve issues—directly relevant to managing VDI hosts and shared endpoints in the proposal.It connects classroom learning to workplace modernization: OS fundamentals, low‑level programming, and Linux administration underpin technologies like cloud desktops, virtualization, and endpoint management.

documenting what you learned proves you can apply these skills to real IT modernization challenges (e.g., troubleshooting VDI performance, scripting automation, managing shared devices).
