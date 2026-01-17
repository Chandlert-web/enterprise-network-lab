# VLAN and Inter-VLAN Routing Documentation

## Overview
This document explains the VLAN segmentation and inter-VLAN routing configuration implemented in the enterprise network lab.

The goal of this design is to separate network traffic by function, improve security, simplify troubleshooting, and enable controlled communication between network segments.

---

## VLAN Design
The network is segmented into the following VLANs:

- **VLAN 10 – Users**
  - End-user devices such as workstations and laptops
- **VLAN 20 – Servers**
  - Application and infrastructure servers
- **VLAN 30 – Management**
  - Network management and administrative access

This separation limits broadcast domains and reduces the impact of network issues.

---

## Access Port Configuration
Access ports are configured to place endpoints into the appropriate VLAN based on their role.

Example:
- User-facing ports are assigned to VLAN 10
- Server-facing ports are assigned to VLAN 20

Spanning Tree PortFast is enabled on access ports to allow faster link availability while preventing loops.

---

## Trunking and VLAN Propagation
A trunk link is configured between the access switch and the router to carry multiple VLANs.

- IEEE 802.1Q encapsulation is used
- Only required VLANs are allowed across the trunk
- This limits unnecessary traffic and improves security

---

## Inter-VLAN Routing
Inter-VLAN routing is implemented using a router-on-a-stick design.

Each VLAN has a dedicated subinterface:
- VLAN 10 → 192.168.10.1/24
- VLAN 20 → 192.168.20.1/24
- VLAN 30 → 192.168.30.1/24

The router provides default gateway services for each VLAN, enabling controlled communication between segments.

---

## Operational Considerations
- VLAN segmentation improves fault isolation
- Routing allows centralized policy enforcement
- This design scales easily by adding additional VLANs and subinterfaces

---

## Troubleshooting Notes
Common troubleshooting steps include:
- Verifying VLAN assignments on switch ports
- Checking trunk VLAN allowances
- Confirming subinterface encapsulation and IP addressing
- Testing gateway reachability from each VLAN

---

## Summary
This configuration demonstrates foundational enterprise networking concepts including VLAN segmentation, trunking, and inter-VLAN routing, aligned with real-world operational practices.
