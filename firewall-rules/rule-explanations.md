# 🛡️ Rule Explanations – With a Splash of Humor

These firewall rules keep the lab secure, but that doesn't mean they can't have some personality. Below is a breakdown of why each rule exists—and the logic behind giving some traffic the cold shoulder.

---

## 🚪 Rule: Allow SSH from internal subnet  
```bash
sudo ufw allow from 192.168.100.0/24 to any port 22 proto tcp
