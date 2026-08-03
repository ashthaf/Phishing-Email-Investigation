# Phishing Investigation Lab Setup

## Overview

This document describes the complete setup process for the phishing email investigation laboratory used throughout this project.

The objective of this lab is to create a dedicated Digital Forensics and Incident Response (DFIR) environment capable of safely analyzing phishing emails, extracting Indicators of Compromise (IOCs), validating threats using threat intelligence platforms, and documenting findings through professional incident reports.

---

# Lab Objectives

The laboratory was configured to provide a safe environment for:

- Email Header Analysis
- IOC Extraction
- URL Investigation
- Attachment Analysis
- Metadata Analysis
- Threat Intelligence Lookups
- MITRE ATT&CK Mapping
- Incident Reporting

---

# Lab Specifications

| Component | Details |
|-----------|---------|
| Operating System | Kali Linux 2026.2 |
| Virtualization | Oracle VirtualBox |
| VM Name | Kali-Analyst |
| Memory | 4096 MB |
| CPUs | 4 |
| Disk | 60 GB VDI |
| Network | NAT |
| Desktop Environment | XFCE |

---

# Investigation Tools

The following tools were installed for phishing investigations.

| Tool | Purpose |
|------|----------|
| Thunderbird | Email Client |
| Git | Version Control |
| curl | Download Files |
| wget | Download Files |
| jq | JSON Parsing |
| ripmime | Email Attachment Extraction |
| ExifTool | Metadata Analysis |
| Wireshark | Packet Analysis |
| Python3 | Automation |
| tree | Directory Visualization |
| zip / unzip | Archive Handling |
| net-tools | Network Utilities |

---

# Downloading Kali Linux

The official Kali Linux installer ISO was downloaded from the Kali Linux website.

This installer provides an offline installation while allowing complete customization of installed packages.

### Kali Linux Download Page

![Downloading Kali](../Screenshots/lab-setup/01-kali-installer-download-page.png)

---

### Kali ISO Successfully Downloaded

The installer ISO was successfully downloaded and stored on the local system before creating the virtual machine.

![ISO Downloaded](../Screenshots/lab-setup/02-kali-iso-downloaded.png)

---

# Creating the Virtual Machine

A new virtual machine named **Kali-Analyst** was created in Oracle VirtualBox.

The downloaded Kali Linux installer ISO was attached as the installation media.

![Creating Virtual Machine](../Screenshots/lab-setup/03-create-vm.png)

---

# Configuring Virtual Hardware

The virtual machine hardware resources were configured before installation.

Configuration:

- Memory: 4096 MB
- CPUs: 4
- Suitable for malware-safe analysis

![Virtual Hardware](../Screenshots/lab-setup/04-virtual-hardware.png)

---

# Configuring Virtual Storage

A dynamically allocated VirtualBox Disk Image (VDI) was created.

Configuration:

- Disk Type: VDI
- Capacity: 60 GB
- Dynamic Allocation Enabled

![Virtual Hard Disk](../Screenshots/lab-setup/05-virtual-harddisk.png)

---

# Summary

At this stage the virtual machine has been successfully created and configured with appropriate hardware resources required for phishing email investigations.

The next section covers VirtualBox configuration and Kali Linux installation.

---

# Configuring Virtual Machine Settings

After creating the virtual machine, several VirtualBox settings were adjusted to optimize performance and provide a stable environment for phishing email investigations.

---

## Motherboard Configuration

The motherboard settings were configured to ensure proper boot order and system stability during installation.

Key configuration:

- Boot Order configured correctly
- EFI disabled
- I/O APIC enabled
- Hardware Clock set to UTC

![Motherboard Settings](../Screenshots/lab-setup/07-system-motherboard.png)

---

## Processor Configuration

The processor allocation was increased to improve overall performance during investigations and while running multiple analysis tools.

Configuration:

- 4 Virtual CPUs
- Execution Cap: 100%
- PAE/NX Enabled

