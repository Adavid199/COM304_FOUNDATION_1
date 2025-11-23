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
