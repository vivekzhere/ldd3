# If KERNELRELEASE is defined, we've been invoked from the
# kernel build system and can use its language.
ifneq ($(KERNELRELEASE),)
	obj-m := hello.o hellop.o

# Otherwise we were called directly from the command
# line; invoke the kernel build system.
else

	KERNELDIR ?= /usr/src/linux-2.6.38.6-26.rc1.fc15.i686.PAE
	PWD := $(shell pwd)

default:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) modules

endif
