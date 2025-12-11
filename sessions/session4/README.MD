[Main Menu](../../sessions/README.md) | [session4](../session4/) 

# Session 4 Consolidate

There is no new material for this session. 

Use this session to consolidate your knowledge and write up what you have done so far

Session 1

 I learn about The history of computing is a progression from manual tools → mechanical automation → electronic machines → microprocessors → ubiquitous networked devices → AI-driven systems.
At its core, the story is about increasing abstraction, automation, miniaturization, and connectivity, leading to today’s intelligent, globally-interconnected computing landscape .Early Foundations (Ancient – 1800s)

Abacus (c. 2500 BCE): First known calculation aid.

Mechanical devices (1600s–1800s):

Napier’s bones, slide rule, and Pascal’s calculator automated arithmetic.

Jacquard loom (1804): Punch cards introduced programmable control.

Charles Babbage & Ada Lovelace (1830s–1840s). Charles Babbage & Ada Lovelace (1830s–1840s):

Analytical Engine: Concept of a general-purpose programmable computer.

Lovelace wrote the first algorithm and foresaw modern computing concepts. 


Electromechanical & Early Electronic Era (1900–1945)

Boolean algebra (Boole, late 1800s) → Foundation for digital logic.

Turing (1936): Universal Turing Machine formalized computation.

Electromechanical computers:

Harvard Mark I (1944): Hybrid mechanical-electrical calculator. Early electronic machines:

Colossus (1943): World’s first programmable electronic computer for codebreaking.

Paved the way for fully electronic computing. First Generation – Vacuum Tubes (1945–1955)

ENIAC (1945): First general-purpose electronic computer.

Stored-program architecture (1948):

Manchester Baby, then EDSAC, EDVAC introduced stored software.

Key ideas:

Programs stored in memory

Binary arithmetic

Input via punch cards. Second Generation – Transistors (1956–1964)

Transistors replaced vacuum tubes → smaller, faster, more reliable.

High-level programming languages emerged:

FORTRAN (1957) for science

COBOL (1959) for business

Mainframes became widespread: IBM 7090, IBM 1401. Third Generation – Integrated Circuits (1965–1975)

IC chips put multiple transistors on one semiconductor.

Gave rise to minicomputers (DEC PDP series).

Operating systems matured: time-sharing, multitasking.

ARPANET (1969): Internet’s precurs. Fourth Generation – Microprocessors & Personal Computing (1975–1990s)

Intel 4004 (1971): First commercial microprocessor.

Personal computers took off:

Altair 8800 (1975), Apple II (1977), IBM PC (1981)

Graphical user interfaces (GUIs) and mice popularized by Xerox PARC → Apple Macintosh, Microsoft Windows.

Networking expanded with TCP/IP (1983) and early Internet development.

Portable computing began to emerge.  Fifth Generation – Internet Era & Mobile Computing (1990s–2010s)

World Wide Web (1991) unlocked global connectivity.

Search engines, email, e-commerce, then social media transformed communication.

Smartphones:

Blackberry → iPhone (2007) → Android.

Cloud computing (AWS 2006 onward) enabled scalable computing and SaaS.

Moore’s Law continued shrinking transistor sizes dramatically .Modern Era – AI, Big Data, and Specialized Hardware (2010s–present)

Machine learning and deep learning became dominant with large datasets and powerful GPUs.

AI accelerators (GPUs, TPUs, NPUs) optimized neural networks.

Quantum computing research advanced (though not yet mainstream).

Edge computing, IoT, and 5G distributed computation everywhere.

Large language models (LLMs) (e.g., GPT series) redefined human–computer interaction. 


Sessions 2

I learn about Microprocessor I/O Architecture defines how a CPU communicates with external devices such as keyboards, displays, sensors, storage, and network hardware. It covers how data is transferred, how devices are addressed, and how the CPU controls or responds to I/O events. Memory-Mapped I/O (MMIO)

I/O devices share the same address space as program memory.

The CPU uses standard load/store instructions to access device registers.

Common in RISC processors (ARM, RISC-V).

Advantage: Unified addressing, simpler instruction set.
Disadvantage: Uses up address space. Port-Mapped I/O (Isolated I/O)

I/O devices use a separate address space.

CPU uses special instructions (e.g., IN, OUT on x86).

Advantage: Memory space stays free for RAM/ROM.
Disadvantage: Requires dedicated I/O instructions. Programmed I/O (Polling)

CPU repeatedly checks device status.

Simple but wastes CPU time.

B. Interrupt-Driven I/O

Device sends an interrupt signal when ready.

CPU pauses current work, executes Interrupt Service Routine (ISR).

Benefit: Efficient; CPU isn’t stuck waiting. Direct Memory Access (DMA)

A DMA controller transfers data directly between device and memory.

CPU is only notified upon completion.

Used in: disk controllers, network cards, ADC/DAC, audio interfaces. Each I/O device exposes registers for:

Status (ready/busy flags)

Control (start, stop, configure)

Data (actual bytes/words)

These registers appear either:

As memory addresses (MMIO), or

As I/O port numbers (Port-Mapped I/O).

CPU interacts by reading/writing these registers.Interrupt Architecture (Essential Concept)

Interrupts allow devices to notify the CPU. Main types:

Maskable Interrupts

Can be disabled by software.

Non-Maskable Interrupts

High-priority events (power failure, hardware faults). Vectored Interrupts

Device provides ISR address directly (fast).

Non-Vectored Interrupts

CPU must poll to identify the source.

Most modern systems use interrupt controllers (e.g., ARM GIC, x86 APIC).  Microprocessor I/O architecture defines how the CPU communicates with external devices using memory-mapped or port-mapped techniques, supports data transfer through programmed I/O, interrupts, or DMA, and uses device registers on serial/parallel buses like USB, I²C, SPI, or PCIe. Interrupt controllers, DMA engines, and GPIO pins provide efficient and flexible interaction, forming the backbone of all embedded and general-purpose computing systems.









