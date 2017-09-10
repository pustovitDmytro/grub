#grub

custom menu for GRUB4DOS

to save changes run
```sh
sudo update-grub
```

in the file `etc/default/grub`:
```
default menu item (starts from 0)
GRUB_DEFAULT=2
```

set time, after what the default variant will boot:
```
GRUB_TIMEOUT=6
```
set full path to grub theme:
```
GRUB_THEME=/boot/grub/theme/theme.txt
```

in the file `/etc/grub.d/40_custom`:
```
menuentry "Shutdown"{
	halt
}
```
```
menuentry "Reboot"{
	reboot
}
```
