# Manjaro-bootsplash-maia

Kernel Bootsplash theme for manjaro Linux using Manjaro logo and a custom spinner with maia colors.

This project was based on multiple other great projects like:

https://github.com/Blacksuan19/Bootsplash-Themes
https://github.com/GrayJack/manjaro-grayjack/tree/master/PKGBUILDs/manjaro-bootsplash-green

The spinner base gif was created using Preloaders.net and heavily modified afterwards

# Installation:

- `git clone https://github.com/tchavei/bootsplash-manjaro-maia.git`
- `cd manjaro-bootsplash-maia`
- run `bootsplash-manjaro-maia.sh` to generate STL model.
- run `makepkg -s` to create Arch package and install it with `pacman -U bootsplash-theme-manjaro-maia`
- append `bootsplash-manjaro-maia` hook in the end of HOOKS string of `/etc/mkinitcpio.conf`
- add `bootsplash.bootfile=bootsplash-themes/manjaro-maia/bootsplash` into `GRUB_CMDLINE_LINUX` string in `/etc/default/grub`
- run `sudo mkinitcpio -p linux420` or ( `sudo mkinitcpio -P` for all presets)
- run `sudo update-grub`