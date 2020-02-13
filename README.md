# Bootsplash-theme-alien

Kernel Bootsplash theme for manjaro Linux using Manjaro logo and a custom spinner with maia colors.

This project was based on multiple other great projects like:

https://github.com/Blacksuan19/Bootsplash-Themes

https://github.com/GrayJack/manjaro-grayjack/tree/master/PKGBUILDs/manjaro-bootsplash-green

https://github.com/tchavei/bootsplash-manjaro-maia

The spinner base gif was created using Preloaders.net and heavily modified afterwards.

The `logo.png` is converted from the theme breeze-icon(alienarena.svg).

# Installation:

- `git clone https://github.com/trdmm/bootsplash-theme-alien.git`
- `cd bootsplash-theme-alien`
- run `chmod +x bootsplash-alien.sh`
- run `chmod +x bootsplash-packer`
- run `bootsplash-alien.sh` to generate STL model.
- run `makepkg -s` to create an Arch package and install it with `pacman -U $package_name`or alternatively make and install with one single command: `makepkg -sci`
- append `bootsplash-alien` hook at the end of HOOKS string in `/etc/mkinitcpio.conf`
- add `bootsplash.bootfile=bootsplash-themes/alien/bootsplash` at the end of `GRUB_CMDLINE_LINUX` string in `/etc/default/grub` and don't forget to remove the `quiet` parameter!
- run `sudo mkinitcpio -P`
- run `sudo update-grub`
