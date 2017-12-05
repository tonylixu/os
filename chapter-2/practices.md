### What is the purpose of system calls?
Answer: System calls provide an interface to the services made available by an operating system. These calls are generally written in low-level languages.

### What are the five major activities of an operating system with regard to process management?
Answer:
* Create and destroy
* Schedule
* Supervisor
* Process synchronization
* Process communication

### What are the three major activities of an operating system with regard to memory management?
* Allocating and deallocating memory space as needed
* Load and unload process/data into memory
* Keeping track of which parts of memory been used by who

### What are the three major activities of an operating system with regard to secondary-storage management?
* Storage allocation
* Free-space management
* Disk scheduling

### What is the purpose of the command interpreter? Why is it usually separate from the kernel?
Answer: Command interpreter provides a way of allowing user to use services made available by OS and hardware resources. In most Unix and Windows systems, command interpreter is just a file locater, to identify a file to be loaded into memory, itself doesn't understand the command.

### What system calls have to be executed by a command interpreter or shell in order to start a new process?
Answer: fork() followed by exec()

### What is the purpose of system programs?
Answers: To provide a convenient environment for program development and execution.

### What is the main advantage of the layered approach to system design? What are the disadvantages of the layered approach?
Answer: Layered approach break OS into small pieces that are smaller and more appropriate. This lets OS retain much greater control over hardware and over the applications that make use of hardware. It also gives more freedom to OS implementers, more system security. The main advantage is simplicity of contruction and debugging. The disadvantage of layered OS is since the higher layer can only invoke the data structures and routines in the lower layer, this structure is less efficient than other types.

### What's the advantage of monolithic structure?
Answer: Compare to Mach or MicroKernel, monolithic structure can provide a distinct performance advantage, but it is difficult to implement and maintain.

### List five services provided by an operating system, and explain how each creates convenience for users. In which cases would it be impossible for user-level programs to provide these services? Explain your answer.

### Why do some systems store the operating system in firmware, while others store it on disk?
Answer: Some OS/kernel is small enough to fit in firmware, such as cellphone or gaming machines. The OS is simplely to support the hardware, and rugged operations.

### How could a system be designed to allow a choice of operating systems from which to boot? What would the bootstrap program need to do?