all:vncserver

CC := /opt/buildroot-master/output/host/usr/bin/arm-buildroot-linux-gnueabihf-gcc 

vncserver:
	$(CC)   fbvncserver.c /opt/buildroot-master/output/host/usr/arm-buildroot-linux-gnueabihf/sysroot/usr/lib/libvncserver.a -static  -lpthread -static  -lresolv -o vncserver

.PHONY:clean
clean:
	-@rm *.out vncserver -f
