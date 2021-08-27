# XFCE4-GoboLinux-Future

## Thunar Plugins
https://docs.xfce.org/xfce/thunar/archive  
https://archive.xfce.org/src/thunar-plugins/  

## Desktop and Thunar
Trash icon is missing.
Maybe Installing gvfs would resolve this.
```
Compile DBus-GLib
Compile GVFS
```
Compiled without automatic dependencies resolvance.  
https://github.com/gobolinux/Recipes/blob/effe66610cad8f33b66634a9e3656a278a567e0b/GVFS/1.0.2/Resources/Dependencies#L4


## TODO
~~Update information in the XFCE-Meta-Stable Recipe with comments on the includes=()~~ Done  
~~Replace mv with tar -C in the installation script for GoboLinux 17 Live CD~~ Done  
Remember to compile and install libinput for better hardware support such as mouse.  
Remember to install package to restore default XFCE hicons and a cursor. 
