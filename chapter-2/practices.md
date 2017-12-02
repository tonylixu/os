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

### List five services provided by an operating system, and explain how each creates convenience for users. In which cases would it be impossible for user-level programs to provide these services? Explain your answer.

### Why do some systems store the operating system in firmware, while others store it on disk?

### How could a system be designed to allow a choice of operating systems from which to boot? What would the bootstrap program need to do?