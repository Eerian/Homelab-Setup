# Homelab Setup

## Overview
This repository documents the setup of my IT homelab, which I built to simulate a corporate IT environment. 
The goal of this project is to showcase my hands-on experience with virtualization, networking, and system administration using technologies such as VMware, Windows Server, Linux, and more.

In this homelab, I will:
- Set up virtual machines (Windows and Linux) using VMware.
- Configure Windows Server and Active Directory.
- Practice IT infrastructure tasks like user management, networking, and security.
- Document the challenges faced and solutions implemented.

## Hardware and Software Used

- **Host Machine**: 
  - CPU: Ryzen 5 2600 6-core
  - RAM: 32GB DDR4
  - GPU NVIDIA GeForce GTX 1650 Super
  - Hypervisor: VMware and Proxmox
  - OS: Windows 11

- **Network Equipment**:
  - Ubiquiti Dream Router (Home Network)
  - Mikrotik Router (for advanced networking configurations)

- **Operating Systems**:
  - Windows Server 2019
  - Windows 10
  - Ubuntu 20.04

## Project Goals

1. **Virtualization Setup**:
   - Install and configure VMware Workstation to host multiple VMs.
   - Set up Windows Server and client machines (Windows/Linux).

2. **Active Directory (AD) Setup**:
   - Install and configure Active Directory on Windows Server.
   - Create and manage users, groups, and organizational units (OUs).
   - Practice group policy management (GPOs).

3. **Networking**:
   - Configure basic networking between the VMs and physical devices.
   - Set up DNS and DHCP services on Windows Server.
   - Explore VLANs and advanced networking using the Mikrotik router.

4. **IT Administrative Tasks**:
   - Simulate common IT tasks such as user management, file sharing, and permissions.
   - Set up remote desktop access to manage the environment.


This setup serves as a learning tool and a demonstration of my technical skills.

# Virtualization Setup

- Installed VMware as the main hypervisor on the host machine (Windows 11) custom built PC.
- Created multiple VMs for different purposes, including:
  - **Windows Server 2019**: Acts as the primary domain controller for Active Directory.
  - **Windows 10 Help Desk**: Admin machine to join the AD domain to act as help desk.
  - **Multiple Windows 10 non admin user machines**: User machines to join the AD domain (homelab.org.

# Active Directory (AD) Setup

- Installed **Windows Server 2019** and promoted it to a **Domain Controller (DC)**.
- Configured **Active Directory Domain Services (AD DS)**:
  - Set up the **domain**: `mydomain.org`.
  - Created **organizational units (OUs)** to simulate a corporate environment:
    - **Employees**
    - **IT Department**
    - **Sales Department**
  - Managed **user accounts** and **security groups**:
    - Created sample users like `John Snow`, `Sansa Stark`, and assigned them to the appropriate departments.
    - Managed **password policies** and **user access permissions**.
- Configured **Group Policy Objects (GPOs)** to enforce security and administrative policies:
  - Mapped network drives.
  - Deployed software.
  - Configured security policies like account lockout thresholds.
