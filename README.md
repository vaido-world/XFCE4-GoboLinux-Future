# XFCE4-GoboLinux-Future

## Thunar Plugins
https://docs.xfce.org/xfce/thunar/archive  
https://archive.xfce.org/src/thunar-plugins/  

## Desktop and Thunar
Trash icon is missing.
Maybe Installing gvfs would resolve this.
Maybe PCRE2 is required
```
curl vaido.world/gobo/unionfs.bash | bash
InstallPackage --same "remove" "https://github.com/vaido-world/resolving-util-linux/raw/main/Util-Linux--2.35.1--x86_64.tar.bz2"
Compile DBus-GLib
Compile dbus
cp -rf -R /Data/Compile/Sources/dbus-1.12.16/dbus /usr/include/dbus-1.0
Compile GVFS

```
/Programs/Make/4.3/bin/make  all-recursive
make[1]: Entering directory '/Data/Compile/Sources/dbus-glib-0.110'
Making all in dbus-gmain
make[2]: Entering directory '/Data/Compile/Sources/dbus-glib-0.110/dbus-gmain'
  CC       dbus-gmain.lo
In file included from ../dbus-gmain/dbus-gmain.h:31,
                 from dbus-gmain.c:33:
/usr/include/dbus-1.0/dbus/dbus.h:29:10: fatal error: dbus/dbus-arch-deps.h: No such file or directory
   29 | #include <dbus/dbus-arch-deps.h>
      |          ^~~~~~~~~~~~~~~~~~~~~~~
compilation terminated.
make[2]: *** [Makefile:751: dbus-gmain.lo] Error 1
make[2]: Leaving directory '/Data/Compile/Sources/dbus-glib-0.110/dbus-gmain'
make[1]: *** [Makefile:524: all-recursive] Error 1
make[1]: Leaving directory '/Data/Compile/Sources/dbus-glib-0.110'
make: *** [Makefile:424: all] Error 2
Compile: DBus-GLib 0.110 - Build process failed.

```



```
Compiled without automatic dependencies resolvance.  (Skip All ) (SA)
https://github.com/gobolinux/Recipes/blob/effe66610cad8f33b66634a9e3656a278a567e0b/GVFS/1.0.2/Resources/Dependencies#L4


## TODO
~~Update information in the XFCE-Meta-Stable Recipe with comments on the includes=()~~ Done  
~~Replace mv with tar -C in the installation script for GoboLinux 17 Live CD~~ Done  
Remember to compile and install libinput for better hardware support such as mouse.  
Remember to install package to restore default XFCE hicons and a cursor. 
