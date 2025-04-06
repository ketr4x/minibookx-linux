# How to install EndeavourOS on CHUWI MiniBook X
## Requirements
- Chuwi MiniBook X
- A flash drive (=> 8GB)

## Preparing the flashdrive
#### Install balenaEtcher
[Windows/MacOS](https://etcher.balena.io/#download-etcher) Linux: `yay etcher`
#### Download the EndeavourOS image
https://endeavouros.com/
#### Flash the image onto the flashdrive
- Open balenaEtcher
- Choose the image and the drive
- Click flash

**Your flash drive is ready**

## Installing EndeavouOS
1. Connect the drive to the MiniBook X
2. Open the BIOS using ESC/DEL/F2
3. Boot using the flash drive
4. Start the installer
5. Install GRUB
6. Configure the installation (region, language, username and password)
7. Choose Gnome
8. Use the pre-defined partitioning with swap and hibernate
9. Hit Install.

The laptop should reboot into EndeavourOS

## Configuring the device
### Setting up the kernel parameters
- Open the Terminal
- Paste this code: `sudo vim /etc/default/grub`
- Type i, then in ??Params?? add this `??TODO (copy params)??`
- Click ESC -> :x
- Type `sudo grub2-mkconfig -o /boot/grub/grub.cfg`

### Downloading the scripts
- [Download the entire repo](https://github.com/ketr4x/minibookx-linux/archive/refs/heads/main.zip)
- Go into terminal and paste this: `cp -d ~/Downloads/minibookx-linux-main.zip/scripts/.config ~/.config`
- Go into Settings -> Keyboard -> Shortcuts -> Custom Shortcuts
- Add an entry for Scaling Toggle: 

        Title: Scaling Toggle 
        Command: bash 
        Shortcut: Put anything you want - Example: Alt+R

### Configuring autorotation
- Open the Terminal
- Type `yay -S minibook-support-git`

    **Big thanks to [petitstrawberry](https://github.com/petitstrawberry) for this driver! [Source](https://github.com/petitstrawberry/minibook-support)**