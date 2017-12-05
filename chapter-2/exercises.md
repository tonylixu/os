### The services and functions provided by an operating system can be divided into two main categories. Briefly describe the two categories, and discuss how they differ.
Answer: One set of categories provides functions that are help to the user, such as:
* User interface; program execution; I/O operations; File-system manipulation; communications and Error detection.

The other set of categories provides functions to ensure the efficient operation of OS itself. Such as:
* Resource allocation
* Accounting
* Protection and security

### Describe three general methods for passing parameters to the operating system.
Answer:
* Pass parameters in registers
* Registers pass starting address of blocks of parameters
* Parameters can be placed or pushed onto the stack by the program, and popped off the stack by the OS.

### Describe how you could obtain a statistical profile of the amount of time spent by a program executing different sections of its code. Discuss the importance of obtaining such a statistical profile.
Answer: You could inject timers into the program at different sections. A statistical profile of which pieces of code were active should be consistent with the time spent by the program in different sections of its code. This profile could help the programer to identify the bottlenecks and optimize the program.

### What are the five major activities of an operating system with regard to file management?
Answer:
* Create
* Delete
* Change ownership and mode
* Copy files
* Backup files

### What are the advantages and disadvantages of using the same systemcall interface for manipulating both files and devices?
Answer: It will be easy to add a new device driver by implementing the hardware-specific code to support this abstract file interface. The disadvantage with using the same interface is that it might be difficult to capture the functionality of certain devices within the context of the file access API, thereby resulting in either a loss of functionality or a loss of performance. 

### Would it be possible for the user to develop a new command interpreter using the system-call interface provided by the operating system?
Answer: Totally, the command line interpreter allows an user to create and manage processes and also determine ways of communication. All of these required functionalities are accessable by user level program using system calls.

### What are the two models of interprocess communication? What are the strengths and weaknesses of the two approaches?
Answer:
* MPI (Message passing Interface):  program structures better separated, dangerous operations firewalled. Not very efficient for large data.
* Shared memory: fast and direct. Shared memory, secruity!

### Why is the separation of mechanism and policy desirable?
* The separation is needed to ensure that systems are easy to modify. With mechanism and policy separate, the policy may be changed at will while the mechanism stays unchanged. This arrangement provides a more flexible system.

### It is sometimes difficult to achieve a layered approach if two components of the operating system are dependent on each other. Identify a scenario in which it is unclear how to layer two system components that require tight coupling of their functionalities.

### What is the main advantage of the microkernel approach to system design? How do user programs and system services interact in a microkernel architecture? What are the disadvantages of using the microkernel approach?

### What are the advantages of using loadable kernel modules?

### How are iOS and Android similar? How are they different?

### Explain why Java programs running on Android systems do not use the standard Java API and virtual machine.

### The experimental Synthesis operating system has an assembler incorporated in the kernel. To optimize system-call performance, the kernel assembles routines within kernel space to minimize the path that the system call must take through the kernel. This approach is the antithesis of the layered approach, in which the path through the kernel is extended to make building the operating system easier. Discuss the pros and cons of the Synthesis approach to kernel design and system-performance optimization.