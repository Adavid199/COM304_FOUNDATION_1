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

Based on the surrounding page content, this section is meant to connect classroom learning with your own applied research and proposal work.It encourages you to document your reflections after completing the exercises in the session.

The focus is on linking what you learned (e.g., machine code, assembly, ARM registers, stacks, interrupts, high-level languages) to real-world technologies that you are analyzing in your IT modernization proposal.By writing personal notes, you demonstrate not just technical understanding but also the ability to reason about code and systems in a way that supports workplace technology recommendations.

The text highlights that being able to reason about code is crucial for learning to program:

If you can’t explain what a fragment of code does, you can’t debug it.

If you can’t explain your code to someone else, you can’t justify your design decisions.

To assess this reasoning ability, programs must be presented in assessment questions.

The page links to a reference language specification developed with academics (Prof. Greg Michaelson, Prof. Quintin Cutts, Prof. Richard Connor) that provides a standardized way to set such questions in schools and universities.

This shows how your personal research is expected to tie into formal educational frameworks and technology proposals.





https://www.sqa.org.uk/sqa/files_ccc/Reference-language-for-Computing-Science-Sep2016.pdf

It’s about bridging theory and practice:

Document your exercises and results.

Reflect on how they build your ability to reason about code.



## Exercises and results
*What exercises did you complete. What results. Screen shots and notes*

This section is part of your Personal Learning Record template. It is designed to help you document practical engagement with the session topics (machine code, assembly, ARM registers, stacks, subroutines, interrupts, high-level languages, etc.) and connect them to your learning outcomes.It prompts you to record the hands-on exercises you carried out during the session.

These exercises are typically done in the CPUlator ARM simulator or similar environments, where you can observe registers, flags, and memory-mapped peripherals in action.By writing down what you did, you create a traceable record of your learning journey.

Writing a simple assembly program to move values into registers.

Observing how the Stack Pointer (R13) changes when calling a subroutine.

Triggering an interrupt via a timer or UART peripheral.

Running a C program and watching how it translates into assembly/machine code.



Document the outcome of each exercise:

Did the program run successfully?

What values appeared in the registers?

How did the stack grow/shrink during function calls?

Did the interrupt handler execute as expected?


Capture CPUlator output (register states, memory views, stack pointer changes).

Screenshots serve as evidence of your work and make your notes more credible.


Add observations and reflections:

What did you learn from the exercise?

Were there any errors or debugging steps?

How does this connect to the theory (e.g., ARM documentation, high-level vs low-level languages)?


It strengthens your ability to reason about code—a skill emphasized in the research link provided earlier.

It also provides artifacts (screenshots, notes) that can support your IT modernization proposal, showing that your recommendations are grounded in hands-on technical learning.This section is essentially your lab diary:

Record the tasks you did.

Capture the results with screenshots.

Reflect with notes that tie back to the session’s learning goals.

## Summary of learning
*What did you learn through these exercises*

Reflection here shows how the exercises helped you connect theory (ARM architecture, machine code, assembly, high-level languages) with practice (CPUlator outputs, register changes, stack behavior, interrupts firing).

This is where you demonstrate growth in your ability to reason about code and systems.Machine code gives total control but is unreadable.

Assembly shows near-direct hardware operations.

High-level languages abstract away details for productivity.General-purpose registers (R0–R14) store values and calculations.

Special registers (SP, LR, PC) manage stack, subroutine calls, and program flow.


Stack pointer moves as values are pushed/popped.

Subroutines save state and return correctly via the Link Register.

Interrupts temporarily halt execution, save context, and resume smoothly.

How memory-mapped peripherals work:

Writing to specific addresses controls devices (UART, LEDs, timers).The trade-offs between interpreted and compiled languages:

Interpreted = easier to test, slower runtime.

Compiled = faster runtime, longer development cycle.Open vs closed source implications:

How sharing source code (open) vs hiding it (closed) affects learning, collaboration, and organizational choices.

Why It Matters

It strengthens your ability to justify design decisions in your IT proposal (e.g., why open-source tools might be better for flexibility, or why compiled languages might suit performance-critical systems).It shows that you are building the skill to reason about code, which the page emphasizes as essential for debugging, teaching, and professional credibility.This section is about turning practice into insight. You capture not only what happened in the exercises but also what you understood and why it matters for programming, system design, and your broader technology proposal.








