# Bootsplash-manjaro-maia

Kernel Bootsplash theme for manjaro Linux using Manjaro logo and a custom spinner with maia colors.

This project was based on multiple other great projects like:

https://github.com/Blacksuan19/Bootsplash-Themes

https://github.com/GrayJack/manjaro-grayjack/tree/master/PKGBUILDs/manjaro-bootsplash-green

The spinner base gif was created using Preloaders.net and heavily modified afterwards

Author: Tony Chaveiro

# Installation:

- `git clone https://github.com/tchavei/bootsplash-manjaro-maia.git`
- `cd bootsplash-manjaro-maia`
- run `chmod +x bootsplash-manjaro-maia.sh`
- run `chmod +x bootsplash-packer`
- run `bootsplash-manjaro-maia.sh` to generate STL model.
- run `makepkg -s` to create an Arch package and install it with `pacman -U $package_name`or alternatively make and install with one single command: `makepkg -sci`
- append `bootsplash-manjaro-maia` hook at the end of HOOKS string in `/etc/mkinitcpio.conf`
- add `bootsplash.bootfile=bootsplash-themes/manjaro-maia/bootsplash` at the end of `GRUB_CMDLINE_LINUX` string in `/etc/default/grub` and don't forget to remove the `quiet` parameter!
- run `sudo mkinitcpio -P`
- run `sudo update-grub`
