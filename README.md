# Virtual-Cybersecurity-Lab-NETWORKWALKS-B083-WK2

Configured and maintained a VirtualBox and Kali Linux lab environment for penetration testing, 
vulnerability assessments, and hands-on cybersecurity training.

# Project Overview
This project involves setting up a virtualised cybersecurity testing environment using VirtualBox and Kali Linux to perform penetration testing, 
vulnerability assessments, and security analysis.

# Project Objectives
- Install and configure Android, Windows 10 and Windows Server 2019 virtual machines within the VirtualBox environment.
- Assign and verify static IP addresses on the Windows 10, Android and Windows Server 2019 virtual machines.
- Test network connectivity and DNS resolution between the virtual machines and external networks.
- Create VM snapshots to preserve system configurations and enable quick restoration when required.
- Install and configure Zenmap on the Windows 10 virtual machine for network discovery and scanning activities.
- Perform network footprinting and reconnaissance of the live website networkwalks.com using six built-in Kali Linux information-gathering tools.
# Purpose of Lab

This lab is designed to conduct information gathering and reconnaissance on the live website networkwalks.com 
using six built-in Kali Linux tools: WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, and DNSRecon. 
Each tool provides unique insights into the target's infrastructure, including domain registration details, web technologies, 
DNS configuration, server information, and potential security controls. By combining the results from these tools, 
a foundational security profile of the target can be established.

The information collected during this exercise will support subsequent activities, including network scanning, 
vulnerability assessment, security analysis, and report preparation. 

Important: This laboratory environment is intended solely for educational purposes and for testing systems that you own or 
have explicit authorisation to assess. Always obtain proper permission before conducting any reconnaissance, scanning, 
or security testing activities. Unauthorised testing of systems may violate organisational policies, 
terms of service, or applicable laws.

# Lab Setup Procedure
Install Windows 10

The Windows 10 virtual machine was downloaded and installed in VirtualBox.
The VM network adapter was configured as follows:
Adapter 1

Attached to: NAT Network
Network: NatNetwork
The VM was allocated 4096 MB RAM.
![image.alt]https://github.com/Eneya-Banda/networkwalks-cybersecurity-lab-setup-wk2-/blob/main/Windows%2010%20Install.png

# Configure the Windows 10 Network
The Windows 10 network configuration was checked and configured with a static IPv4 address.
![image.alt]https://github.com/Eneya-Banda/networkwalks-cybersecurity-lab-setup-wk2-/blob/main/Windows%2010_IP.png

# Create a Clean VM Snapshot
Upon completion of the initial system configuration, a VirtualBox snapshot was taken to preserve the current state of the virtual machines and provide a reliable backup for future restoration.

# Android Virtual Machine Installation and Network Configuration
The Android virtual machine (VM) was successfully downloaded and installed within the VirtualBox environment. After installation, the VM's network settings were configured to enable connectivity through a NAT network.

Network Adapter Configuration
Adapter 1
Attached to: NAT Network
Network: NatNetwork

This configuration allows the Android virtual machine to communicate with other virtual machines connected to the same NAT network while maintaining access to external network resources through VirtualBox's network address translation (NAT) service.

