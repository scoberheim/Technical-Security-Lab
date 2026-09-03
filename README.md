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

Interface ➡️  Purpose\
vmbr1     ➡️ WAN bridge connected to ISP router/modem\
vmbr0  	  ➡️ Internal LAN bridge connected to OPNsense LAN interface\

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

# Network-Diagram
This diagram illustrates the architecture of my cybersecurity homelab, built using Proxmox VE and OPNsense. The environment is designed to provide hands-on experience with network security, system administration, virtualization, and security operations concepts.
Internet connectivity is provided through an OPNsense virtual firewall, with separate WAN (vmbr1) and LAN (vmbr0) bridges configured within Proxmox. The primary LAN provides connectivity to physical devices and wireless clients, while an isolated Cyber Lab network (VLAN 30) hosts security testing systems including Kali Linux, Windows 11 and Ubuntu virtual machines.

Network segmentation and firewall policies are used to control traffic between environments, allowing safe experimentation with security tools and techniques while protecting the primary network. This lab serves as a platform for developing practical skills in firewall administration, network architecture, vulnerability assessment, incident investigation, and Microsoft security technologies.


<img width="641" height="501" alt="Network Diagram drawio" src="https://github.com/user-attachments/assets/2bbe3e9d-68f4-4414-9042-1fc7a46794da" />


