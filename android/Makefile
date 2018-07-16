all:vncserver vncser

CC := /opt/buildroot-master/output/host/usr/bin/arm-buildroot-linux-gnueabihf-gcc 
CC2 := /opt/buildroot-2018.02.2/output/host/usr/bin/arm-buildroot-linux-gnueabihf-gcc
vncserver:
	$(CC)   fbvncserver.c /opt/buildroot-master/output/host/usr/arm-buildroot-linux-gnueabihf/sysroot/usr/lib/libvncserver.a -static  -lpthread -static  -lresolv -o vncserver
vncser:
	$(CC2)   fbvncserver.c /opt/buildroot-2018.02.2/output/host/usr/arm-buildroot-linux-gnueabihf/sysroot/usr/lib/libvncserver.a -static  -lpthread -static  -lresolv -lz -o $@
pc:
	gcc fbvncserver.c -I ../libvncserver-0.9.11 ../libvncserver-0.9.11/libvncserver/.libs/libvncserver.a -l pthread -lresolv 
.PHONY:clean
clean:
	-@rm *.out vncserver vncser -f
