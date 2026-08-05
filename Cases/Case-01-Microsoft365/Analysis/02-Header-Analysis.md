# 02 - Header Analysis

## Objective

Extract and preserve the complete email header for forensic analysis.

## Method

The complete email header was extracted from the working copy using:

```bash
sed '/^$/q' sample-7918.eml
