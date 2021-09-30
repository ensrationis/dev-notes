```console
nano /etc/default/grub
```
``GRUB_CMDLINE_LINUX_DEFAULT="quiet splashs i915.enable_psr=0 i8042.direct i8042.dumbkbd"``
```console
update-grub
```
Touchpad

The touchpad is barely usable, only with the "right" pressure. https://gitlab.freedesktop.org/libinput/libinput/-/issues/604.

Luckily, the fix is easy. As mentioned in the bug report, just create file /etc/libinput/local-overrides.quirks with the following content:

[Lenovo Yoga Slim 9 Pressurepad]
MatchBus=i2c
MatchVendor=0x27C6
MatchProduct=0x01E8
AttrEventCodeDisable=ABS_MT_PRESSURE;ABS_PRESSURE;

After that, log out and log in again and the touchpad should work. 

https://wiki.archlinux.org/title/Lenovo_Yoga_Slim_9_(intel)
