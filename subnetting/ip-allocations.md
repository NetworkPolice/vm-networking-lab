# IP Allocations – VM Lab Environment

This file maps virtual machines to IP addresses across the subnet layout defined in `subnet-plan.md`.

## Subnet B – Infrastructure Services

| Hostname      | Role                  | IP Address        | Notes                                 |
|---------------|-----------------------|-------------------|----------------------------------------|
| ubuntu-core   | Apache2 + Python + DNS| 192.168.100.70    | First VM; core services hub            |

## Future Subnet A – Web Servers

| Hostname      | Role         | IP Address        | Notes                 |
|---------------|--------------|-------------------|------------------------|
| web-01        | Apache Test  | 192.168.100.10    | Planned deployment     |

## Subnet C – Client Machines

| Hostname      | Role         | IP Address        | Notes                 |
|---------------|--------------|-------------------|------------------------|
| client-01     | Test Client  | 192.168.100.130   | Reserved for testing   |

## Reserved Subnet D – DMZ / External-Facing

| Hostname      | Role         | IP Address        | Notes                 |
|---------------|--------------|-------------------|------------------------|
| dmz-01        | Firewall Target | 192.168.100.200 | Placeholder for testing|
