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

