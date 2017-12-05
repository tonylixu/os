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
Answer: The virtual memory subsystem and the storage subsystem are typically tightly coupled and requires careful design in a layered system due to the following interactions. Many systems allow files to be mapped into the VM of an executing process. On the other hand, the virtualmemory subsystemtypically uses the storage system to provide the backing store for pages that do not currently reside in memory. Also, the updates to the data on the file system sometimes buffered in memory first, then flushed to disk, thereby requiring careful coordination of design.

### What is the main advantage of the microkernel approach to system design? How do user programs and system services interact in a microkernel architecture? What are the disadvantages of using the microkernel approach?
Answer: Main advantages are: a) adding a new service is easy and not modifying the kernel. b) More secure that more operations are done outside of kernel level. c) A simpler kernel design and functionality typically results in a more reliable operating system. User programs and system services interact through MPI. The main disadvantage of microkernel is not as efficient than monolithic OS.

### What are the advantages of using loadable kernel modules?
Answer: You don't need to recompile the kernel when load a module. Less and compact kernel.

### How are iOS and Android similar? How are they different?
Answer: They both layered stack of software that provides a rich set of framework for developing mobile OS. The underline of Android is Google version of Linux, the iOS is microkernel.

### Explain why Java programs running on Android systems do not use the standard Java API and virtual machine.
Answer: For execution efficiency. The Java class files are
first compiled to Java bytecode and then translated into an executable file that runs on the Dalvik virtual machine. The Dalvik virtual machine was designed for Android and is optimized for mobile devices with limited memory and
CPU processing capabilities.

### The experimental Synthesis operating system has an assembler incorporated in the kernel. To optimize system-call performance, the kernel assembles routines within kernel space to minimize the path that the system call must take through the kernel. This approach is the antithesis of the layered approach, in which the path through the kernel is extended to make building the operating system easier. Discuss the pros and cons of the Synthesis approach to kernel design and system-performance optimization.
Answer: Synthesis is impressive due to the performance it achieves through on-the-fly compilation. Unfortunately, it is difficult to debug problems within the kernel due to the fluidity of the code. Also, such compilation is system specific, making Synthesis difficult to port (a new compiler must be written for each architecture).