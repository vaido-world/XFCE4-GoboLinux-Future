## Development notes
https://archive.xfce.org/src/apps/xfce4-terminal/0.6/

It seems that xfce4-terminal-0.6.92.tar.bz2  is the latest version before XFCE 4.14 release

It seems it requires dependency of vte-2.91


> Xfce Terminal is based on the VTE Terminal Widget Library, just like gnome-terminal. Vte is probably not the fastest terminal emulation library on earth, but it's one of the best when it comes to Unicode support, and not to forget, it's actively developed. 


```
MakeRecipe XFCE4-Terminal 0.6.92 https://archive.xfce.org/src/apps/xfce4-terminal/0.6/xfce4-terminal-0.6.92.tar.bz2
Compile XFCE4-Terminal
CreatePackage XFCE4-Terminal
```

## For users
`InstallPackage XFCE4-Terminal 0.6.92`
