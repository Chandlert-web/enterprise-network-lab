# Enterprise Network Lab

## Overview
This project demonstrates the design, configuration, monitoring, and troubleshooting of a segmented enterprise network.  
The lab is built to mirror real-world enterprise and service provider environments, with an emphasis on reliability, scalability, and operational visibility.

---

## Objectives
- Design a structured enterprise network using VLAN segmentation
- Implement inter-VLAN routing and centralized network services
- Apply structured troubleshooting using the OSI model
- Demonstrate monitoring and operational best practices
- Document configurations and incident resolution clearly

---

## Network Architecture
The network is designed with multiple VLANs to separate traffic by function, improve security, and simplify troubleshooting.  
Routing is used to enable controlled communication between segments while maintaining isolation where required.

### Enterprise Network Topology

This project implements a segmented enterprise network design using VLANs and router-on-a-stick inter-VLAN routing.

The topology includes:
- A router performing inter-VLAN routing
- An 802.1Q trunk between the router and access switch
- Segmented VLANs for Users, Servers, and Management networks

The network topology diagram is available in the `diagrams/` directory of this repository.

Planned components include:
- Access and distribution switching
- Inter-VLAN routing
- Centralized DHCP and DNS services
- Monitoring and alerting visibility

---

## Technologies & Tools
- **Routing & Switching:** Cisco IOS-style configuration
- **Networking:** TCP/IP, VLANs, Subnetting, ARP
- **Monitoring:** SNMP, ICMP, performance metrics
- **Troubleshooting:** OSI model, packet loss, latency analysis
- **Tools:** SolarWinds concepts, Wireshark, Linux, Git/GitHub

---

## Zero Trust Alignment

This network design aligns with Zero Trust principles by enforcing segmentation and controlled access
between network zones. VLANs are used to isolate user, server, and management traffic, while inter-VLAN
routing is explicitly configured to prevent implicit trust and limit lateral movement.

Access between segments is intentional, monitored, and auditable.

## Repository Structure

---

## Key Skills Demonstrated
- Enterprise network design and segmentation
- Routing and switching fundamentals
- Proactive monitoring and fault detection
- Structured troubleshooting and root cause analysis
- Technical documentation and operational clarity

---

## Status
This project is actively being expanded with additional configurations, diagrams, and troubleshooting scenarios.
