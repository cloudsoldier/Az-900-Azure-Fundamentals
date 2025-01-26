# Lecture Notes: Azure Firewall Service

## Overview
- **Azure Firewall**:
  - A managed, cloud-based firewall service.
  - Provides advanced capabilities to protect resources in a virtual network.

- **Comparison with Network Security Groups (NSGs)**:
  - NSGs:
    - Basic firewall functionality.
    - Used to filter traffic with inbound and outbound rules.
    - Applied to network interfaces or subnets.
  - Azure Firewall:
    - Protects the entire virtual network.
    - Offers enhanced capabilities similar to traditional firewalls.

---

## Key Features of Azure Firewall
1. **Managed Service**:
   - Eliminates the need to purchase, install, and configure third-party firewall software.
2. **Traffic Filtering**:
   - Filters traffic not just by IP addresses but also based on domain name systems (DNS).
3. **Threat Intelligence Feeds**:
   - Alerts and denies traffic to/from known malicious IP addresses.
4. **Comprehensive Protection**:
   - Safeguards the entire virtual network, unlike NSGs, which are applied at specific levels (NICs or subnets).

---

## Use Case
- **Scenario**:
  - A company wants advanced firewall capabilities without managing its own firewall appliance.
- **Solution**:
  - Use Azure Firewall for centralized protection of all resources in the virtual network.

---

## Summary
- **Azure Firewall vs NSG**:
  - NSG is suitable for basic filtering at the network interface or subnet level.
  - Azure Firewall provides enhanced, centralized protection for the entire virtual network.
- **Key Features**:
  - Managed service.
  - Traffic filtering by IP and DNS.
  - Built-in threat intelligence.
- **Purpose**:
  - A comprehensive solution for securing virtual networks in Azure.