![Processor Settings](../Screenshots/lab-setup/08-system-processor.png)

---

## Display Configuration

Display settings were configured to provide a smooth graphical experience.

Configuration:

- Graphics Controller: VMSVGA
- Video Memory: 128 MB
- 3D Acceleration Enabled

![Display Settings](../Screenshots/lab-setup/09-display-settings.png)

---

## Shared Folder Configuration

Shared folders were configured to simplify the transfer of documentation, screenshots, and investigation reports between the host operating system and the Kali Linux virtual machine.

> **Note:** Shared folders should not be used for storing active phishing samples or malicious files. Investigation evidence should remain inside the isolated virtual machine.

![Shared Folder Configuration](../Screenshots/lab-setup/10-shared-folders.png)

---

## Storage Configuration

The Kali Linux installation ISO was attached to the virtual optical drive before booting the virtual machine.

Storage configuration was verified to ensure the system boots directly into the Kali installer.

![Storage Settings](../Screenshots/lab-setup/11-storage-settings.png)

---

## Network Configuration

The virtual machine was configured to use a NAT network adapter.

This allows the system to access the internet for software updates and threat intelligence lookups while remaining isolated from the host operating system.

Configuration:

- Adapter Type: NAT
- Cable Connected: Enabled

![Network Settings](../Screenshots/lab-setup/12-network-settings.png)

---

## USB Configuration

USB support was intentionally disabled because external removable media is not required for this project.

Disabling unused virtual hardware also reduces unnecessary attack surface.

![USB Configuration](../Screenshots/lab-setup/13-usb-disabled.png)

---

## Final Virtual Machine Review

Before starting the installation, all VirtualBox settings were reviewed to ensure the virtual machine was correctly configured.

The following checklist was verified:

- Virtual Hard Disk Attached
- Kali Installer ISO Attached
- Memory Allocation Verified
- CPU Allocation Verified
- Display Settings Verified
- Network Configuration Verified

![Final VM Configuration](../Screenshots/lab-setup/13-final-vm-configuration.png)

---

# Installing Kali Linux

After verifying the virtual machine configuration, the Kali Linux installation process was started.

The graphical installer was used to simplify the installation and configure the system correctly.

---

## Booting the Installer

The virtual machine successfully booted from the Kali Linux installer ISO.

The graphical installation option was selected.

![Kali Boot Menu](../Screenshots/lab-setup/14-kali-boot-menu.png)

---

## Disk Partitioning

Automatic partitioning was selected to simplify storage management for this dedicated investigation workstation.

The installer automatically created the required Linux partitions.

![Disk Partitioning](../Screenshots/lab-setup/18-partitioning.png)

---

## Software Selection

The default XFCE desktop environment and standard Kali Linux tools were selected.

This provides a lightweight yet powerful operating system suitable for digital forensics and phishing investigations.

![Software Selection](../Screenshots/lab-setup/19-software-selection.png)

---

## Installation Completed

After copying the required files and installing all selected packages, the installation completed successfully.

The system was then prepared for its first reboot.

![Installation Complete](../Screenshots/lab-setup/20-installation-complete.png)

---

# Summary

At this stage:

- Oracle VirtualBox was fully configured.
- Kali Linux was successfully installed.
- The virtual machine was ready for its initial boot and post-installation configuration.

---

# First Login

After the installation completed successfully, the virtual machine rebooted into the Kali Linux login screen.

The analyst account created during installation was used to access the operating system for the first time.

Successful login confirms that the installation completed without errors.

![First Login](../Screenshots/lab-setup/21-first-login.png)

---

# Updating Kali Linux

Before beginning any investigations, the operating system was updated to ensure that all installed packages were running the latest stable versions.

Updating the system also ensures that security patches and bug fixes are applied before handling real phishing samples.

The following command was executed:

```bash
sudo apt update
```

![APT Update](../Screenshots/lab-setup/22-apt-update.png)

