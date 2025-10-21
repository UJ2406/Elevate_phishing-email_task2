# Phishing Email Analysis (Task 2)

## 📋 Task Overview
Analyze a suspicious email for phishing characteristics, including header and content review, social engineering detection, and report creation. 

---

## 🎯 Objectives
Analyze a sample phishing email to identify indicators of compromise and document findings as per requirements.

---

## 🛠️ Tools Used
- Email Header Analyzer (MXToolbox)
- Manual Content Inspection
- Reference: PhishTank phishing sample database

---

## ⚙️ Methodology

The phishing email analysis was carried out using a systematic approach:

1. **Email Sample Collection:** Obtained a suspicious phishing email for detailed analysis.
2. **Header Analysis:** Used online email header analyzers like MXToolbox to examine the sender IP, domain alignment, SPF, DKIM, and DMARC authentication status. Key indicators such as spoofed domains, failed authentication, and blacklisting were identified.
3. **Content Examination:** Inspected email language for urgency, spelling/grammar errors, generic greetings, and threatening language aimed at social engineering victims.
4. **Link and Attachment Inspection:** Analyzed embedded URLs for domain manipulation, absence of HTTPS, URL shorteners hiding true destinations, and presence of suspicious attachments.
5. **Social Engineering Detection:** Detected psychological triggers such as urgency, authority impersonation, fear, and loss aversion.
6. **Reporting:** Compiled all findings, including screenshots and header analysis, into a structured report for submission.

---

## 📝 Analyzed Phishing Email Sample

**From:** security-team@amaz0n-verification.com  
**To:** customer@email.com  
**Date:** January 15, 2025, 03:42 AM  
**Subject:** URGENT: Your Amazon Account Has Been Suspended – Immediate Action Required!  
**Originating IP:** 123.45.67.89

### Email Body Red Flags

- Claimed security threat from Nigeria device
- Threatens permanent account closure within 24 hours
- Requests highly sensitive data: full name, address, credit card, CVV, SSN, password
- Multiple suspicious links (typosquatting, bit.ly shortener)
- Grammar/spelling errors (“temporarely”, “permanantly”)
- Generic greeting, false claims of security

---

##  🔍 Phishing Indicators Detected

| Indicator    | Evidence          | Severity    |
|--------------|-------------------|-------------|
| Spoofed domain | amaz0n-verification.com | Critical |
| Bad origin IP | Russia, not Amazon | Critical |
| SPF/DKIM/DMARC | All failed or absent | Critical |
| Malicious links | Typosquatting, shortener | Critical |
| Sensitive info requests | Password, SSN, CVV | Critical |
| Threat language | "Legal action", urgency | Critical |
| Grammar errors | "temporarely" spelling | High |
| Generic greeting | "Dear Valued Customer" | High |
| Blacklisted sender | IP/domain flagged | High |
| Social engineering | Authority, urgency, loss aversion | Critical |

---

## 🔐 Email Header Analysis


- **Authentication Results**:  
    - SPF: Fail  
    - DKIM: Fail  
    - DMARC: No record  
    - Origin server: suspicious IP  
    - Blacklist: Yes
- **Mailer Used**: PHP/7.3, typical for spam/phishing
- **Screenshots**:  
  ![Header Analyzer Results]  
  ![SPF/DKIM Info]  
  ![Received Header Details]

---

## 📊 Interview Questions & Answers

**1. What is phishing?**  
Phishing is a cybercrime technique where attackers impersonate trustworthy entities via email to steal sensitive information.

**2. How to identify a phishing email?**  
Through sender/email checks, failed email authentication, suspicious requests/links, spelling errors, urgent language, and requests for sensitive data.

**3. What is email spoofing?**  
Forging the sender’s address to appear as a legitimate contact, exploiting weaknesses in SMTP.

**4. Why are phishing emails dangerous?**  
They result in identity theft, financial loss, malware infection, and breach of other accounts.

**5. How can you verify sender authenticity?**  
Check full header details, analyze SPF/DKIM/DMARC results, and validate via official sources.

**6. What tools are used for header analysis?**  
MXToolbox, Google Message Header, WHOIS, VirusTotal, and email client security features.

**7. Response to suspected phishing email?**  
Do not interact; report to IT/security/organization; mark as phishing; delete.

**8. Use of social engineering in phishing?**  
Attackers manipulate urgency, fear, authority, and personalize attacks to bypass defenses.

---

## 🚀 Key Takeaways

- Phishers often use domain spoofing with lookalike domains and bypass authentication because many domains lack SPF/DKIM/DMARC.
- Robust phishing detection combines both technical header analysis and behavioral content examination.
- Legitimate organizations do not request sensitive data like passwords, SSNs, or CVVs by email and maintain high-quality spelling and personalization.
- Email header authentication failures, suspicious origin IPs, and blacklisted senders are strong technical red flags.
- Awareness of social engineering tactics enhances defense against phishing attempts.
- Practical hands-on experience with phishing email analysis tools is critical for cybersecurity preparedness.

---

## 📂 Repository Content 


```
cybersecurity-task2-phishing-mail/
├── README.md           # This file - Complete documentation
├── phishingemail.txt   # Full sample email
├── phishemailheaders.txt    # Raw headers for analysis
├── analysisreport.txt  # Detailed findings
├── phishingindicators.txt  # List of red flags
└── image.png           # Screenshot of scan execution
```


---


