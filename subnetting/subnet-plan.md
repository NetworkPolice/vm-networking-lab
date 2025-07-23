# Subnetting Plan for VM Lab

This document outlines the IP allocation strategy for my virtual machine lab. It's designed to segment services for better security, traffic flow, and learning clarity.

## Base Network: 192.168.100.0/24

| Subnet | CIDR Notation        | Role                  | IP Range             |
|--------|----------------------|------------------------|----------------------|
| A      | 192.168.100.0/26     | Web Servers (future)  | 192.168.100.1–62     |
| B      | 192.168.100.64/26    | Core Infra (Ubuntu VM) | 192.168.100.65–126   |
| C      | 192.168.100.128/26   | Client/Test Machines   | 192.168.100.129–190  |
| D      | 192.168.100.192/26   | Reserved / DMZ         | 192.168.100.193–254  |

## Notes

- The **Ubuntu VM** sits in Subnet B and hosts Apache2, Python, and DNS services as needed.
- Future web VMs will be placed in Subnet A for logical separation.
- Subnet D is reserved for potential firewall testing or external-facing services.
## 📊 Subnet Diagram Overview

Here's a simplified layout of the VM lab subnets:

+----------------------------+        +----------------------------+
| Subnet A: Web Servers      |        | Subnet B: Infrastructure   |
| CIDR: 192.168.100.0/26     |        | CIDR: 192.168.100.64/26    |
| Range: 192.168.100.1–62    |        | Range: 192.168.100.65–126  |
| Example VM: web-01         |        | Example VM: ubuntu-core    |
+----------------------------+        +----------------------------+

         ↕ Routing, Firewall Controls

+----------------------------+        +----------------------------+
| Subnet C: Clients          |        | Subnet D: DMZ / Reserved   |
| CIDR: 192.168.100.128/26   |        | CIDR: 192.168.100.192/26   |
| Range: 192.168.100.129–190 |        | Range: 192.168.100.193–254 |
| Example VM: client-01      |        | Example VM: dmz-01         |
+----------------------------+        +----------------------------+
