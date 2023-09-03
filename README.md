# arch-grub-renamer


The bash script renames grub kernel labels according to pacman installed package version (pacman -Q --info linux | grep version).

Usage: grubnamer <grub.cfg file>

If the file is "/boot/grub/grub.cfg" the script will generate the file first (by initiating: grub-mkconfig -o /boot/grub/grub.cfg). That way it is convenient to run it after any change in "/etc/default/grub" or kernel package update.

It is recommended to set the flag "GRUB_DISABLE_SUBMENU=y" (/etc/default/grub) so all kernels will be visible without the need to access the submenu.
