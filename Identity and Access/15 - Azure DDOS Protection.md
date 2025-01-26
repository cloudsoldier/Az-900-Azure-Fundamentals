https://azure.microsoft.com/en-us/pricing/details/ddos-protection/

# Lecture Notes: Azure DDoS Protection

## Overview
- **DDoS (Distributed Denial-of-Service) Attacks**:
  - Malicious users use bots to flood traffic to an application, overwhelming its resources.
  - The result: The application cannot serve legitimate users, effectively denying service.

- **Example Scenario**:
  - A web application hosted on virtual machines in Azure.
  - A DDoS attack floods traffic, making the application unresponsive to legitimate users.
  - This constitutes a **network-based attack** on infrastructure.

---

## Azure DDoS Protection

### Types of DDoS Protection
1. **Network Protection**:
   - Protects a set of public IP addresses.
2. **IP Protection**:
   - Provides protection for individual public IP resources.

---

## Key Features of Azure DDoS Protection
- **24/7 Traffic Monitoring**:
  - Monitors incoming traffic automatically to detect potential attacks.
- **Real-Time Metrics**:
  - Provides real-time insights when an attack is detected.
- **Rapid Response Team**:
  - Access to a team for immediate response during attacks.

---

## Cost Consideration
- Azure DDoS Protection is not free and comes with associated costs.
- **AZ-900 Exam Focus**:
  - Understand the existence and purpose of Azure DDoS Protection but no need for in-depth technical details.

---

## Summary
- **Purpose**: Protect Azure infrastructure against DDoS attacks.
- **Types**: Network-level and IP-level protection.
- **Benefits**:
  - Continuous monitoring.
  - Real-time metrics during attacks.
  - Support from a rapid response team.
- **Key Takeaway**: Azure DDoS Protection is an essential service to safeguard applications and infrastructure against DDoS attacks.

