<div align="center">

# Enterprise Management & Automation: WinPE ISO Deployment

[Back to Portfolio](https://github.com/fenndw)

</div>

---

# WinPE ISO Deployment – Custom Windows 11 Imaging Lab

## Overview
This project focuses on creating a functional WinPE ISO using Windows 11 Audit Mode and Sysprep, then deploying that image to bare‑metal virtual machines. The goal was to practice real‑world imaging, build a reusable deployment ISO, and understand how enterprise environments standardize and roll out Windows installations. This ISO was also later reused across multiple lab environments.

---

## Highlights
- Entered Windows 11 Audit Mode to customize and prepare the base image  
- Generalized the system using Sysprep with the `/generalize` and `/oobe` flags  
- Built a WinPE boot environment using DISM  
- Created a reusable deployment ISO  
- Deployed the ISO to virtual machines using VMWare  
- Practiced disk partitioning and imaging workflows with DiskPart  

---

## Technical Breakdown

### **1. Audit Mode Customization**
- Booted into Windows 11 Audit Mode using `Ctrl + Shift + F3`  
- Installed updates, configured settings, and prepared the environment  
- Ensured the system was ready for generalization  

Here is my customized system for reference:
<img width="1105" height="831" alt="image" src="https://github.com/user-attachments/assets/0ffe9890-7763-4c19-93f0-03d96a99f85c" />

Some other updates and making sure all hurdles are dealt with prior to generalization:
<img width="1064" height="808" alt="image" src="https://github.com/user-attachments/assets/8682b9d7-7008-40d4-9167-922e37fe89eb" />

### **2. Sysprep Generalization**
Used Sysprep to prepare the image for deployment:

This removed system‑specific data and reset the machine for first‑boot setup.

### **3. WinPE Environment Creation**
- Used the Windows ADK to build a WinPE environment  
- Mounted the WinPE image using DISM  
- Added necessary tools and scripts  
- Generated a bootable ISO  

### **4. Deployment to Virtual Machines**
- Booted VMWare VMs from the WinPE ISO  
- Used DiskPart to clean, partition, and format the virtual disk  
- Applied the custom image  
- Verified successful boot and configuration

Disk Part in use: 
<img width="975" height="597" alt="image" src="https://github.com/user-attachments/assets/70a692b7-d403-4fef-a03b-5c5f7fdb6df0" />

Boot Manager to boot to my WinPE ISO (EFI VMware Virtual SATA CDROM Drive (1.0) was chosen):
<img width="975" height="729" alt="image" src="https://github.com/user-attachments/assets/f74fea3b-f552-44a0-9842-7c7c3387e17c" />

Diskpart again to format drives properly:
<img width="975" height="651" alt="image" src="https://github.com/user-attachments/assets/3ab5bb40-1c04-46fb-a2d0-ae17bf00fe01" />

Dism to capture the image:
<img width="975" height="154" alt="image" src="https://github.com/user-attachments/assets/a56a0b11-e45f-47d3-bb2c-a1d1e377f76b" />

Image saved successfully! Then was applied to a bare metal machine:
<img width="814" height="238" alt="image" src="https://github.com/user-attachments/assets/3849b3dc-2093-429b-bc4d-9632d9e9e9e5" />

Successfully deployed:
<img width="975" height="733" alt="image" src="https://github.com/user-attachments/assets/e3ac8e66-3536-44a7-9e85-2ff81941482c" />

---

<div align="center">

[Back to Portfolio](https://github.com/fenndw)

</div


