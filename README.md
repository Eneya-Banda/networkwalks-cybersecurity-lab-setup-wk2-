# Virtual-Cybersecurity-Lab-NETWORKWALKS-B083-WK2

Configured and maintained a VirtualBox and Kali Linux lab environment for penetration testing, 
vulnerability assessments, and hands-on cybersecurity training.

# Project Overview
This project involves setting up a virtualised cybersecurity testing environment using VirtualBox and Kali Linux to perform penetration testing, vulnerability assessments, and security analysis.

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
![image.alt](https://github.com/Eneya-Banda/networkwalks-cybersecurity-lab-setup-wk2-/blob/main/Windows%2010%20Install.png)

# Configure the Windows 10 Network
The Windows 10 network configuration was checked and configured with a static IPv4 address.
![image.alt](https://github.com/Eneya-Banda/networkwalks-cybersecurity-lab-setup-wk2-/blob/main/Windows%2010_IP.png)

# Create a Clean VM Snapshot
Upon completion of the initial system configuration, a VirtualBox snapshot was taken to preserve the current state of the virtual machines and provide a reliable backup for future restoration.

# Android Virtual Machine Installation and Network Configuration
The Android virtual machine (VM) was successfully downloaded and installed within the VirtualBox environment. After installation, the VM's network settings were configured to enable connectivity through a NAT network.

Network Adapter Configuration
Adapter 1
Attached to: NAT Network
Network: NatNetwork

This configuration allows the Android virtual machine to communicate with other virtual machines connected to the same NAT network while maintaining access to external network resources through VirtualBox's network address translation (NAT) service.
![image.alt](https://github.com/Eneya-Banda/networkwalks-cybersecurity-lab-setup-wk2-/blob/main/Android%20OS.png)

# Configure the Android Network

The Android virtual machine's network settings were reviewed and configured with a static IPv4 address to ensure consistent network communication and reliable connectivity within the virtual lab environment. This configuration enables the device to maintain a fixed address, facilitating network management, testing, and communication with other systems on the virtual network.
![image.alt](https://github.com/Eneya-Banda/networkwalks-cybersecurity-lab-setup-wk2-/blob/main/Android%20Net%20Config.png)

# Creating a VirtualBox Snapshot
Upon completion of the initial system setup and configuration, a VirtualBox snapshot was created to capture the current state of the virtual machine. This snapshot serves as a backup and recovery point, allowing the environment to be restored quickly in the event of configuration errors, system failures, or changes made during subsequent testing activities.

# Problems Encountered
# 1. Virtual Machines not communicating
After assigning static IP addresses to the virtual machines, they were unable to communicate with one another because they were not connected to the configured NAT Network. The NAT Network was also not appearing as an available option in the network settings of the VMs.

To resolve the issue, all virtual machines were powered off, and the following VirtualBox commands were executed from the host machine:

- VBoxManage modifyvm "Windows_10" --nic1 natnetwork
- VBoxManage modifyvm "Windows_10" --nat-network1 NatNetwork

The same configuration was applied to the other virtual machines as required. After running these commands and restarting the VMs, the NAT Network became available in the VirtualBox network settings. The virtual machines were then successfully connected to the NAT Network and were able to communicate with each other using their assigned static IP addresses.

# Screenshots of six Kali Linux tools

# 1. Whois
![image.alt](https://github.com/Eneya-Banda/networkwalks-cybersecurity-lab-setup-wk2-/blob/main/whois.png)

# 2. Whatweb
![image.alt](https://github.com/Eneya-Banda/networkwalks-cybersecurity-lab-setup-wk2-/blob/main/whatweb.png)

# 3. Wafw00f
![image.alt](https://github.com/Eneya-Banda/networkwalks-cybersecurity-lab-setup-wk2-/blob/main/wafw00f.png)

# 4. nslookup
![image.alt](https://github.com/Eneya-Banda/networkwalks-cybersecurity-lab-setup-wk2-/blob/main/nslookup.png)

# 5. curl -I
![image.alt](https://github.com/Eneya-Banda/networkwalks-cybersecurity-lab-setup-wk2-/blob/main/curl.png)

# 6. dnsrecon -d
![image.alt](https://github.com/Eneya-Banda/networkwalks-cybersecurity-lab-setup-wk2-/blob/main/dnsrecon.png)

# 7. nmap -sn
![image.alt](https://github.com/Eneya-Banda/networkwalks-cybersecurity-lab-setup-wk2-/blob/main/nmap%20scan.png)

# 8. Network topology
![image.alt](https://github.com/Eneya-Banda/networkwalks-cybersecurity-lab-setup-wk2-/blob/main/Topology.png)

# What I learned
This lab demonstrated how various built-in Kali Linux reconnaissance tools can be used to collect valuable information about a target system before conducting vulnerability assessments or penetration testing. By using tools such as WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, and DNSRecon, it was possible to gather details about domain ownership, web technologies, DNS records, web server responses, web application firewalls, and network infrastructure.

The exercise highlighted the importance of information gathering as the first phase of a security assessment. Each tool provided a unique perspective on the target, and the combined results helped build a comprehensive profile of the website's environment. The information obtained can be used to support future scanning activities, identify potential attack surfaces, and guide authorised security testing efforts. Proper documentation of all findings is essential, as the collected data forms the basis of the final report and supports subsequent stages of the assessment.

# Tools and Resources
- 7-Zip: https://7-zip.org/download.html
- VirtualBox: https://virtualbox.org/wiki/Downloads
- Kali Linux: https://kali.org/get-kali
- Android: https://www.android-x86.org/download

# Author
Eneya Joseph Banda | Cybersecurity Professional B083 | LinkedIn: https://www.linkedin.com/in/eneya-joseph-banda-78325262/

# Project Information
Program Name: Cybersecurity at Networkwalks | Week: 02 | Project: FOOTPRINTING & RECONNAISSANCE ATTACKS WITH MULTIPLE KALI TOOLS | Repository: GitHub

