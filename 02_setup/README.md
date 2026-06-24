# Setting up VirtualBox and Oracle Linux

<a href="https://youtu.be/eFPF2envNi8" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/setup.png?raw=true" alt="setup oracle linux and virtualbox" width="600">
</a>



## VirtualBox

VirtualBox is a virtualization software that allow you to run multiple operating systems simultaneously on the same physical computer. Download [VirtualBox from here](https://www.virtualbox.org/wiki/Downloads).

## Oracle Linux

Download [Oracle Linux](https://yum.oracle.com/oracle-linux-isos.html#content-2) from here. Choose the newest, version 10.1, as of this writing as this is the most stable one.

If you are on a M1, M2, ... chip Mac, then you need to pick "Oracle Linux Arm (aarch64) ISO", otherwise you should choose "Oracle Linux x86_64 ISO". This is because VirtualBox is not an emulator, so it requires matching CPU architecture between the guest OS (Oracle Linux in this case) and the host system.

Choose full version as it contains everything needed for local installations.

## Setup Oracle Linux on VirtualBox

## New VM

**Create a new VM**

<img src="https://github.com/kokchun/assets/blob/main/linux/new_virtual_machine.png?raw=true" alt="creating new virtual machine" width="600">


**VM size**

Example of VM size, it can probably work with less memory, less CPU cores and less storage, but try to keep to a minimum of 

- memory: 2 CPU cores
- RAM: 6 GB
- 40 GB 

<img src="https://github.com/kokchun/assets/blob/main/linux/vm_size.png?raw=true" alt="setup guest OS" width="600">

These can be scaled up/down after installed

- memory (max half of your computers memory)
- number of CPUs (max half of your computers memory)

Disk size can't be decreased after isntallation, but can grow

> [!NOTE]
> the VM needs to be powered off to scale it

<!-- **setup guest OS**

<img src="https://github.com/kokchun/assets/blob/main/linux/virtual_box_oracle_guest_setup.png?raw=true" alt="setup guest OS" width="600"> -->

Before installation you will see this summary

<img src="https://github.com/kokchun/assets/blob/main/linux/vm_setup_summary.png?raw=true" alt="vm setup summary" width="600">

You can click preview to see the installation going on

## Start VM

Now it's time to start the VM and you will see GRUB - this menu here, now you can install Oracle Linux - I use 10.1.0 here

<img src="https://github.com/kokchun/assets/blob/main/linux/grub.png?raw=true" alt="vm setup summary" width="600">

## Scaled mode

To make the text and window scale -> goto VirtualBox VM and click on View and then "Scaled Mode (Host+C)". Otherwise the text is too small to read.

## Install settings


<img src="https://github.com/kokchun/assets/blob/main/linux/install_settings.png?raw=true" alt="installation settings" width="600">


**choose language**

<img src="https://github.com/kokchun/assets/blob/main/linux/choose_language.png?raw=true" alt="language choice" width="600">


**root account**

- keep it disabled, best practice to use sudo 

**create a user**


**install Oracle Linux**

**login**

Congratulations on coming so far. Now it's time to upgrade all your existing packages on your linux system. Open up a terminal and run 

```bash
sudo dnf upgrade
```

This requires your password and then just click y to accept each installation prompt. 

## Fix screen resolution

- devices -> insert guest additions cd
- go into files and then run software


<!-- ### change keyboard settings

```bash
# syntax
localectl set-keymap <layout-code>

# example swedish
localectl set-keymap se
```
 -->
