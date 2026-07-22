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

### Intelligence Requirement

The objective of this assessment is to identify publicly available information about GitLab that could be leveraged during the reconnaissance phase of a cyber attack while demonstrating how passive OSINT techniques can help defenders understand and reduce an organization's public attack surface.

Before collecting intelligence, the target organization must first be verified to ensure that all information gathered throughout the investigation can be accurately attributed to GitLab.

--- 
## Phase 2 – Target Identification

### Intelligence Question

How can GitLab's official digital presence be verified before collecting technical intelligence?

### Collection Method

GitLab's official company website, product documentation, security resources, and coordinated vulnerability disclosure page were reviewed using a web browser.

Official GitLab-controlled sources were prioritized over third-party sources to establish a reliable baseline for the investigation.

### Findings

| Item | Confirmed Property | Confidence |
|---|---|---|
| Organization | GitLab | High |
| Official company website | `about.gitlab.com` | High |
| Primary service domain | `gitlab.com` | High |
| Official documentation | `docs.gitlab.com` | High |
| Official security resource | `about.gitlab.com/security/` | High |
| Coordinated disclosure page | `about.gitlab.com/security/disclosure/` | High |

### Evidence

![GitLab Official Website](screenshots/01-gitlab-official-website.png)

### Analysis

The official GitLab website and related GitLab-controlled resources confirm the organization's primary digital properties.

Establishing these verified properties creates a trusted baseline for the remainder of the investigation. Domains, certificates, infrastructure, and other assets discovered during later phases should be compared against these confirmed properties before being attributed to GitLab.

This process reduces the possibility of incorrectly associating unrelated websites, third-party services, or impersonation domains with the organization.

### Security Relevance

An attacker may begin reconnaissance by identifying an organization's official domains, documentation, security resources, products, and public services. This information can help an attacker understand the organization's technology environment and create more believable social-engineering or impersonation attempts.

Defenders can use the same information to maintain an accurate external asset inventory and identify websites or domains falsely claiming to represent the organization.


