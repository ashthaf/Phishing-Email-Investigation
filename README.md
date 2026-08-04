# 📧 Phishing Email Investigation & Incident Response Lab

> A hands-on Digital Forensics and Incident Response (DFIR) project focused on investigating real-world phishing emails using industry-standard tools and methodologies.

---

## 📖 Project Overview

Phishing remains one of the most common initial access techniques used by cybercriminals to steal credentials, distribute malware, and compromise organizations. Security analysts must be able to safely analyze suspicious emails, identify Indicators of Compromise (IOCs), validate findings using threat intelligence, and document incidents in a structured and repeatable manner.

This repository documents the creation of a dedicated phishing investigation laboratory and demonstrates complete end-to-end phishing email investigations performed inside an isolated Kali Linux virtual machine.

The project follows a methodology similar to the workflow used by Security Operations Center (SOC) analysts and Digital Forensics & Incident Response (DFIR) teams.

---

## 🎯 Project Objectives

This project was created to:

- Build a dedicated phishing email investigation laboratory.
- Analyze phishing emails in an isolated environment.
- Preserve digital evidence using forensic best practices.
- Perform email header analysis.
- Extract Indicators of Compromise (IOCs).
- Investigate malicious URLs and attachments.
- Validate findings using threat intelligence platforms.
- Map attacker techniques to the MITRE ATT&CK Framework.
- Produce professional incident reports.
- Document every investigation for learning and portfolio purposes.

---

## ✨ Project Features

✔ Dedicated Kali Linux Investigation Lab

✔ Complete Lab Documentation

✔ Phishing Email Analysis

✔ Email Header Investigation

✔ URL & Attachment Analysis

✔ IOC Extraction

✔ Threat Intelligence Validation

✔ MITRE ATT&CK Mapping

✔ Incident Response Documentation

✔ Reusable Investigation Templates

✔ Python Automation Scripts *(Coming Soon)*

✔ Multiple Real-World Investigation Cases *(Coming Soon)*

---

## 🧰 Tools & Technologies

| Category | Tools |
|----------|------|
| Operating System | Kali Linux |
| Virtualization | Oracle VirtualBox |
| Email Analysis | Thunderbird |
| Network Analysis | Wireshark |
| Attachment Extraction | ripMIME |
| Metadata Analysis | ExifTool |
| Version Control | Git & GitHub |
| Automation | Python 3 |
| Command Line Utilities | curl, wget, jq, tree, zip, unzip |

---

## 📂 Repository Structure

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

## 🏗️ Laboratory Architecture

```
                   Windows 11 Host
                          │
                          │
                  Oracle VirtualBox
                          │
                          ▼
         +----------------------------------+
         |     Kali Linux Investigation VM  |
         |----------------------------------|
         | Thunderbird                      |
         | Wireshark                        |
         | ripMIME                          |
         | ExifTool                         |
         | Git                              |
         | Python                           |
         | CyberLab Workspace               |
         +----------------------------------+
```

---

## 📚 Documentation

| Document | Description |
|----------|-------------|
| Lab-Setup.md | Complete laboratory setup guide |
| Case Reports | Individual phishing investigations |
| Templates | Investigation templates and reporting formats |

## 🔄 Investigation Workflow

Every phishing email investigation performed in this repository follows a structured workflow based on common Security Operations Center (SOC) and Digital Forensics & Incident Response (DFIR) methodologies.

