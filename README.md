# Mediroza-Hospital-Penetration-Testing-Report

# Authorized Black-Box Web Application Security Assessment — Mediroza General Hospital | Networkwalks B082 Internship

Overview

This repository contains the documentation and evidence from an authorized black-box penetration testing assessment conducted against the Mediroza General Hospital web application.

The assessment was performed as part of the Networkwalks Cybersecurity B082 Internship — Week 4 Capstone.

Target:

https://medirozahospital.com

Primary scope:

Patient Portal

Primary authentication endpoint:

/patient/login.php
Assessment Objectives

The assessment focused on identifying and validating:

Web application attack surfaces
Authentication weaknesses
Username enumeration
SQL injection
Authentication bypass
Confidential document exposure
PDF encryption weaknesses
Metadata leakage
Public directory listing
Database backup exposure
Sensitive information disclosure
Attack Chain
Reconnaissance
      │
      ▼
robots.txt
      │
      ▼
Patient Portal Discovery
      │
      ▼
Username Enumeration
      │
      ▼
SQL Injection
      │
      ▼
Authentication Bypass
      │
      ▼
Confidential Patient Reports
      │
      ▼
PDF Password Recovery
      │
      ▼
PDF Metadata
      │
      ▼
/old/ Directory
      │
      ▼
Database Backup
      │
      ▼
Employee & Shareholder Data
Key Findings
ID	Finding	Severity
MED-01	Username Enumeration	Medium
MED-02	SQL Injection / Authentication Bypass	Critical
MED-03	Confidential Patient PDF Exposure	High
MED-04	Weak PDF Passwords	High
MED-05	Sensitive PDF Metadata Disclosure	Medium
MED-06	Public Database Backup	Critical
MED-07	Employee & Shareholder Data Exposure	Critical
Overall Risk
CRITICAL

The vulnerabilities can be chained together to progress from publicly accessible information to confidential patient, employee and corporate information.

Tools

The assessment used tools including:

curl
whois
nslookup
WhatWeb
WAFW00F
wget
pdfinfo
pdf2john.pl
John the Ripper
qpdf
ExifTool
Evidence

Evidence is organized chronologically under the EVIDENCE/ directory.

EVIDENCE/
├── 01-reconnaissance/
├── 02-patient-portal/
├── 03-username-enumeration/
├── 04-sql-injection/
├── 05-patient-reports/
├── 06-pdf-password-recovery/
├── 07-pdf-metadata/
├── 08-old-directory/
└── 09-database-backup/
Reports

The complete professional penetration testing report is available under:

REPORT/
└── Mediroza-Penetration-Testing-Report.pdf
Remediation Priorities
Critical
Fix SQL injection using parameterized queries.
Remove database backups from the public web root.
Disable directory indexing.
Implement strict authorization for patient documents.
Remove exposed sensitive employee and shareholder information.
Review and secure all historical backups.
High
Strengthen document encryption.
Replace weak PDF passwords.
Store patient documents outside the public web root.
Implement proper access-control checks.
Medium
Prevent username enumeration.
Remove unnecessary PDF metadata.
Reduce unnecessary technology disclosure.
Authorization

This project was performed as an authorized cybersecurity laboratory assessment.

Testing was restricted to the approved target and scope.

No denial-of-service testing or social-engineering activity was performed.

Disclaimer

This repository is intended for educational and authorized security-testing purposes only.

The techniques and procedures documented here must not be used against systems without explicit authorization from the system owner.

Project

Networkwalks Cybersecurity B082 Internship

Assessment: Mediroza General Hospital
Type: Authorized Black-Box Penetration Test
Risk: CRITICAL

Prepared for educational and professional cybersecurity assessment purposes.
