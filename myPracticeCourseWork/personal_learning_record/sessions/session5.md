[Personal Learning Record](../../personal_learning_record/personal_learning_record.md) | [Session Notes](../sessions/README.md) 

# Session 5

## Topics covered

*What topics were covered in this session*

Machine Code 🖥️

The raw binary instructions (0s and 1s) that a CPU executes directly.

It’s the “native tongue” of the processor, with each instruction corresponding to a very specific hardware operation.Extremely fast but unreadable to humans—think of it as the electrical pulse-level language of computing.Assembly Code ⚙️

A thin abstraction over machine code, using mnemonic symbols (like MOV, ADD, JMP) instead of raw binary.

Each assembly instruction maps almost one-to-one with machine code, but it’s far easier for humans to read and write.

Programmers often use assemblers to translate assembly into machine code automatically.

It’s still “low-level” because it requires intimate knowledge of the CPU architecture.

High-Level Languages 🌐

Languages like Python, Java, or C++ that allow programmers to write instructions in a human-friendly, abstract way.

They hide hardware details, focusing instead on logic, algorithms, and problem-solving.

Compilers or interpreters translate high-level code into machine code (sometimes via intermediate steps like assembly).

They enable portability—one program can often run on multiple hardware platforms without rewriting.

The progression from machine code → assembly → high-level languages reflects the history of computing: as hardware became more complex, humans needed more accessible ways to instruct machines. Each layer trades off control vs abstraction.

machine code gives total control but is unreadable, assembly balances readability with precision, and high-level languages maximize productivity and portability at the cost of direct hardware control.

🖥️ ARM Registers (Core of the Documentation)
General Purpose Registers (R0–R14)

Sixteen 32‑bit registers are available (R0–R15).

R0–R14 can be used freely for calculations, data storage, or passing values between instructions.Special Registers

R13 (SP – Stack Pointer): Always points to the next free space on the memory stack.

R14 (LR – Link Register): Holds the return address when a function call is made.

R15 (PC – Program Counter): Tracks the current instruction being executed. Writing to PC changes program flo

Status Registers

CPSR (Current Program Status Register): Holds condition flags that reflect the result of the last operation:

N (Negative): Set if the result was negative.

Z (Zero): Set if the result was zero (often used in comparisons).

C (Carry): Set if an addition caused an unsigned overflow.

V (Overflow): Set if a signed overflow occurred.

SPSR (Saved Program Status Register): Stores a copy of CPSR from a previous mode, useful when switching execution contexts.

⚙️ Memory-Mapped Peripherals
The documentation also explains how ARM interacts with devices:

Each peripheral (LEDs, switches, UART, timers, VGA, etc.) is mapped to a specific address range in memory.

Writing values into those addresses controls the device.

Example: Writing to the JTAG UART memory range sends characters to a simulated terminal.

The page emphasizes simplification: the real ARM 7 documentation is vast, but here only the registers and flags most relevant to programming exercises are highlighted. Learners are shown how these registers and flags change when running C or assembly programs in CPUlator.This bridges theory (ARM architecture) with practice (seeing registers update live in the simulator).

It highlights registers, flags, and memory‑mapped peripherals so you can understand how the CPUlator simulator behaves when running C or assembly code.

“Stacks, Subroutines, Interrupts” is meant as a gentle introduction to three fundamental programming concepts in the ARM simulator context. Here’s how the surrounding content frames them:

A stack is a special memory structure that works like a “last in, first out” pile.

In ARM, the Stack Pointer (R13/SP) always points to the next free space in this stack.

When functions are called, registers (like the Link Register or temporary values) are pushed onto the stack to save their state.

When the function ends, those values are popped back, restoring the CPU to its previous state.

In CPUlator, you can actually watch the stack pointer move as you step through instructions.


🔄 Subroutines
A subroutine is essentially a function: a reusable block of code that can be called from different places.

