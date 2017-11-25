### What are the three main purposes of an operating system?
The three main purpose of an OS are:
* To provide an environment for users to execute their programs on computer hardware in a convenient efficient manner.
* Process management, the resource allocation between applications should be as fair and efficient as possible.
* Supervision of running processes, and management of I/O devices.

### We have stressed the need for an operating system to make efficient use of the computing hardware. When is it appropriate for the operating system to forsake this principle and to “waste” resources? Why is such a system not really wasteful?
* Single graphic user system should provide a good user experience for the user. HA (high availability) system with a second server in stand-by mode can also count.

### What is the main difficulty that a programmer must overcome in writingan operating system for a real-time environment?
* The task scheuduling. If a task doesn't complete in a certain time frame, it will cause a breakdown of the entire system. A programmer must make sure the response time doesn't exceed the time constraint.

### Keeping in mind the various definitions of operating system, consider whether the operating system should include applications such as web browsers and mail programs. Argue both that it should and that it should not, and support your answers.
* I think the OS should not embedd applications like web browser, mail and etc. First of all, there are applications, should stay out of kernel space. Second, include these applications could make OS more and more fat. Third, the more applications you embedded in OS, the more security risk and volunerabilities you are putting into the OS.

### How does the distinction between kernel mode and user mode function as a rudimentary form of protection (security) system?
* Normally a `mode` bit is being used and added to the hardware of the computer to indicate the current mode: kernel(0) or user(1). With the mode bit, we can distinguish between a task that is executed on behalf of the OS and the one is executed on behalf of user. When the system is executing on behalf of a user application, the system is in user mode. However, when a user application requests a service from the OS, the system must transition from user mode to kernel mode.

### Which of the following instructions should be privileged?
* Set value of timer. - previleged
* Read the clock.
* Clear memory. - previleged
* Issue a trap instruction.
* Turn off interrupts. - previleged
* Modify entries in device-status table. - previleged
* Switch from user to kernel mode.
* Access I/O device. - previleged

### Some early computers protected the operating system by placing it in a memory partition that could not be modified by either the user job or the operating system itself. Describe two difficulties that you think could arise with such a scheme.
* The data required by the OS would have to be passed or stored in the memory and thus be accessible to unauthorized users.

### Some CPUs provide for more than two modes of operation. What are two possible uses of these multiple modes?
* Provide an enhanced security policy. If distinguish between user and kernel mode are not enough. For example, you could distinguish between different types of user mode, lock down the security permission at user group level.
* Provide different distinctions within kernel code. For example, a specific mode could allow USB device drivers to run, this could mean that USB device can be served without switch into kernel mode.