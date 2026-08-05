# 02 - Header Analysis

## Objective

Extract and preserve the complete email header for forensic analysis.

## Method

The complete email header was extracted from the working copy using:

```bash
sed '/^$/q' sample-7918.eml
```

## Results

- Header extracted successfully
- File saved as:
  Analysis/02-Email-Headers.txt

- Total Header Lines:
  195

- Status:
  Complete
