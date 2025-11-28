[Personal Learning Record](../personal_learning_record/personal_learning_record.md) | [Personal Reflection](../personal_learning_record/personalReflection.md) 

# personal reflection

---
**NOTE**

* At the conclusion of the module, describe how you have progressed.
* 
it demonstrates self-awareness, critical thinking, and the ability to connect theory with practice.Describe how your skills, knowledge, or confidence have evolved. For example, you might have moved from basic familiarity with cloud infrastructure to confidently drafting modernization proposals.Highlight fresh concepts, tools, or methods you encountered (e.g., virtualization labs, hot desking case studies, or automation scripts).Acknowledge challenges—whether technical (troubleshooting Linux utilities) or conceptual (linking research evidence to workplace proposals).Document independent exploration, such as reading case studies, experimenting with Raspberry Pi, or benchmarking systems.Outline how you plan to extend your learning, whether through deeper research, applying skills in real-world projects, or refining proposal-writing techniques.
  
* Start by recalling your baseline knowledge at the beginning of the module.Celebrate achievements but also admit difficulties.

This balance shows maturity and self-awareness.Identify challenges and how you addressed them.Outline steps to consolidate and extend your learning.Celebrate achievements but also admit difficulties.

Contrast it with your current capabilities, showing tangible growth.

* What have you learnt that is new.
* 
Microprocessor IO architecture describes how a processor exchanges data with the outside world — the buses, ports, controllers, and protocols that connect the CPU and memory to sensors, displays, storage, and other peripherals.Microprocessor I/O architecture is the set of hardware and low‑level mechanisms that enable communication between the processor, memory, and peripheral devices. It covers the physical interfaces (pins, ports, buses), the logical mapping of devices into the processor’s address or port space, and the control logic that coordinates transfers.CPU and Control Unit coordinate I/O operations and generate control signals.System Bus (address, data, control lines) carries information between CPU, memory, and I/O.Memory‑Mapped I/O treats device registers as memory addresses so normal load/store instructions access devices.Port‑Mapped I/O (or isolated I/O) uses a separate instruction set or address space for device access.

Programmed I/O (Polling) has the CPU repeatedly check device status.

Interrupt‑Driven I/O lets devices signal the CPU when they need attention, reducing wasted cycles.

Port‑Mapped I/O (or isolated I/O) uses a separate instruction set or address space for device access.

I/O Controllers and Peripheral Devices act as intermediaries (e.g., UARTs, network controllers, ADCs).For larger or time‑sensitive transfers, architectures often include Direct Memory Access (DMA) engines that move blocks of data between memory and peripherals without continuous CPU intervention, and prioritisation/arbiter logic on shared buses to manage contention. These mechanisms are part of designing an I/O subsystem that meets throughput and latency goals.

Raspberry Pi is a hands‑on introduction to a small, affordable computer: set it up (power, microSD, peripherals or headless SSH), explore its desktop or command line, and run simple projects to learn hardware and software basics.
  
Raspberry Pi as a learning platform. It prepares you to complete later labs that involve GPIO, sensors, and small‑scale systems work, and it ensures you can capture evidence (code, screenshots, notes) for your Personal Learning Record.to perform are: prepare a boot medium (microSD with an OS image), connect a power supply, and choose whether to run the Pi with a monitor/keyboard or headless over the network via SSH. The official Raspberry Pi documentation and beginner guides walk through these exact steps and the options for desktop vs headless operationbasic system use and exploration: booting the Pi, navigating the desktop or terminal, using the package manager, and running simple programs. It also introduces digital making concepts—connecting components, reading sensors, and controlling outputs—so you can move from theory to small projects and experiments..

Package management is taught as a hands‑on system administration skill so you can prepare and maintain the software environment on a Raspberry Pi or server used in labs. The course places it alongside kernel history, basic Linux commands, and Apache installation to show it is a prerequisite for later practical tasks and assessments.A package manager automates software lifecycle tasks: locating packages in repositories, resolving and installing dependencies, upgrading software, and removing packages cleanly. This avoids manual compilation and reduces errors when assembling a working system. Package managers also provide commands to query installed versions and verify package integrity.Different Linux distributions use different managers: Debian/Ubuntu use apt, Red Hat/Fedora use dnf/yum, Arch uses pacman, and lightweight systems may use apk (Alpine). Each has its own commands and repository model, but all serve the same core purpose of managing packages and dependencies, include the distro and manager used, the exact commands you ran, outputs or screenshots, and one troubleshooting example (for instance resolving a dependency conflict or adding a repository). Showing these concrete steps demonstrates practical competence and reproducibility for assessors.mastering package management makes your labs repeatable and maintainable; document commands, evidence, and one resolved problem to show real learning and readiness to manage systems in practical settings.



* What have you struggled with.
* What personal research have you done.
* What will you need to do next to consolidate your knowledge.

---


TBD