When a subroutine is called, the Link Register (R14/LR) stores the return address so the CPU knows where to continue afterward.

The stack is used to preserve register values during the call, ensuring the program can resume correctly.Subroutine program make the call to printis a subroutine call — the CPU saves state, jumps to the library code, then returns.


⚡ Interrupts
An interrupt is a signal that temporarily halts normal program execution so the CPU can respond to an event (like input from a keyboard or timer).

The CPU saves its current state (using the stack and status registers), runs the interrupt handler, then resumes the original program.In the simulator, interrupts are tied to peripherals (e.g., timers, UART, keyboard). They show how external events can “break in” and demand CPU attention.

This is crucial for real-time systems, where the CPU must react immediately to hardware signals.


Stacks, Subroutines, and Interrupts because they are tightly linked:

Subroutines rely on stacks to save/restore state.

Interrupts also rely on stacks to preserve execution context.

Together, they illustrate how ARM programs manage control flow and external events in a structured way.

Stacks, Subroutines, and Interrupts are introduced as the core mechanisms for managing program flow and CPU state. They show how ARM handles function calls, returns, and external events — all of which you can observe directly in CPUlator when stepping through assembly or C code.


High Level Languages

They are designed to let programmers express concepts and logic without worrying about the low-level details of how the CPU manipulates bits and bytes.

Examples include C, Java, Python, BASIC, JavaScript.assembly, which is tied closely to hardware registers and instructions, high-level languages abstract away those details so programmers can focus on solving problems.

Two Main Types
Interpreted Languages

Code is read and executed line by line at runtime.

Examples: Python, JavaScript, PHP, Bash.

Advantages:

Easier to write and test incrementally.

Immediate feedback when running code.

Advantages:

Easier to write and test incrementally.

Immediate feedback when running code.


Disadvantages:

Slower execution, since translation to machine code happens every time the program runs.

Bugs may only appear when specific parts of the program are executed.

Special case: Node-RED (a low-code visual tool) is essentially an interpreter that converts flow diagrams into JavaScript, then into machine code.

Compiled Languages

Code is translated into machine code ahead of time through a compilation process.

Examples: C, C++.

Advantages:

Faster execution since the program is already in machine code.

Compiler can check the entire program, catching errors and optimizing performance.

Disadvantages:

Slower development cycle because you must compile before running.

Supporting tools:

Linker: connects your program with external libraries.

Loader: places the compiled program into memory so the CPU can run it.


🔒 Open vs Closed Source
Closed Source: Companies distribute only compiled machine code, keeping the original source hidden to protect intellectual property.

Open Source: Developers share both source code and compiled binaries. Examples include Linux and the gcc compiler.

High-level languages are about human readability and productivity. They trade off direct hardware control for abstraction, making programming more accessible and efficient. The choice between interpreted and compiled languages reflects a balance between ease of development and runtime performance.



## Personal Notes and research following this session research refers to technology in this proposal. Link to examples.**

The ability to reason about code is increasingly being seen as a crucial part of 
learning to program. For example, if you can’t explain in precise detail what a 
fragment of code does, you can’t debug. If you can’t explain the code you’ve just 
written to someone else, how can you justify any of the decisions you made in 
creating it and then demonstrate any level of understanding? 
To assess candidates’ ability to reason about programs, programs must be 
presented in assessment questions. This document contains a specification for a 
reference language designed for setting such questions, developed in 
collaboration with Prof. Greg Michaelson of Heriot Watt University, Prof. Quintin 
Cutts of the University of Glasgow, and Prof. Richard Connor of Strathclyde 
University. It enables assessors, teachers and candidates to work to one well
defined notation and is suitable for use in schools and further education/higher 
education institutions.

https://www.sqa.org.uk/sqa/files_ccc/Reference-language-for-Computing-Science-Sep2016.pdf







## Exercises and results
*What exercises did you complete. What results. Screen shots and notes*



## Summary of learning
*What did you learn through these exercises*
