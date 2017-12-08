obj-m += simple.o
all:
        (tab)make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules
clean:
        (tab)make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean