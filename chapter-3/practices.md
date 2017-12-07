### Including the initial parent process, how many processes are created by the program shown in Figure 3.31?
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