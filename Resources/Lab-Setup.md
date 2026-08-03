# Kali Linux Phishing Investigation Lab Setup

---

## Table of Contents

1. Introduction
2. Lab Objectives
3. System Requirements
4. Software Used
5. Downloading Kali Linux
6. Creating the Virtual Machine
7. Configuring the Virtual Machine
8. Installing Kali Linux
9. First Login
10. Updating Kali Linux
11. Installing Essential Investigation Tools
12. Configuring Git
13. Creating Investigation Workspace
14. Lab Verification
15. Final Environment
16. Conclusion

---

# Introduction

A dedicated forensic workstation was created to investigate phishing emails safely inside an isolated virtual environment.

The lab is designed to simulate the workflow followed by SOC analysts and Digital Forensics & Incident Response (DFIR) professionals while investigating suspicious emails.

The environment is fully separated from the host operating system using Oracle VirtualBox, allowing malware analysis and phishing investigations without affecting the primary machine.

# Lab Objectives

The objective of this lab is to build a complete phishing email investigation environment capable of:

- Email Header Analysis
- IOC Extraction
- Attachment Analysis
- URL Investigation
- Threat Intelligence Lookup
- MITRE ATT&CK Mapping
- Incident Documentation
- Evidence Preservation

# System Requirements

| Component | Specification |
|-----------|---------------|
| Host OS | Windows 11 |
| Processor | Intel i7 |
| RAM | 16 GB |
| Virtualization | Oracle VirtualBox |
| Guest OS | Kali Linux 2026.2 |
| Virtual RAM | 4 GB |
| Virtual CPU | 4 vCPUs |
| Virtual Disk | 60 GB |

# Software Used

| Software | Purpose |
|----------|---------|
| Oracle VirtualBox | Virtualization Platform |
| Kali Linux | Investigation Workstation |
| Git | Version Control |
| Thunderbird | Email Client |
| Wireshark | Network Analysis |
| ripmime | Email Attachment Extraction |
| jq | JSON Parsing |
| curl | HTTP Requests |
| wget | File Download |
| ExifTool | Metadata Analysis |

# Downloading Kali Linux

The official Kali Linux Installer ISO was downloaded from the Kali Linux website.

The installer image provides a complete offline installation while allowing customization of installed packages, making it suitable for a dedicated phishing investigation environment.

Screenshot:

![Downloading Kali](../Screenshots/Lab-Setup/01-download-kali-iso.png)

# Creating the Virtual Machine

A new virtual machine named **Kali-Analyst** was created in Oracle VirtualBox.

The virtual machine was configured to run a 64-bit Linux operating system using the downloaded Kali Linux Installer ISO.

Screenshot:

![Creating VM](../Screenshots/Lab-Setup/03-create-virtual-machine.png)

# Configuring Virtual Hardware

The virtual machine hardware was configured with:

- 4 GB RAM
- 4 Virtual CPUs
- 60 GB Virtual Disk
- VMSVGA Graphics Controller
- 128 MB Video Memory

These settings provide sufficient performance for phishing investigations while maintaining efficient resource usage.

Screenshot:

![Hardware Configuration](../Screenshots/Lab-Setup/04-vm-hardware-settings.png)

# Installing Kali Linux

Kali Linux was installed using the graphical installer.

The default XFCE desktop environment and recommended tools were selected during installation to provide a lightweight yet powerful forensic workstation.

Screenshot:

![Installation](../Screenshots/Lab-Setup/08-kali-installer-menu.png)

# First Login

After the installation completed successfully, the virtual machine booted into the Kali Linux login screen.

A new analyst account was used to access the investigation environment.

Screenshot:

![First Login](../Screenshots/Lab-Setup/11-first-login.png)

# Updating Kali Linux

Immediately after installation, the package repositories were updated using:

```bash
sudo apt update
sudo apt full-upgrade -y

```
# Installing Essential Investigation Tools

The following utilities were installed to support phishing investigations.

- Thunderbird
- Git
- curl
- wget
- jq
- ripmime
- ExifTool
- Wireshark
- Python3
- net-tools
- tree
- zip
- unzip

Screenshot:

![Tools Installation](../Screenshots/Lab-Setup/14-essential-tools-installation.png)

# Configuring Git

Git was configured with the analyst's identity to enable version control and documentation throughout the project.

Commands used:

```bash
git config --global user.name "Abdull Ashthaf CK"
git config --global user.email "ashthaf935@gmail.com"

```
# Creating Investigation Workspace

A structured CyberLab directory was created to organize evidence, indicators of compromise (IOCs), reports, scripts, resources, and forensic tools.

Directory Structure:

```text
CyberLab/
├── Cases
├── Evidence
├── IOCs
├── Reports
├── Scripts
├── Resources
└── Tools

```
# Lab Verification

The environment was successfully verified.

| Verification | Status |
|--------------|--------|
| Kali Installed | ✅ |
| Internet Working | ✅ |
| Git Configured | ✅ |
| Investigation Tools Installed | ✅ |
| CyberLab Created | ✅ |
| Ready for Investigation | ✅ |

# Conclusion

A dedicated phishing email investigation workstation has been successfully deployed and configured.

The environment now provides all essential tools required to perform email header analysis, IOC extraction, attachment analysis, threat intelligence lookups, and professional incident reporting.

The lab is now ready for Case-001 phishing email investigation.



