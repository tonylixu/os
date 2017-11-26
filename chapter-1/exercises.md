### In a multiprogramming and time-sharing environment, several users share the system simultaneously. This situation can result in various security problems.
* What are two such problems?
* Can we ensure the same degree of security in a time-shared machine as in a dedicated machine? Explain your answer.

Answer:
* Access to user data from different users.
* Access to system resources from different users.

Mechanisms have to be inplace to ensure that system resources such as files, memories CPUs can be operated on by only proper authorizaed processes. For example, memory-addressing hardware ensures that a process can execute only within its own address space.

### Under what circumstances would a user be better off using a timesharing system than a PC or a single-user workstation?
Answer: A scientific computing server, a compiler server or a build server.

### Describe the differences between symmetric and asymmetric multiprocessing. What are three advantages and one disadvantage of multiprocessor systems?
Answer: In an `asymmetric multiprocessing` system, each processor is assigned a specific task. For example, a boss processor controls the system, and other processors either look to the boss for instruction or have predefined tasks. In a SMP (symmetric multiprocessing) system, all the processors are peers, there is no boss processor. All processors can execute all tasks. 

Multiprocessing increases computing power, the amount of memory (if CPU has integrated memory controlelr) and multitasking. One disadvantage is multiprocessing can cause a system to change it memory access model from UMA  to NUMA (Non-uniform memory access). UMA is defined as the situation in which access to any RAM from any CPU takes the same amount of time. But with NUMA, some parts of memory may take longer to access, which creates a performance penalty.