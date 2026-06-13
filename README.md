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
git clone https://github.com/NopeVfx/Everforest-Plymouth.git
cd Everforest-Plymouth
sudo ./install.sh install
# then rebuild your initramfs (e.g. `sudo mkinitcpio -P` on Arch)
```

`install.sh install` copies the theme to `/usr/share/plymouth/themes/everforest-arch`
and sets it as the default. The theme name is **`everforest-arch`**, so you can also
enable it manually at any time with:
```bash
sudo plymouth-set-default-theme -R everforest-arch
```

You can remove theme if you didnt deleted cloned repo folder.
Go to the repo directory and run:
```bash
sudo ./install remove
```

# Boot too fast to see the animation?

On fast machines (NVMe + quick userspace) the system can finish booting before
the splash gets to play, so Plymouth is torn down almost immediately. The
included `plymouth-hold.service` fixes this by keeping the splash on screen for a
fixed number of seconds before the display manager takes over.

Install and enable it:
```bash
sudo cp plymouth-hold.service /etc/systemd/system/
sudo systemctl daemon-reload
sudo systemctl enable plymouth-hold.service
```

Adjust the delay by editing the `ExecStart=/usr/bin/sleep 5` line (seconds). The
animation itself is roughly 2s (slider) + 1s (end glow); `5` adds a little
headroom. Higher = splash lingers longer, lower = faster boot.

Disable it again with:
```bash
sudo systemctl disable plymouth-hold.service
```

# Screenshots

![](./screenshots/image1.png)
![](./screenshots/image2.png)
![](./screenshots/image3.png)
![](./screenshots/image4.png)