```text
Receive Suspicious Email
            │
            ▼
Evidence Preservation
            │
            ▼
Email Header Analysis
            │
            ▼
Authentication Validation
(SPF • DKIM • DMARC)
            │
            ▼
URL Extraction
            │
            ▼
Attachment Extraction
            │
            ▼
Metadata Analysis
            │
            ▼
Hash Generation
(MD5 • SHA1 • SHA256)
            │
            ▼
Threat Intelligence
(VirusTotal • WHOIS • DNS)
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

# 🔬 Investigation Methodology

Each investigation is performed using a repeatable methodology designed to preserve evidence and maintain investigation integrity.

### Phase 1 – Evidence Collection

- Preserve the original email.
- Record timestamps.
- Maintain evidence integrity.
- Avoid modifying the original sample.

---

### Phase 2 – Email Analysis

- Review email headers.
- Identify sender information.
- Validate SPF.
- Validate DKIM.
- Validate DMARC.
- Review Message-ID.
- Inspect Return-Path.
- Analyze Received headers.

---

### Phase 3 – IOC Extraction

Extract every observable indicator including:

- Domains
- URLs
- Email Addresses
- IP Addresses
- File Names
- Hashes

---

### Phase 4 – Threat Intelligence

Every extracted IOC is validated using trusted intelligence sources.

Examples include:

- VirusTotal
- URLhaus
- WHOIS
- DNS Lookups
- AbuseIPDB (when applicable)

---

### Phase 5 – Reporting

Every investigation concludes with:

- Executive Summary
- Technical Findings
- IOC Table
- Risk Assessment
- MITRE ATT&CK Mapping
- Recommendations

---

# 🛠️ Tools Used During Investigations

| Tool | Purpose |
|------|---------|
| Thunderbird | Email Analysis |
| Wireshark | Network Traffic Analysis |
| ripMIME | Attachment Extraction |
| ExifTool | Metadata Analysis |
| Python | Automation |
| Git | Version Control |
| Kali Linux | Investigation Environment |
| Oracle VirtualBox | Isolated Virtual Machine |

---

# 🧠 Skills Demonstrated

This project demonstrates practical experience with:

- Digital Forensics
- Incident Response
- Phishing Email Analysis
- Email Header Analysis
- IOC Extraction
- Threat Intelligence
- Linux Administration
- Git & GitHub
- Technical Documentation
- Virtual Machine Administration
- Network Analysis
- Cybersecurity Reporting

---

# 📁 Investigation Cases

| Case | Status |
|------|--------|
| Case-001 – Credential Harvesting Email | 🚧 In Progress |
| Case-002 | ⏳ Planned |
| Case-003 | ⏳ Planned |
| Case-004 | ⏳ Planned |
| Case-005 | ⏳ Planned |

---

# 📊 Current Project Progress

| Phase | Status |
|--------|--------|
| Laboratory Setup | ✅ Completed |
| Repository Documentation | ✅ Completed |
| Investigation Templates | 🚧 In Progress |
| Case-001 Investigation | ⏳ Upcoming |
| Python Automation Toolkit | ⏳ Planned |
| Additional Investigation Cases | ⏳ Planned |
| Final Portfolio Polish | ⏳ Planned |

# 🗺️ Project Roadmap

The project is being developed in multiple phases to simulate a real-world phishing investigation workflow.

| Phase | Description | Status |
|--------|-------------|--------|
| Phase 1 | Build Investigation Laboratory | ✅ Completed |
| Phase 2 | Repository Documentation | ✅ Completed |
| Phase 3 | Investigation Templates | 🚧 In Progress |
| Phase 4 | Case-001 Investigation | ⏳ Upcoming |
| Phase 5 | Python Investigation Toolkit | ⏳ Planned |
| Phase 6 | Additional Phishing Cases | ⏳ Planned |
| Phase 7 | Repository Enhancement | ⏳ Planned |

---

# 📅 Future Improvements

This project will continue to evolve with additional features and investigations.

Planned improvements include:

- Multiple real-world phishing investigations
- Python automation toolkit
- IOC extraction automation
- Email header parser
- Automated report generation
- IOC database
- MITRE ATT&CK Navigator mapping
- Detection engineering notes
- Sigma detection rules
- YARA rules (where applicable)
- Splunk detection queries
- Incident response playbooks

---

# 📜 Repository Guidelines

The phishing samples and investigation artifacts included in this repository are intended **solely for cybersecurity education, research, and defensive security purposes**.

The investigations focus on:

- Understanding attacker techniques
- Learning phishing analysis methodologies
- Practicing digital forensics
- Building incident response skills

No malicious content is created or distributed by this project.

---

# 🤝 Contributing

Contributions, suggestions, and constructive feedback are welcome.

If you find inaccuracies or have ideas for improving the investigation methodology or documentation, feel free to open an issue or submit a pull request.

---

# 📄 License

This project is licensed under the **MIT License**.

See the `LICENSE` file for additional information.

---

# 👨‍💻 Author

**Abdull Ashthaf CK**

- Cybersecurity Enthusiast
- Digital Forensics & Incident Response (DFIR)
- Security Operations Center (SOC)
- Ethical Hacking
- Threat Detection & Analysis

---

# ⭐ Acknowledgements

This project was inspired by real-world Security Operations Center (SOC) workflows, Digital Forensics & Incident Response (DFIR) practices, and publicly available phishing research.

Special thanks to the cybersecurity community for providing open educational resources that support hands-on learning and defensive security research.

---

# 🚀 Current Status

```text
█████████████████████████████ 100%  Laboratory Setup

██████████████████████░░░░░░░  70%  Repository Documentation

░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   0%  Investigation Templates

░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   0%  Case-001 Investigation

░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   0%  Python Investigation Toolkit

░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   0%  Additional Investigation Cases
```

---

## 🌟 If you found this repository useful, consider giving it a star.

Every completed investigation will be added to this repository as a new case, demonstrating practical phishing email analysis and incident response techniques using industry-standard methodologies.
