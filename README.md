# Technical-Security-Lab

# proxmox-setup

**Hardware**

5th gen i5 processor\
16gb RAM\
Intel I350-T4\
Realtek RTL8111\
256gb SSD

**Installation**

Proxmox has been installed as a type 1 hypervisor. This was done by creating a bootable usb drive with Rufus and a Proxmox iso. A type 1 hypersvisor could have been used, however, bare metal gives a more streamlined, dedicated server experience.

Network Configuration

Physical Network Interfaces  

Interface  	Purpose\
vmbr1 WAN bridge connected to ISP router/modem\
vmbr0  	Internal LAN bridge connected to OPNsense LAN interface

Virtual Networking

The environment uses OPNsense as the virtual firewall and router.

vmbr1 provides Internet connectivity to the OPNsense WAN interface.\
vmbr0 provides internal LAN connectivity for virtual machines and the primary network.\
VLAN 30 is used as an isolated Cyber Lab network for security testing and experimentation.\
Network segmentation and firewall policies are enforced by OPNsense.

Network Objectives

Separate security testing systems from the primary LAN.\
Provide Internet access to lab environments through OPNsense.\
Simulate enterprise network segmentation and firewall management.\
Storage configuration

**Virtual Machines**

VM	Purpose
Windows Server	AD Lab
Windows 11	Client
Ubuntu	Linux Admin
Kali Linux	Security Testing


