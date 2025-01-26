# Lecture Notes: Zero Trust Concept

<img width="658" alt="image" src="https://github.com/user-attachments/assets/093e05dd-f717-4d8a-9ab5-13668dba6426" />

<img width="664" alt="image" src="https://github.com/user-attachments/assets/c6b3e053-0e37-4f14-a678-e934f4092a75" />


## Overview
- **Zero Trust**:
  - A security framework that requires strict identity verification and assumes no resource, user, or application is inherently trusted.
  - Applies to both **on-premises** and **cloud environments**.

---

## Key Principles of Zero Trust

### 1. **Verify Explicitly**
- Always authenticate and authorize users before granting access.
- Applies even to employees accessing resources.

### 2. **Use Least Privilege Access**
- Grant users only the permissions they need to perform their tasks.
- Avoid giving owner-level privileges unless absolutely necessary.

### 3. **Assume Breach**
- Proactively identify vulnerabilities by assuming a security breach can occur.
- Continuously monitor and evaluate potential threats.

---

## Areas to Secure
- **Identity**:
  - Ensure robust user authentication and authorization processes.
- **Endpoints**:
  - Protect devices accessing resources.
- **Applications**:
  - Secure deployed applications both on-premises and in the cloud.
- **Data**:
  - Implement measures to safeguard sensitive data.

---

## Example Scenario
- A company is using Azure resources (e.g., virtual machines, SQL databases, web apps) alongside an on-premises environment with applications, servers, and firewalls.
- Employees manage resources across both environments.
- Implementing zero trust ensures:
  - Authentication and authorization are enforced for all users.
  - Minimal permissions are granted to prevent misuse.
  - Potential breaches are accounted for, minimizing impact.

---

## Summary
- **Core Philosophy**: "Never trust, always verify."
- **Key Principles**:
  - Verify explicitly.
  - Apply least privilege access.
  - Assume breach.
- **Focus Areas**:
  - Identity, endpoints, applications, and data security.
- **Objective**:
  - Reduce vulnerabilities and enhance overall security posture in hybrid environments.






