[Personal Learning Record](../../personal_learning_record/personal_learning_record.md) | [Session Notes](../sessions/README.md) 

# Session 7

## Topics covered
*What topics were covered in this session*

“Operating System Structure” on the GitHub page you’re viewing introduces a key part of the course: understanding how an operating system is organised internally. It builds on the previous session’s focus on the kernel and leads into practical exploration of Linux utilities and system management.Kernel layer: Handles CPU scheduling, memory management, device drivers, and system calls.System libraries: Provide higher‑level interfaces for applications to access kernel functions.System utilities: Tools for managing files, processes, networking, and user accounts.

User interface: Shells (command line) or GUIs that allow humans to interact with the OS.Supporting services: Daemons and background processes that manage logging, networking, and security.Foundation for Linux practice: The page directs students to start with OS structure before attempting tasks like installing Apache on a Raspberry Pi. Understanding the structure clarifies how services (like Apache) interact with the kernel, libraries, and utilities.Link to proposal technologies: Knowledge of OS structure underpins virtualization, cloud desktops, and endpoint management discussed elsewhere in your modernization proposal. Bridge from theory to practice: By studying OS structure, students can connect abstract concepts (processes, memory, scheduling) to real tools and configurations in Linux labs..


“Operating System Structure” on this page signals the transition from kernel internals to the broader architecture of an OS, using Linux as the practical case study. It sets the stage for hands‑on exercises like installing and managing services, which rely on understanding how the OS layers fit together.


Kernel” on the GitHub page you’re viewing introduces one of the most fundamental components of a modern operating system. It is part of the section Operating System Structure, which explains how Linux and other OSes are organised.The kernel is the core of the operating system, responsible for managing hardware resources and providing essential services to applications.Version control: Kernels are versioned, and all libraries and programs in a system must be compatible with a specified range of kernel versions.Scheduler: Decides which processes run on the CPU and when, ensuring fair and efficient use of resources.Device drivers: Allow the OS to communicate with hardware like disks, network cards, and GPUs.Virtual memory management: Provides each process with its own address space, handles paging/swapping, and ensures isolation.File systems: Manages how data is stored, retrieved, and organised on disk.Proposal relevance: Understanding the kernel is essential for managing cloud desktops, virtualization hosts, and endpoint devices in your modernization plan. It explains why certain applications or drivers may fail if kernel versions are mismatched.Security and stability: Because all higher‑level services depend on the kernel, its correctness and compatibility are critical for system reliability.

“Kernel” here refers to the core operating system component that manages hardware and provides the essential services upon which all other parts of Linux (and other OSes) depend. It is the foundation of the OS structure described on the page.



Language Systems” on the GitHub page you’re viewing is part of the Operating System Structure section. It refers to how programming languages and their supporting libraries are integrated into a Linux environment, and what is required to run or develop software on such systems.Practical implication for students: If you only have runtime libraries, you can run existing code but not compile new programs. Installing development libraries expands your ability to experiment, build, and extend software.Connection to earlier labs: This ties directly to the CPUlator and Raspberry Pi exercises mentioned earlier—students first write Assembly and C code, then need compilers and development libraries to build and run those programs on real hardware.
Proposal relevance: In workplace modernization, understanding language systems helps when deploying cloud desktops or shared endpoints. For example, ensuring the right runtimes are available for business apps, or installing development stacks for technical teams.




## Personal Notes and research following this session

*Which class sessions and personal research refers to technology in this proposal. Link to examples.*

is a reflective instruction in your personal learning record. On the GitHub page you’re viewing, it appears in the section where you connect your course sessions and independent research back to the technologies discussed in your modernization proposal (e.g., cloud desktops, virtualization, endpoint management, booking systems).Identify relevant class sessions that introduced or practiced technologies now appearing in your proposal.Reference personal research (case studies, whitepapers, industry articles) that supports or validates those technologies.
Operating System Structure	Virtualization, cloud desktop hosts	Lab notes on Linux kernel and system utilities
Playing with Linux	Endpoint management, user accounts	Screenshots of process/file management exercises
CPUlator & Raspberry Pi labs	Low‑level troubleshooting, performance	Source code in Assembly/C and test logs
Personal research: Cloud desktop case study	Azure Virtual Desktop feasibility	Link to industry whitepaper or article
Personal research: Hot‑desking adoption	Booking systems.




These sessions directly connect to proposal technologies like virtualization, cloud desktops, and endpoint management. Your personal research (e.g., industry case studies on hot‑desking adoption or cloud desktop ROI) provides external validation.


https://walkccc.me/CS/OS/Chap02/

## Exercises and results
*What exercises did you complete. What results. Screen shots and notes*
“File Systems and Security” on the GitHub page you’re viewing introduces one of the core aspects of Linux operating system structure. It highlights how files are organised and how permissions form the foundation of the OS security model.Hierarchical organisation: Linux arranges files in a tree‑like structure with standard locations for binaries, configuration files, devices, and user data.Devices as files: Even hardware components (like disks or processors) are represented as files, allowing uniform access through the file system.Consistency across distributions: While there are small differences, most Linux systems follow conventions such as /home for user directories, /etc for configuration, and /dev for devices.Ownership: Every file has an owner (a registered user) and a group. System files may be owned by root.Permission bits: Permissions are expressed in three sets of rwx (read, write, execute) for owner, group, and all users.

