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

How can GitLab's official online presence be verified before collecting technical intelligence?

### Why This Matters

Before collecting information about an organization, it is important to verify that the investigation is focused on official company resources. Establishing a trusted starting point reduces the risk of gathering information from unofficial or fraudulent sources and provides a reliable foundation for the remainder of the assessment.

### Collection Method

The official GitLab website was reviewed using a web browser in Kali Linux. The organization's publicly available homepage was examined to verify its identity and understand the primary service it provides.

### Evidence

**Figure 1 – GitLab Official Website**

![GitLab Official Website](screenshots/01-gitlab-official-website.png)

### Findings

| Observation | Result |
|--------------|--------|
| Organization | GitLab |
| Official Website | `about.gitlab.com` |
| Primary Product | GitLab Platform |
| Primary Service | DevSecOps Platform |

### Analysis

The official GitLab website confirms the organization's identity and establishes `about.gitlab.com` as an official company resource. The homepage identifies GitLab as a DevSecOps platform and provides a trusted starting point for collecting additional publicly available information throughout the assessment.

### Analyst Assessment

The official company website serves as the foundation for the remainder of the investigation. Verifying GitLab's official online presence ensures that future findings—including domain registration records, DNS information, certificate transparency logs, and other publicly available intelligence—can be confidently attributed to the correct organization.
