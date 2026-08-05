# 02 - Header Analysis

## Objective

Extract and preserve the complete email header for forensic analysis.

## Method

The complete email header was extracted from the working copy using:

```bash
sed '/^$/q' sample-7918.eml
```

---

# Investigation Evidence

## Header Extraction

![Header Extraction](../Screenshots/headerextraction.png)

Email headers were extracted successfully from the original EML file.

---

## Subject Analysis

![Subject Analysis](../Screenshots/subject.png)

The subject line was reviewed for indicators of urgency and impersonation.

---

## MIME Analysis

![Content Type](../Screenshots/contenttype.png)

The MIME Content-Type confirmed the structure of the email.

---

## Extracted Body

![Body Files](../Screenshots/bodyfiles.png)

The extracted email body files were examined for embedded content.

---

## Plain Text Body

![Plain Text](../Screenshots/textfile1.png)

Plain text version of the email.

---

## HTML Body

![HTML Body](../Screenshots/textfile2.png)

HTML version of the phishing email.


## Results

- Header extracted successfully
- File saved as:
  Analysis/02-Email-Headers.txt

- Total Header Lines:
  195

- Status:
  Complete
