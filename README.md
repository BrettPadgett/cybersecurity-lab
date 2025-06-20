# cybersecurity-lab

# 🛡️ Kali Linux Cybersecurity Lab

A personal virtual lab environment built using Kali Linux on VirtualBox for deeper understanding of Kali Linux, cybersecurity, and information security operations. 

## 🔍 Purpose

This project is designed to simulate real-world cybersecurity scenarios in a safe, isolated environment. It allows me to practice offensive security techniques, test tools, and build hands-on experience with a Linux-based system.

## 🖥️ Environment Overview

- **Host OS**: Windows 11 (HP Pavilion Aero 13)
- **Virtualization**: VirtualBox
- **Guest OS**: Kali Linux (latest ISO)
- **Networking**: Bridged + Host-only adapters for internal and external simulation
- **Optional Tools**: Docker, WSL2, Metasploitable2, OWASP Juice Shop

## ⚙️ Setup Instructions

1. **Download Kali ISO**  
   [Get Kali Linux](https://www.kali.org/get-kali/) I downloaded the recommended Installer Image to base my VM on. 

2. **Create VM in VirtualBox**  
   - Type: Linux (Debian 64-bit)  
   - RAM: 4–8 GB  
   - Disk: 40+ GB (VDI, dynamically allocated)  
   - Enable EFI, 2+ CPUs, 128MB video memory

3. **Install Kali Linux**  
   - Use Graphical Installer  
   - Create non-root user  
   - Guided partitioning  
   - Install GRUB bootloader

4. **Post-Install Setup**  
   ```bash
   #Most tools come with the Kali Installer Image
   sudo apt update && sudo apt upgrade -y
   sudo apt install nmap wireshark hydra john sqlmap nikto gobuster -y 
