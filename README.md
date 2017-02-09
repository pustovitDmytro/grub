#grub

to save changes run
	sudo update-grub


etc/default/grub:
#default menu item (starts from 0)
GRUB_DEFAULT=2
#time before the default variant will boot
GRUB_TIMEOUT=6
#full path to grub theme
GRUB_THEME=/boot/grub/theme/theme.txt


/etc/grub.d/40_custom:
#!/bin/sh
exec tail -n +3 $0
# This file provides an easy way to add custom menu entries.  Simply type the
# menu entries you want to add after this comment.  Be careful not to change
# the 'exec tail' line above.

menuentry "Shutdown"{
	halt
}

menuentry "Reboot"{
	reboot
}
