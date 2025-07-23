## 📈 Results & Observations

After configuring `named.conf.options` and restarting BIND9, DNS resolution was successfully tested using both `dig` and `host`.

### 🔍 `dig` Command Output
```bash
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
