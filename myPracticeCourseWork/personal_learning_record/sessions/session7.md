[Personal Learning Record](../../personal_learning_record/personal_learning_record.md) | [Session Notes](../sessions/README.md) 

# Session 7

## Topics covered
*What topics were covered in this session*

“Operating System Structure” on the GitHub page you’re viewing introduces a key part of the course: understanding how an operating system is organised internally. It builds on the previous session’s focus on the kernel and leads into practical exploration of Linux utilities and system management.Kernel layer: Handles CPU scheduling, memory management, device drivers, and system calls.System libraries: Provide higher‑level interfaces for applications to access kernel functions.System utilities: Tools for managing files, processes, networking, and user accounts.

User interface: Shells (command line) or GUIs that allow humans to interact with the OS.Supporting services: Daemons and background processes that manage logging, networking, and security.Foundation for Linux practice: The page directs students to start with OS structure before attempting tasks like installing Apache on a Raspberry Pi. Understanding the structure clarifies how services (like Apache) interact with the kernel, libraries, and utilities.Link to proposal technologies: Knowledge of OS structure underpins virtualization, cloud desktops, and endpoint management discussed elsewhere in your modernization proposal. Bridge from theory to practice: By studying OS structure, students can connect abstract concepts (processes, memory, scheduling) to real tools and configurations in Linux labs..


“Operating System Structure” on this page signals the transition from kernel internals to the broader architecture of an OS, using Linux as the practical case study. It sets the stage for hands‑on exercises like installing and managing services, which rely on understanding how the OS layers fit together.




## Personal Notes and research following this session
*Which class sessions and personal research refers to technology in this proposal. Link to examples.*

is a reflective instruction in your personal learning record. On the GitHub page you’re viewing, it appears in the section where you connect your course sessions and independent research back to the technologies discussed in your modernization proposal (e.g., cloud desktops, virtualization, endpoint management, booking systems).Identify relevant class sessions that introduced or practiced technologies now appearing in your proposal.Reference personal research (case studies, whitepapers, industry articles) that supports or validates those technologies.
Operating System Structure	Virtualization, cloud desktop hosts	Lab notes on Linux kernel and system utilities
Playing with Linux	Endpoint management, user accounts	Screenshots of process/file management exercises
CPUlator & Raspberry Pi labs	Low‑level troubleshooting, performance	Source code in Assembly/C and test logs
Personal research: Cloud desktop case study	Azure Virtual Desktop feasibility	Link to industry whitepaper or article
Personal research: Hot‑desking adoption	Booking systems.


These sessions directly connect to proposal technologies like virtualization, cloud desktops, and endpoint management. Your personal research (e.g., industry case studies on hot‑desking adoption or cloud desktop ROI) provides external validation.




## Exercises and results
*What exercises did you complete. What results. Screen shots and notes*
“File Systems and Security” on the GitHub page you’re viewing introduces one of the core aspects of Linux operating system structure. It highlights how files are organised and how permissions form the foundation of the OS security model.Hierarchical organisation: Linux arranges files in a tree‑like structure with standard locations for binaries, configuration files, devices, and user data.Devices as files: Even hardware components (like disks or processors) are represented as files, allowing uniform access through the file system.Consistency across distributions: While there are small differences, most Linux systems follow conventions such as /home for user directories, /etc for configuration, and /dev for devices.Ownership: Every file has an owner (a registered user) and a group. System files may be owned by root.Permission bits: Permissions are expressed in three sets of rwx (read, write, execute) for owner, group, and all users.

Directory bit: A leading d indicates a directory rather than a file.

Security model: File permissions are the primary way Linux enforces access control, ensuring only authorised users can read, write, or execute files.System integrity: Protects system files from accidental or malicious modification.

User management: Supports multi‑user environments by isolating user data and controlling shared resources.Proposal relevance: Understanding file systems and permissions is crucial for managing cloud desktops, shared endpoints, and VDI hosts—technologies referenced elsewhere in your modernization proposal. It ensures compliance, auditability, and secure operation in a hot‑desking environment.

“File Systems and Security” refers to how Linux organises files and enforces access control through permissions. It is a foundational concept in operating systems, directly tied to system stability, user management, and the secure deployment of services like those described in the proposal.





## Summary of learning
*What did you learn through these exercises*