---

After updating the package repository, all installed packages were upgraded.

```bash
sudo apt full-upgrade -y
```

This command upgraded all installed software to the latest available versions.

![Full Upgrade](../Screenshots/lab-setup/23-full-upgrade.png)

---

# Installing Essential Investigation Tools

A dedicated phishing investigation workstation requires several utilities for collecting evidence, extracting Indicators of Compromise (IOCs), analysing attachments, inspecting metadata, and documenting findings.

The following command was executed to install the required tools.

```bash
sudo apt install -y \
thunderbird \
wireshark \
ripmime \
jq \
curl \
wget \
python3-pip \
python3-venv \
python3-dev \
libimage-exiftool-perl \
git \
tree \
zip \
unzip \
net-tools
```

The installation completed successfully.

![Essential Tools Installed](../Screenshots/lab-setup/22-essential-tools-installed.png)

---

## Installed Investigation Tools

| Tool | Purpose |
|------|---------|
| Thunderbird | Email Client |
| Wireshark | Network Traffic Analysis |
| ripMIME | Extract MIME Attachments |
| ExifTool | Metadata Analysis |
| curl | Download Files |
| wget | Download Files |
| jq | JSON Parsing |
| Python3 | Automation Scripts |
| Git | Version Control |
| Tree | Directory Visualization |
| zip / unzip | Archive Handling |
| net-tools | Network Utilities |

---

# Git Configuration

Git was configured using the analyst's identity to enable version control and maintain proper commit history throughout the project.

Commands executed:

```bash
git config --global user.name "Abdull Ashthaf CK"

git config --global user.email "ashthaf935@gmail.com"
```

Configuration was verified using:

```bash
git config --list
```

![Git Configuration](../Screenshots/lab-setup/24-git-configured.png)

---

# Creating the CyberLab Workspace

To maintain a structured workflow throughout the investigation process, a dedicated workspace named **CyberLab** was created.

This workspace will store evidence, investigation notes, scripts, reports, extracted indicators, and analysis resources.

The following directory structure was created:

```text
CyberLab/
├── Cases
├── Evidence
├── IOCs
├── Reports
├── Resources
├── Scripts
└── Tools
```

The workspace was verified using:

```bash
tree ~/CyberLab
```

![CyberLab Workspace](../Screenshots/lab-setup/23-cyberlab-workspace.png)

---

# Security Considerations

To minimise the risk of accidental exposure while handling phishing samples, the following precautions were implemented during lab setup:

- Dedicated Kali Linux virtual machine used exclusively for investigations.
- Personal accounts are not used inside the investigation environment.
- Investigation evidence remains inside the virtual machine.
- The operating system is fully updated before analysis begins.
- Version control is used for documentation only.
- Investigation samples will never be executed on the host operating system.

These practices help maintain a safe and repeatable phishing investigation workflow.

---

# Summary

At this stage, the laboratory environment has been successfully prepared.

Completed tasks include:

- Kali Linux installed successfully.
- Virtual machine configured.
- System updated.
- Essential investigation tools installed.
- Git configured.
- CyberLab workspace created.
- Environment verified.

The laboratory is now ready to begin phishing email investigations.

---

# Lab Verification

After completing the installation and configuration process, the laboratory environment was verified to ensure that all required components were functioning correctly.

The following checklist was completed.

| Verification Item | Status |
|-------------------|--------|
| Kali Linux Installed | ✅ Completed |
| Virtual Machine Configured | ✅ Completed |
| Internet Connectivity Verified | ✅ Completed |
| Package Repository Updated | ✅ Completed |
| System Upgraded | ✅ Completed |
| Essential Investigation Tools Installed | ✅ Completed |
| Git Configured | ✅ Completed |
| CyberLab Workspace Created | ✅ Completed |
| Environment Ready for Investigation | ✅ Completed |

---

# Final Laboratory Architecture

The completed phishing investigation laboratory consists of a dedicated Kali Linux virtual machine running inside Oracle VirtualBox.

