# 🧪 VM Networking Lab

This repository documents a series of virtual machine networking experiments designed to reinforce key skills in DNS setup, firewall rules, subnetting, and intrusion detection. These labs reflect my hands-on learning as I prepare for Network+ and Security+ certification.

---

## 📁 Lab Index

- DNS Configuration
- Subnetting & Routing
- Firewall Management
- Wireshark Packet Capture (Coming Soon)

---

## 🔍 DNS Configuration

This lab uses BIND9 on Ubuntu to configure a local DNS server. Below are the steps taken and validation commands used.

$ dig example.com

;; ANSWER SECTION:
example.com.     300 IN A 93.184.216.34

$ host example.com

example.com has address 93.184.216.34

+------------+         +------------+         +--------------------+
| Client VM  |  --->   |   BIND9    |  --->   | Public DNS Forwarder|
| (dig/host) |         | Local DNS  |         | (8.8.8.8 / 1.1.1.1) |
+------------+         +------------+         +--------------------+
      |                     |                        |
      |<--------------------|<-----------------------|
   Resolved IP        Forwarded Query          Final Answer

### ✅ Installation
```bash
sudo apt update
sudo apt install bind9 dnsutils
>>>>>>> 45f5e85 (Add DNS resolution results and diagram)
>>>>>>> 6ac88e4 (Add DNS resolution results and diagram)
