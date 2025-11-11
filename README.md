# 🧩 VirtualBox Setup – Enterprise Virtualization Lab

![GitHub Repo Size](https://img.shields.io/github/repo-size/abdulyusuf-it/virtualbox-setup?color=blue)  
![License](https://img.shields.io/badge/license-MIT-green)  
![Status](https://img.shields.io/badge/status-Complete-brightgreen)

A hands-on project that documents the full process of installing and configuring **Oracle VirtualBox** for enterprise-style IT labs.  
This setup prepares a clean virtualization environment for creating and running **Windows 11 virtual machines** — complete with CPU, RAM, disk, EFI, and dual-network (NAT + Internal) configurations.

---

## 🧠 Project Overview

The goal of this project is to establish a stable, professional-grade virtualization platform suitable for:
- **IT support**, **system administration**, and **cybersecurity** labs  
- Simulating **enterprise network environments** safely  
- Building a foundation for the next step — **Windows 11 client installation** and **Active Directory deployment**

---

## 🧰 Tools & System Requirements

| Component | Details |
|------------|----------|
| **Host OS** | Windows 10 / 11 (x64) |
| **Virtualization Platform** | Oracle VirtualBox 7.x |
| **Guest OS (ISO)** | Windows 11 Pro x64 |
| **Memory (RAM)** | 4 GB |
| **CPU** | 2 vCPUs |
| **Disk Space** | 60 GB |
| **Network Modes** | NAT + Internal (`InternalLabNet`) |
| **Features** | EFI Boot • Bidirectional Clipboard • Drag and Drop |

---

## 🪜 Configuration Steps

### Step 1 — Install Oracle VirtualBox
Download and install **Oracle VirtualBox 7.2.4** on your host system.  
This is the hypervisor that enables multiple isolated operating systems.

![VirtualBox Installed](./Screenshots/virtualbox_installed.png)

---

### Step 2 — Create a New Virtual Machine
Launch VirtualBox and click **New**.  
Enter the VM name `ABDUL-WIN11-CL01`, select **Windows 11 (64-bit)**, and attach your Windows 11 ISO.

![VM Creation](./Screenshots/new_vm_name_iso.png)

---

### Step 3 — Configure Virtual Hardware
Assign **4 GB RAM**, **2 CPUs**, and a **60 GB virtual hard disk**.  
Enable **EFI** for Secure Boot and modern firmware compatibility.

![VM Hardware](./Screenshots/vm_hardware.png)

---

### Step 4 — Review VM Summary
Confirm that CPU, RAM, EFI, and ISO settings are correct before finalizing.  
This prevents boot or driver issues during installation.

![VM Summary](./Screenshots/vm_summary.png)

---

### Step 5 — Enable Shared Features
Under **General → Advanced**, enable the following:
- **Shared Clipboard:** Bidirectional  
- **Drag and Drop:** Bidirectional  

These options simplify text and file transfers between host ↔ guest.

![Shared Features](./Screenshots/general_bidirectional.png)

---

### Step 6 — Configure Network Adapters
- **Adapter 1 (NAT):** Provides external internet access  
  ![Network NAT](./Screenshots/network_nat.png)

- **Adapter 2 (Internal Network):** Connects lab VMs in a private subnet  
  ![Network Internal](./Screenshots/network_internal.png)

---

### Step 7 — Verify Storage and ISO
Check under **Storage** that the Windows 11 ISO is properly attached as a virtual optical disk.

![Storage ISO](./Screenshots/storage_iso.png)

---

### Step 8 — Final Review
Do a complete final review to confirm:
- Hardware = Correct (RAM, CPU, Disk)  
- Networking = Set (NAT + Internal)  
- ISO = Attached  
- EFI = Enabled  

Once validated, the VM is ready to boot.

![VM Details](./Screenshots/vm_details.png)

---

## 🚀 Next Steps

✅ Proceed to the next phase: [**Windows 11 Installation Lab →**](https://github.com/abdulyusuf-it/windows11-installation)  
This continuation covers partitioning, user setup, and post-installation configuration within the VM.

---

## 💡 Project Purpose

This lab establishes a consistent and reusable virtual environment for:
- Practicing **Windows system configuration**  
- Building **Active Directory + Domain Controller** environments  
- Testing **Group Policy, PowerShell, and security policies** in isolation  

---

## 📜 License
This project is licensed under the [MIT License](./LICENSE).

---

### ⭐ If you found this useful
Please consider **starring 🌟 this repository** — it helps others find and learn from your setup.
