# Web Application Security Assessment — Internship Project
##[Documentation](https://security-assessment-internship.vercel.app/)

A penetration testing project completed as part of a cybersecurity internship task: identifying vulnerabilities in a web application and recommending data protection improvements, using industry-standard tools and methodology.

## 🎯 Objective

Identify vulnerabilities across critical areas of a web application — login pages, user profiles, and APIs — with a focus on:
- SQL Injection (SQLi)
- Cross-Site Scripting (XSS)
- Cross-Site Request Forgery (CSRF)
- Security misconfigurations and information disclosure

## 🛠️ Tools Used

- **OWASP ZAP** (Zed Attack Proxy) — automated crawling (Spider, AJAX Spider) and active vulnerability scanning
- **Browser DevTools** — manual request/response inspection, header analysis, and authentication architecture review
- **Manual testing** — payload-based verification of every automated finding before it was recorded

## 🧪 Test Environment

All hands-on testing in this repository was performed against **[OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)**, an intentionally vulnerable application maintained by OWASP specifically for security training. This allowed the full testing methodology to be developed and validated safely and legally before being applied to any live or staging system.

> **Note:** No testing in this repository was performed against any live production system without authorization. Any future testing against a staging or production environment will only be carried out with explicit written permission, a defined scope, and an agreed test window.

## 🔍 Methodology

1. **Reconnaissance** — manual browsing and automated crawling to map application routes, forms, and parameters
2. **Automated scanning** — OWASP ZAP Active Scan to surface candidate vulnerabilities
3. **Manual verification** — every scanner finding was manually reproduced to rule out false positives
4. **Risk rating** — each confirmed finding rated High / Medium / Low / Informational based on impact and exploitability
5. **Reporting** — findings documented with evidence, CWE references, and remediation guidance

## 📋 Key Findings (Summary)

| ID | Finding | Risk | Verified |
|----|---------|------|----------|
| F-004 | SQL Injection — product search endpoint | High | ✅ |
| F-006 | DOM-Based Cross-Site Scripting (XSS) — search | High | ✅ |
| F-001 | Missing Anti-Clickjacking Header | Medium | ✅ |
| F-002 | Session/Transport Identifier Exposed in URL | Medium | ✅ |
| F-003 | Missing X-Content-Type-Options Header | Low | ✅ |
| F-005 | Verbose Error Message — Information Disclosure | Low | ✅ |
| F-007 | CSRF — Assessed, Not Exploitable (Token-Based Auth) | Informational | ✅ |

Full details — including evidence, CWE references, and remediation recommendations for each finding — are in the report.

## 📁 Repository Contents

```
├── Internee_Security_Assessment_Report.docx   # Full formal report
├── Internee_Security_Findings_Tracker.xlsx    # Working findings log
└── README.md                                  # This file
```

## 💡 Skills Demonstrated

- Web application vulnerability assessment (OWASP Top 10 concepts)
- Tool-assisted and manual penetration testing
- Evidence-based finding verification (avoiding false positives)
- Security reporting and risk communication
- Responsible/ethical testing practices and scope discipline

## ⚠️ Disclaimer

This project is for educational and professional development purposes. Testing was conducted only against an authorized, intentionally vulnerable practice application. This repository does not contain any vulnerability details about real, live, third-party systems.
