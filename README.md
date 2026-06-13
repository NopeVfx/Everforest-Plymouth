# Arch Slider And Glow — Everforest Dark

A plymouth theme with a Mac OS like slider and a glowing logo at the end of the animation, recolored for [Everforest Dark](https://github.com/sainnhe/everforest).
Licensed under [MIT License](LICENSE)

This is an Everforest-Dark variant of [ArchSliderGlowPlymouth](https://github.com/HasanAgitUnal/ArchSliderGlowPlymouth):
- Arch logo recolored to Everforest green `#a7c080`
- Slider / progress bar highlight recolored from blue to Everforest green `#a7c080`
- Background set to Everforest-Dark gray `#1e2326`

Based on: [www.opendesktop.org/p/2106821/](https://www.opendesktop.org/p/2106821/)

Insipired from: [www.opendesktop.org/p/1000032/](https://www.opendesktop.org/p/1000032/)

# Installation

Install with these commands:
```bash
git clone https://github.com/HasanAgitUnal/ArchSliderGlowPlymouth.git
cd ArchSliderGlowPlymouth
sudo ./install.sh install
# then rebuild your initramfs (e.g. `sudo mkinitcpio -P` on Arch)
```

`install.sh install` copies the theme to `/usr/share/plymouth/themes/arch-slider-and-glow`
and sets it as the default. The theme name is **`arch-slider-and-glow`**, so you can also
enable it manually at any time with:
```bash
sudo plymouth-set-default-theme -R arch-slider-and-glow
```

You can remove theme if you didnt deleted cloned repo folder.
Go to the repo directory and run:
```bash
sudo ./install remove
```

# Screenshots

![](./screenshots/image1.png)
![](./screenshots/image2.png)
![](./screenshots/image3.png)
![](./screenshots/image4.png)
