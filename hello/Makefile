# common makefile type

ifneq ($(KERNELRELEASE),)
	obj-m := hello.o

else 
	KERNELDIR ?= /lib/modules/$(shell uname -r)/build
	PWD := $(shell pwd)

modules:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) modules

modules_install:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) modules_install

clean:
	rm -rf *.o *.ko .depend *.mod.o *.mod.c Module.* modules.* .*.ko.cmd .*.o.cmd

.PHONY: modules modules_install clean

endif
