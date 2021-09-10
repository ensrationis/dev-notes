```console
nano /etc/default/grub
```
``GRUB_CMDLINE_LINUX_DEFAULT="quiet splashs i915.enable_psr=0 i8042.direct i8042.dumbkbd"``
```console
update-grub
```
