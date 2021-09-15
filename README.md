# XFCE4-GoboLinux-Future
![image](https://user-images.githubusercontent.com/21064622/131251743-094a53be-fdaa-4376-a07d-e062d63cc126.png)

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
'cp' -rf -R /Data/Compile/Sources/dbus-1.12.16/dbus /usr/include/dbus-1.0 
Compile GVFS
```

# Glib

Source Code: https://gitlab.gnome.org/GNOME/glib/-/releases
Latest Stable Release: 2.68.4 

Current error
```
 File "/Programs/Python/3.8.1/lib/python3.8/os.py", line 221, in makedirs
    mkdir(name, mode)
FileNotFoundError: [Errno 2] No such file or directory: '/usr/include/glib-2.0/gobject'
FAILED: meson-install 
/System/Aliens/PIP/3.8/bin/meson install --no-rebuild
ninja: build stopped: subcommand failed.
UnionSandbox: Cleaning up.
UnionSandbox: Moving entries to: /Programs/GLib/2.68.4/.SandboxInstall_Root
Compile: Installation was moved to /Programs/GLib/2.68.4-failed
Compile: GLib 2.68.4 - Installation failed
root@LiveCD ~]

```
## There is probably a missing 
https://packages.debian.org/sid/sh4/libglib2.0-dev/filelist




```
CFLAGS=`pkg-config --cflags glib-2.0`   
LDLIBS=`pkg-config --libs glib-2.0`
```

```
MakeRecipe "GLib" "2.68.4" "https://gitlab.gnome.org/GNOME/glib/-/archive/2.68.4/glib-2.68.4.tar.bz2"
Compile "GLib"
```.

## Compile
```
InstallPackage https://gobolinux.org/packages/017/Fuse--2.9.7--x86_64.tar.bz2
InstallPackage https://gobolinux.org/packages/017/UnionFS-Fuse--2.1--x86_64.tar.bz2
InstallPackage --same "remove" "https://github.com/vaido-world/resolving-util-linux/raw/main/Util-Linux--2.35.1--x86_64.tar.bz2"
Compile glib
CreatePackage GLib
```

## Use 

InstallPackage --same https://github.com/vaido-world/XFCE4-GoboLinux-Future/raw/main/GLib--2.63.5--x86_64.tar.bz2


# Dbus
## Compile

```
Compile dbus
```

## Use
```
InstallPackage
```

# GVfs errors

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
  131 |    _g_dbus_message_iter_append_cstring (&obj_struct_iter, path);
      |    ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
      |    dbus_message_iter_append_basic
gvfsdaemonprotocol.c: In function ‘_g_dbus_get_file_attribute’:
gvfsdaemonprotocol.c:433:8: warning: implicit declaration of function ‘_g_dbus_message_iter_get_args’; did you mean ‘g_dbus_message_get_arg0’? [-Wimplicit-function-declaration]
  433 |    if (_g_dbus_message_iter_get_args (&obj_iter,
      |        ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~
      |        g_dbus_message_get_arg0
gvfsdaemonprotocol.c:447:11: error: ‘G_DBUS_TYPE_CSTRING’ undeclared (first use in this function); did you mean ‘DBUS_TYPE_STRING’?
  447 |           G_DBUS_TYPE_CSTRING, &str,
      |           ^~~~~~~~~~~~~~~~~~~
      |           DBUS_TYPE_STRING
gvfsdaemonprotocol.c:447:11: note: each undeclared identifier is reported only once for each function it appears in
make[2]: *** [Makefile:378: gvfsdaemonprotocol.lo] Error 1
make[2]: Leaving directory '/Data/Compile/Sources/gvfs-1.0.2/common'
make[1]: *** [Makefile:353: all-recursive] Error 1
make[1]: Leaving directory '/Data/Compile/Sources/gvfs-1.0.2'
make: *** [Makefile:283: all] Error 2
Compile: GVFS 1.0.2 - Build process failed.
root@LiveCD ~]

```

```
Compile glib
/usr/lib/dbus-1.0/include: No such file or directory [-Werror=missing-include-dirs]

```



```
Compiled without automatic dependencies resolvance.  (Skip All ) (SA)
https://github.com/gobolinux/Recipes/blob/effe66610cad8f33b66634a9e3656a278a567e0b/GVFS/1.0.2/Resources/Dependencies#L4


## TODO
~~Update information in the XFCE-Meta-Stable Recipe with comments on the includes=()~~ Done  
~~Replace mv with tar -C in the installation script for GoboLinux 17 Live CD~~ Done  
Remember to compile and install libinput for better hardware support such as mouse.  
Remember to install package to restore default XFCE hicons and a cursor. 



![image](https://user-images.githubusercontent.com/21064622/133430490-57e90e89-b989-4d6c-ada9-57a84c6581e4.png)
