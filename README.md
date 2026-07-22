# Passive Open-Source Intelligence Assessment of GitLab

## Project Overview

This project documents a passive Open-Source Intelligence (OSINT) assessment of GitLab's publicly accessible digital footprint.

The objective of this assessment is to identify information that is publicly available about GitLab and evaluate how that information could assist an attacker during the reconnaissance phase of a cyber attack. At the same time, the assessment demonstrates how defenders can use the same intelligence to better understand and reduce their organization's attack surface.

Only passive collection techniques were used throughout this investigation. No active scanning, exploitation, authentication attempts, vulnerability testing, social engineering, or interaction with GitLab systems was performed.

---

## Objectives

- Identify GitLab's official public assets.
- Collect publicly available intelligence using passive OSINT techniques.
- Analyze how attackers could leverage publicly available information.
- Provide defensive recommendations based on the findings.

---

## Scope

### In Scope

- Official GitLab resources
- Public DNS records
- WHOIS records
- Certificate Transparency logs
- Public search engines
- Public OSINT platforms

### Out of Scope

- Port scanning
- Vulnerability scanning
- Brute-force attacks
- Exploitation
- Authentication testing
- Social engineering
- Contacting employees

---

# Investigation

## Phase 1 - Planning and Direction

### Assessment Objective

The objective of this assessment is to identify publicly available information about GitLab that could be leveraged during the reconnaissance phase of a cyber attack while demonstrating how passive OSINT techniques can help defenders understand and reduce an organization's public attack surface.

Before collecting intelligence, the target organization must first be verified to ensure that all information gathered throughout the investigation can be accurately attributed to GitLab.

--- 
# Phase 2 – Target Identification

### Assessment Question

What publicly available organizational information can be identified through GitLab's official website?

### Why This Matters

An organization's official website is often the first source consulted during passive reconnaissance. Reviewing official resources helps establish a trusted starting point for an investigation while identifying information the organization intentionally makes available to customers, partners, investors, researchers, and the public.

### Collection Method

The official GitLab website (`about.gitlab.com`) was reviewed using Firefox on host Mac browser. The **Company** navigation menu was explored to identify publicly available organizational resources, including company information, leadership pages, investor relations, and other corporate resources.

### Evidence

**Figure 1 – GitLab Company Navigation**

![GitLab Company Navigation](screenshots/01-gitlab-company-menu.png)

**Figure 2 – GitLab Executive Leadership**

![GitLab Executive Leadership](screenshots/02-gitlab-executive-team.png)

**Figure 3 – GitLab Board of Directors**

![GitLab Board of Directors](screenshots/03-gitlab-board-of-directors.png)

### Findings

| Observation | Result |
|--------------|--------|
| Official Website | `about.gitlab.com` |
| Company Resources | Public access to company, careers, events, investor relations, trust center, handbook, and press resources |
| Executive Leadership | Executive leadership information is publicly available |
| Corporate Governance | Board of Directors information is publicly available |

### Analysis

Reviewing GitLab's official website identified several publicly accessible organizational resources. The **Company** navigation menu provides direct access to information about the organization's leadership, governance, investor relations, trust center, handbook, and other corporate resources.

The Executive Leadership and Board of Directors pages provide publicly available information about GitLab's organizational structure, demonstrating a transparent corporate presence and establishing additional sources for passive intelligence collection.

### Analyst Assessment

GitLab maintains a comprehensive public-facing website that intentionally provides organizational and corporate information. From an OSINT perspective, these resources establish verified information about the company and its structure while illustrating the types of publicly available data that may be referenced during reconnaissance activities. All information was obtained from official public web pages.

---
# Phase 3 – Domain Registration Analysis

### Assessment Question

What publicly available domain registration information can be identified for GitLab's primary domain?

### Why This Matters

WHOIS records provide publicly available registration information that helps analysts validate a domain's legitimacy, identify its registrar, review registration history, and determine the domain's current status. This information establishes a trusted baseline before investigating an organization's DNS infrastructure and other publicly accessible assets.

### Collection Method

A WHOIS lookup was performed against GitLab's primary domain (`gitlab.com`) using the native `whois` utility in Kali Linux. The output was reviewed to identify publicly available registration information associated with the domain.

### Evidence

**Figure 4 – WHOIS Results for `gitlab.com`**

![WHOIS Results](screenshots/04-gitlab-whois-results.png)

### Findings

| Observation | Result |
|--------------|--------|
| Domain Name | `gitlab.com` |
| Registrar | Gandi SAS |
| Registrar WHOIS Server | `whois.gandi.net` |
| Creation Date | January 15, 2004 |
| Last Updated | December 11, 2025 |
| Registry Expiration Date | January 15, 2027 |
| Domain Status | `clientTransferProhibited` |
| Authoritative Name Servers | `DIVA.NS.CLOUDFLARE.COM`<br>`JERMAINE.NS.CLOUDFLARE.COM` |
| DNSSEC | Unsigned |

### Analysis

The WHOIS lookup identified GitLab's primary domain as being registered through **Gandi SAS** and showed that the domain has been registered since **2004**, indicating a long-established domain presence. The WHOIS record also identifies **Cloudflare authoritative name servers** associated with the domain, providing additional information about its publicly available DNS registration.

The domain status is listed as **clientTransferProhibited**, a standard registration status intended to help prevent unauthorized domain transfers. Additionally, the WHOIS record reports that **DNSSEC is currently unsigned**, which was documented as part of the publicly available registration information.

### Analyst Assessment

The WHOIS record provides verified registration information that confirms key details about GitLab's primary domain. The identified registrar, registration timeline, domain status, and authoritative name servers establish a foundation for the next phase of the assessment, where GitLab's DNS configuration and infrastructure will be examined using additional passive OSINT techniques.
