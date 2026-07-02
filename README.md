# Website Vulnerability Assessment Report

## Project Overview
This repository contains a passive, read-only security assessment of my personal academic project, the Laundry Management System (Washify).

## Website Tested
- **Website:** Laundry Management System (Washify)
- **URL:** https://laundry-management-system-1-2prt.onrender.com
- **Ownership:** Personal academic project owned and controlled by the tester

## Scope and Ethics
The assessment was limited to public-facing pages and normal Admin Portal access.

No login bypass, password testing, exploitation, brute-force attacks, denial-of-service testing, or active vulnerability scanning was performed.

## Tools Used
- Google Chrome DevTools
- Canva

## Key Findings

### 1. Incomplete Security Header Configuration — Medium Risk
The website included `Strict-Transport-Security` and `X-Content-Type-Options`, but Content-Security-Policy, X-Frame-Options, Referrer-Policy, and Permissions-Policy were not observed during passive inspection.

**Recommendation:** Configure the missing headers through Helmet in the Express backend.

### 2. Application Data Stored in Local Storage — Medium Risk
The application stores an administrator login indicator and laundry-entry data in browser Local Storage.

**Recommendation:** Use backend authentication and authorization controls, server-side sessions, or secure HttpOnly cookies.

## Informational Observations
- No cookies were observed on the public homepage.
- No obvious passwords, API keys, tokens, or database connection strings were found in public page source.
- The Admin Portal displayed a username-and-password login screen during normal access.
- No session data was observed during the review.

## Repository Contents
- `Washify_Vulnerability_Assessment_Report_Palak_Agarwal.pdf` — Final assessment report
- `evidence/` — Supporting screenshots from passive browser inspection
