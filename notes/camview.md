# Adding a camera view to linuxcnc

Roughly followed this guide: http://wiki.linuxcnc.org/cgi-bin/wiki.pl?Axis_Embed_Video

## steps:

Installed `camview-emc` from http://psha.org.ru/debian/README.html:

```
echo 'deb http://psha.org.ru/debian/ lucid contrib' >> /etc/apt/sources.list
wget -O- http://psha.org.ru/debian/pubkey.gpg | sudo apt-key add -

apt-get update && apt-get upgrade
apt-get install camview-emc
```

edit my ini file `3040t.ini`, add this to the `[DISPLAY]`-section:

```
EMBED_TAB_NAME = camera
EMBED_TAB_COMMAND = camview-emc -C camview.conf -w {XID}
```

`camview.conf` can be found in `configs/3040t/`
