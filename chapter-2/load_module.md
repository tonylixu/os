### How to Write a Simple Kernel Module?

In this blog, you will learn how to create a kernel module and load it into Linux Kernel in AWS EC2 environment. Since you are directly interact with the Kernel, there is a possibility that you could crash the kernel, well, another reason why you should use a cloud platform such as AWS EC2. You can simply spin up and tear down servers.

### Preparation:
* OS: Ubuntu 16.04.3 LTS (I tried RedHat 7 and Amazon Linux AMI 2017.09.1, didn't work for me, so hard to get the necessary lib installed)
* You need to install the following packages:
```bash
# apt-get install build-essential linux-headers-$(uname -r)
```
* At least a open SSH port (22) on your AWS EC2 server.

### The Kernel Module
Creating the kernel module called "simple.c":

### The Makefile
Create the `Makefile`

Note: Make sure you use tab instead of spaces. Otherwise you will see "Makefile:3: *** missing separator.  Stop." error.

### Compile and Generate Kernel Module
```bash
$ make
make -C /lib/modules/4.4.0-1041-aws/build M=/home/ubuntu modules
make[1]: Entering directory '/usr/src/linux-headers-4.4.0-1041-aws'
  Building modules, stage 2.
  MODPOST 1 modules
make[1]: Leaving directory '/usr/src/linux-headers-4.4.0-1041-aws'
$ ls
Makefile  modules.order  Module.symvers  small.c  small.ko  small.mod.c  small.mod.o  small.o
```
The "make" command will create a "small.ko" file, this is the compiled module file.

### Load and Unload Module
```bash
$ sudo insmod small.ko
$ dmesg | tail -1
[ 6751.246020] Loading Module small
$ sudo rmmod small.ko
$ dmesg | tail -1
[ 6796.304281] Removing Module
```

When a module is inserted into the kernel, the `module_init` macro will be invoked, which will call the function `small_init`. Similarly, when the module is removed with `rmmod`, `module_exit` macro will be invoked, which will call the `small_exit`. Using dmesg command, we can see the output from the sample Kernel module.