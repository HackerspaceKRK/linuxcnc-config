# Building HeeksCNC on ubuntu 14.04


Follow instructions in
http://code.google.com/p/heekscad/wiki/BuildHeeksCncUnderLinux


Fix error about missing `libheekstinyxml.so.1.0.0`:

`heekscad: error while loading shared libraries: libheekstinyxml.so.1.0.0: cannot open shared object file: No such file or directory`

Add this to your `~/.bashrc` or `/etc/bash.bashrc`:


```
# LD_LIBRARY_PATH for HEEKSCNC
LD_LIBRARY_PATH=/usr/local/lib
export LD_LIBRARY_PATH
```

Fix Postprocessing:
```
sudo ln -s /usr/local/lib/heekscnc /usr/lib/heekscnc
```
