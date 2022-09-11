# install-pi-hole


This tutorial assumes you have already have proxmox installed and are ready to spin up some machines.
Stuff to download:
Proxmox (if you haven't already): https://www.proxmox.com/
Debian: https://www.debian.org/

First, install debian or your linux distro of choice.
Once you reach the command line...
Install Sudo
- apt install sudo

- give "yourself" sudo permissions
- usermod -aG sudo "yourusername"

Then change your dhcp to static
navigate up:
cd ..
then we need to use nano to edit a file:
- nano etc/network/interfaces
- Change DHCP to static (see the video)

- Follow the video to install pihole

- https://youtu.be/ov8vb2nztmE


```
after finish set the ip manually
```
# server specifications
```
 CPU  1 CPU(s)
 Memory usage  1024 MiB
 Bootdisk size 4.00 GiB
 ```
# Edit /etc/network/interfaces
```
# the primary network interface
auto ens18
allow-hotplug ens18
address 'ip a 'set ip the ens18''
netmask 255.255.255.0
dns-nameservers 8.8.8.8
gateway xxx.xxx.xxx.xxx
```
