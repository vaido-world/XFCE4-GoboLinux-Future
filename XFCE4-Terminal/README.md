## Development notes
https://archive.xfce.org/src/apps/xfce4-terminal/0.6/

It seems that xfce4-terminal-0.6.92.tar.bz2  is the latest version before XFCE 4.14 release

It seems it requires dependency of vte-2.91

> Xfce Terminal is based on the VTE Terminal Widget Library, just like gnome-terminal. Vte is probably not the fastest terminal emulation library on earth, but it's one of the best when it comes to Unicode support, and not to forget, it's actively developed. 

0.57 seems to be the latest version of vte before XFCE 4.14 release.
https://download-fallback.gnome.org/sources/vte/0.57/


```
MakeRecipe VTE 0.57 https://download-fallback.gnome.org/sources/vte/0.57/vte-0.57.90.tar.xz
Compile VTE 0.57
CreatePackage VTE

MakeRecipe XFCE4-Terminal 0.6.92 https://archive.xfce.org/src/apps/xfce4-terminal/0.6/xfce4-terminal-0.6.92.tar.bz2
Compile XFCE4-Terminal
CreatePackage XFCE4-Terminal
```

## For users
`InstallPackage XFCE4-Terminal 0.6.92`
