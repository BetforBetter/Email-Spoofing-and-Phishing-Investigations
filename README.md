# Email-Spoofing-and-Phishing-Investigation

## Overview

This project demonstrates a comprehensive **email forensic investigation** focused on identifying spoofed and phishing emails through header analysis, email authentication validation, and OSINT techniques.

The investigation analyzes multiple `.eml` files to determine their authenticity by examining email headers, sender infrastructure, routing paths, authentication mechanisms (SPF, DKIM, and DMARC), embedded hyperlinks, and IP reputation.

The project follows standard **Digital Forensics and Incident Response (DFIR)** methodology for analyzing suspicious email communications.

## Scenario

Below there are two different emails sent to actual email address user@cyphoreninja.com. When the recipient checks both emails he sees no difference at the first sight. The task is to analyze headers and bodies of both emails and find out which email is spoofed and what evidence was found through header analysis. Additionally, “I won't be able to make it today.eml” email was also sent from user@cyphoreninja.com to mgunestas@hotmail.coman. The email's content and header needs to be analyzed the to find what is inconsistent.

<br><br>
<img width="628" height="546" alt="Screenshot 2026-07-27 at 1 05 17 PM" src="https://github.com/user-attachments/assets/3dd5910a-eb18-4156-a255-302ee73927d5" />
<br><br>
<img width="632" height="548" alt="image" src="https://github.com/user-attachments/assets/a86e4d48-67f4-475c-b284-8cc9841a7faf" />
<br><br>

## Objectives

- Verify forensic integrity of email evidence
- Analyze raw email headers (.eml)
- Detect email spoofing
- Validate SPF, DKIM, and DMARC authentication
- Perform IP and domain OSINT
- Identify phishing indicators
- Correlate forensic evidence to determine email authenticity

## Tools Used

- Windows Command Prompt
- Notepad
- ViewDNS.info
- SHA-256 Hash Verification (`certutil`)
- Windows 11

## Investigation Workflow

```
Evidence Acquisition
        │
        ▼
SHA-256 Hash Verification
        │
        ▼
Analyze Email Headers
        │
        ▼
Review Message Routing
        │
        ▼
Extract Sender Metadata
        │
        ▼
Validate SPF
        │
        ▼
Validate DKIM
        │
        ▼
Validate DMARC
        │
        ▼
WHOIS & IP Reputation Analysis
        │
        ▼
Inspect Embedded Links
        │
        ▼
Correlate Indicators
        │
        ▼
Determine Email Authenticity
```

## Key Investigation Steps

### 1. Evidence Verification

Verified SHA-256 hashes of all `.eml` files to ensure forensic integrity before beginning the investigation.

### 2. Email Header Analysis

Examined:

- Received headers
- Sender information
- Return-Path
- Message-ID
- Routing path
- Timestamp consistency

to reconstruct email transmission.

### 3. Authentication Validation

Validated industry-standard authentication mechanisms:

- SPF
- DKIM
- DMARC

to determine whether each email originated from an authorized sender.

### 4. OSINT Investigation

Performed WHOIS and IP reputation lookups on originating IP addresses and domains to identify suspicious infrastructure and spoofing services.

### 5. Phishing Analysis

Inspected HTML content to identify mismatched hyperlinks and other phishing indicators hidden within email bodies.

### 6. Evidence Correlation

Correlated:

- Authentication failures
- Suspicious IP addresses
- Header inconsistencies
- Email routing
- Embedded links

to determine whether each email was legitimate or spoofed.

## Key Findings

- Successfully distinguished legitimate emails from spoofed emails.
- Identified spoofing attempts through failed SPF, DKIM, and DMARC validation.
- Detected phishing indicators by analyzing embedded hyperlinks.
- Traced suspicious sender infrastructure using WHOIS and IP reputation analysis.
- Demonstrated how email header analysis can reveal malicious activity even when message content appears legitimate.