Directory bit: A leading d indicates a directory rather than a file.

Security model: File permissions are the primary way Linux enforces access control, ensuring only authorised users can read, write, or execute files.System integrity: Protects system files from accidental or malicious modification.

User management: Supports multi‑user environments by isolating user data and controlling shared resources.Proposal relevance: Understanding file systems and permissions is crucial for managing cloud desktops, shared endpoints, and VDI hosts—technologies referenced elsewhere in your modernization proposal. It ensures compliance, auditability, and secure operation in a hot‑desking environment.

“File Systems and Security” refers to how Linux organises files and enforces access control through permissions. It is a foundational concept in operating systems, directly tied to system stability, user management, and the secure deployment of services like those described in the proposal.

Language Systems” here refers to the way Linux manages programming languages: providing runtime libraries for execution, development libraries for compiling, and sometimes kernel libraries for deeper system integration. It explains the difference between running software and building software, and why both matter in operating system structure and practical labs.


Boot System Structure” on the GitHub page you’re viewing is part of the Operating System Structure section. It explains how an operating system starts up and what processes are involved before the system is ready for use.Boot process definition: The sequence of steps a computer follows to load and start the operating system.Initial firmware: On PCs, the BIOS (Basic Input Output System) runs first. It is stored in ROM and provides basic diagnostics and configuration without an OS.Complexity of OS startup: The page stresses that an OS is not a single program—it requires many processes and data structures to be set up before it can run.Hardware awareness: The boot system tells the OS what hardware is installed, which is critical for device drivers and kernel configuration.Proposal relevance: For workplace modernization, understanding boot systems helps with provisioning endpoints, automating server deployment, and troubleshooting startup failures in cloud or VDI environments.

“Boot System Structure” refers to the layered process of starting an operating system: firmware (BIOS/IPMI), boot loader (like GRUB), kernel initialization, and service startup. The surrounding page uses Linux and Raspberry Pi examples to show how these steps differ across platforms and why they matter for system management.


Key Shell Commands” on the GitHub page you’re viewing is part of the Operating System Structure section. It introduces the practical tools students use to interact with Linux systems via the command line interface (CLI). These commands are foundational for navigating, managing files, monitoring processes, and configuring systems.Security awareness: Commands like ls -all reveal file permissions, tying back to the earlier section on File Systems and Security.System management: Tools like top, ps, and df -h connect directly to operating system concepts such as process scheduling and resource allocation.Proposal relevance: In workplace modernization, knowing these commands supports endpoint troubleshooting, automation scripts, and secure configuration of shared or virtual desktops.

“Key Shell Commands” refers to the essential Linux terminal commands highlighted on the page. They provide hands‑on experience with navigating the file system, managing processes, editing files, and configuring network settings—skills that reinforce the operating system concepts discussed earlier and prepare you for real system administration tasks.

“Package Management” on the GitHub page you’re viewing is part of the Operating System Structure section. It refers to one of the most important functions of modern operating systems: the ability to install, update, and remove software in a controlled way using package managers.Package management is the system that handles software distribution, installation, and maintenance.A package is a bundle containing the program itself plus metadata (dependencies, version, configuration).Managers: Tools like apt (Debian/Ubuntu) or yum/dnf (Fedora/Red Hat) automate the process of fetching, verifying, and installing packages.Repositories: Packages are stored in central repositories, ensuring consistency and security.The page highlights that package management is a key function of operating systems, allowing users to add or remove programs that run on top of the OS services.It introduces an exercise: installing the Apache 2 web server on a Raspberry Pi using package management tools.System integration: Package management ensures that installed software is compatible with the kernel and libraries already on the system.


Proposal relevance: In workplace modernization, package management underpins automation, endpoint configuration, and cloud desktop provisioning. It allows IT teams to deploy consistent environments across many devices quickly.

Package Management” here refers to the OS’s ability to manage software installation and removal through package managers. On the page, it is illustrated with the example of installing Apache on a Raspberry Pi, showing how Linux systems use tools like apt or rpm to simplify and secure software deployment.




## Summary of learning
*What did you learn through these exercises*

You learned how the kernel, libraries, and utilities interact to manage processes, memory, and devices.

This clarified how services like Apache or VDI agents depend on the OS structure.Low‑level programming (CPUlator → Raspberry Pi)

Writing Assembly and C code showed how instructions execute at the hardware level.

Running code on the Raspberry Pi revealed real‑world differences in timing, I/O, and peripheral control compared to emulation.File systems and security

You gained understanding of Linux’s hierarchical file organisation and permission model.

This reinforced how access control and ownership protect system integrity in multi‑user environments.Language systems

You saw the distinction between runtime libraries (running code) and development libraries (building code).

This connected directly to labs where compilers and toolchains were required to compile and test programs.It demonstrates evidence of learning: showing that your proposal is grounded in both theory and practice.It connects classroom labs to workplace technologies: virtualization, cloud desktops, endpoint management, and booking systems.It strengthens your proposal credibility: reviewers can see that your recommendations are backed by hands‑on experience and research.

articulate the concrete skills and insights gained from exercises like CPUlator programming, Linux labs, and OS structure studies, and link them back to the technologies in your modernization plan.