The workstation has been configured exclusively for phishing email investigations and documentation.

```text
+-----------------------------------------------------------+
|                     Host Operating System                 |
|                     Windows 11                            |
+---------------------------+-------------------------------+
                            |
                            |
                    Oracle VirtualBox
                            |
                            |
+-----------------------------------------------------------+
|                Kali Linux Investigation VM               |
|-----------------------------------------------------------|
|                                                           |
|  Thunderbird          Email Analysis                      |
|  Wireshark            Network Analysis                    |
|  ripMIME              Attachment Extraction               |
|  ExifTool             Metadata Analysis                   |
|  curl / wget          Evidence Collection                 |
|  jq                   JSON Processing                     |
|  Python3              Automation                          |
|  Git                  Documentation                       |
|                                                           |
|  CyberLab Workspace                                       |
|                                                           |
|      Cases                                                |
|      Evidence                                             |
|      IOCs                                                 |
|      Reports                                              |
|      Scripts                                              |
|      Resources                                            |
|      Tools                                                |
|                                                           |
+-----------------------------------------------------------+
```

---

# Investigation Workflow

Every phishing email investigated in this repository will follow the same structured workflow.

```text
Receive Email
      │
      ▼
Preserve Original Evidence
      │
      ▼
Extract Email Headers
      │
      ▼
Header Analysis
      │
      ▼
Extract URLs
      │
      ▼
Extract Attachments
      │
      ▼
Metadata Analysis
      │
      ▼
Hash Calculation
      │
      ▼
Threat Intelligence Lookup
      │
      ▼
IOC Extraction
      │
      ▼
MITRE ATT&CK Mapping
      │
      ▼
Incident Report
```

---

# Investigation Methodology

Every investigation performed in this repository follows the principles of digital forensics.

1. Preserve original evidence.
2. Avoid modifying original files.
3. Perform static analysis before dynamic analysis.
4. Record every observation.
5. Extract all Indicators of Compromise (IOCs).
6. Validate findings using trusted threat intelligence sources.
7. Produce a structured incident report.

This methodology ensures investigations remain repeatable, well-documented, and forensically sound.

---

# Repository Structure

The repository has been organized to separate laboratory documentation, investigation cases, resources, templates, and screenshots.

```text
Phishing-Email-Investigation/
│
├── Assets/
│
├── Cases/
│
├── Resources/
│   └── Lab-Setup.md
│
├── Screenshots/
│   └── lab-setup/
│
├── Templates/
│
├── README.md
│
├── LICENSE
│
└── .gitignore
```

---

# Skills Demonstrated

The laboratory setup demonstrates practical experience with:

- Virtual Machine Deployment
- Linux Administration
- Git Version Control
- Investigation Environment Preparation
- Email Analysis Environment Setup
- Tool Installation and Verification
- Digital Forensics Documentation
- Technical Documentation
- Cybersecurity Lab Design

---

# Next Phase

With the laboratory environment successfully configured, the next phase of the project focuses on practical phishing email investigations.

The first investigation will include:

- Evidence Preservation
- Email Header Analysis
- SPF, DKIM, and DMARC Validation
- URL Extraction
- Attachment Extraction
- IOC Collection
- Threat Intelligence Analysis
- MITRE ATT&CK Mapping
- Professional Incident Reporting

Each investigation will be documented as an independent case inside the `Cases` directory.

---

# Conclusion

A dedicated phishing email investigation laboratory has been successfully designed, deployed, configured, and documented.

The environment provides a safe and structured workspace for analyzing phishing emails, extracting Indicators of Compromise (IOCs), validating malicious artifacts using threat intelligence platforms, and producing professional incident reports.

This laboratory serves as the foundation for all future investigations documented in this repository.

The next step is **Case-001: Phishing Email Investigation**, where the laboratory will be used to perform a complete end-to-end analysis of a real phishing email sample.
