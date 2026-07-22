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
## Phase 2 – Target Identification

### Assessment Question 

How can GitLab's official digital presence be verified before collecting technical intelligence?

### Why This Matters

Before collecting technical intelligence, it is important to verify the target organization and its official digital properties. Establishing this baseline helps ensure that all information gathered throughout the investigation is accurately attributed to GitLab and reduces the risk of analyzing unrelated or impersonating assets.

### Collection Method

The investigation began by reviewing GitLab's official website to identify the organization's primary services, official domains, and publicly available resources. Information collected during this phase will serve as the baseline for subsequent OSINT collection.

### Evidence

![GitLab Official Website](screenshots/01-gitlab-official-website.png)

### Findings

| Observation | Result |
|--------------|--------|
| Organization | GitLab |
| Official Company Website | about.gitlab.com |
| Primary Platform | gitlab.com |
| Primary Service | DevSecOps Platform |
| Official Documentation | docs.gitlab.com |
| Official Security Resources | about.gitlab.com/security/ |

### Analysis

The official GitLab website confirmed the organization's identity and established trusted digital properties for the remainder of the assessment. Future findings, including WHOIS records, DNS information, certificate transparency logs, and infrastructure data, will be compared against these confirmed assets before being attributed to GitLab.

Establishing verified organizational assets is a fundamental step in OSINT investigations because it reduces attribution errors and provides a reliable foundation for intelligence collection.

### Analyst Assessment

Threat actors often begin reconnaissance by identifying an organization's official domains, products, documentation, and public services. This information helps attackers understand the target environment and may assist with phishing, social engineering, or infrastructure mapping.

Defenders can use the same publicly available information to validate their external asset inventory and identify unauthorized domains or services that could be used for impersonation.
