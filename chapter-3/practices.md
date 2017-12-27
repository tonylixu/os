### Including the initial parent process, how many processes are created by the program shown in the following code?
```c
#include <stdio.h>
#include <unistd.h>
int main()
{
    /* fork a child process */
    fork();
    /* fork another child process */
    fork();
    /* and fork another */
    fork();
    return 0;
}
```

### Original versions of Apple’s mobile iOS operating system provided nomeans of concurrent processing. Discuss three major complications that concurrent processing adds to an operating system.

### The Sun UltraSPARC processor has multiple register sets. Describe what happens when a context switch occurs if the new context is already loaded into one of the register sets. What happens if the new context is in memory rather than in a register set and all the register sets are in use?

### When a process creates a new process using the fork() operation, which of the following states is shared between the parent process and the child process?
* Stack
* Heap
* Shared memory segments

### Consider the “exactly once”semantic with respect to the RPC mechanism. Does the algorithm for implementing this semantic execute correctly even if the ACK message sent back to the client is lost due to a network problem? Describe the sequence of messages, and discuss whether “exactly once” is still preserved.

### Assume that a distrubuted system is susceptible to server failure. What mechanisms would be required to guarantee the "exactly once" sematic for execution of RPCs?