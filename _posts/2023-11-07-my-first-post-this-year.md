---
layout: post
title: Activity3
subtitle: The Solar Winds Breach Case Study
categories: Discussions
tags: [discussions, SolarWinds]
---

## The Solar Winds Breach Table
[activity3.docx](https://github.com/20802777/20802777.github.io/files/13769639/activity3.docx)

## The Solar Winds Breach Summary

1. **Reconnaissance:**
   - **Description:** Research on target, exploiting SolarWinds apps for passwords.
   - **Mitigations:**
     - Strengthen access controls, and use multi-factor authentication (MFA).
     - Utilize Intrusion Prevention Systems (IPS) and Security Information and Event Management (SIEM) systems to monitor and detect reconnaissance activities.

2. **Weaponization:**
   - **Description:** Hackers tested modifying SolarWinds' code.
   - **Mitigations:**
     - Employ code signing mechanisms, secure coding practices, and a Zero Trust model.
     - Use code signing and static analysis tools to ensure code integrity and identify vulnerabilities during development.

3. **Delivery:**
   - **Description:** Hackers elevated privileges using passwords and source codes.
   - **Mitigations:**
     - Implement strong password policies.
     - Use Identity and Access Management (IAM) solutions to control user access during delivery.

4. **Exploitation:**
   - **Description:** Attackers used a bait-and-switch tactic during SolarWinds' code compilation.
   - **Mitigations:**
     - Strengthen supply chain security, and implement continuous monitoring.
     - Use vulnerability scanning and penetration testing tools to identify and address weaknesses proactively.

5. **Installation:**
   - **Description:** Attackers installed a version with a backdoor.
   - **Mitigations:**
     - Use Software Composition Analysis (SCA) tools to analyze and track software components.
     - Deploy continuous monitoring to identify unusual patterns during installation.

6. **Command and Control:**
   - **Description:** Lack of multi-factor authentication facilitated access.
   - **Mitigations:**
     - Enforce multi-factor authentication.
     - Utilize Intrusion Detection and Prevention Systems (IDPS) to monitor and block suspicious activities.

7. **Actions on Objectives:**
   - **Description:** Concerns about data exfiltration and potential destruction.
   - **Mitigations:**
     - Regularly back up critical data, and implement data integrity checks.
     - Use network segmentation and Endpoint Detection and Response (EDR) solutions to detect and prevent unauthorized actions.

In summary, the SolarWinds attack involved exploiting weaknesses across multiple phases of the kill chain, highlighting the need for a comprehensive cybersecurity strategy that includes measures such as access controls, code integrity checks, continuous monitoring, and proactive vulnerability management.
