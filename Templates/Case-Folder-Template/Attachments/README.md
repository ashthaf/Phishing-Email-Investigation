# Attachments

## Purpose

This directory stores all email attachments collected during the investigation.

Attachments are preserved exactly as received and are never modified.

---

## Possible File Types

- PDF
- DOCX
- XLSX
- PPTX
- ZIP
- ISO
- IMG
- EXE
- DLL
- JS
- VBS
- HTA
- LNK
- BAT
- CMD
- HTML
- EML

---

## Investigation Workflow

When an attachment exists:

1. Preserve the original file.
2. Calculate MD5 and SHA256 hashes.
3. Record file size.
4. Determine MIME type.
5. Identify file extension.
6. Extract metadata.
7. Perform static analysis.
8. If suspicious, execute inside an isolated sandbox.
9. Record all Indicators of Compromise (IOCs).
10. Document findings in the case report.

---

## Typical Tools

- file
- sha256sum
- md5sum
- exiftool
- strings
- oletools
- pdfid
- pefile
- CyberChef
- VirusTotal
- Any.Run
- Hybrid Analysis
- Cuckoo Sandbox

---

## Folder Usage

If multiple attachments exist, preserve them using their original filenames.

Example

```
Invoice.pdf
Payment.docm
Resume.zip
Update.html
```

If attachments are extracted from archives:

```
Invoice.zip
└── Invoice.exe
```

---

## Notes

- Never execute an attachment directly on the analyst workstation.
- Preserve the original evidence.
- Work only on copied samples.
- Record every action in the investigation timeline.
