# Firewall Rules & Network Traffic Filtering

## 📌 Objective
To understand how firewalls regulate network traffic, control incoming and outgoing packet flows, and enforce strict security policies to protect systems from unauthorized access and network-based threats.

---

## 🛠️ Concepts & Tools Covered
* **Core Concepts:** Packet Filtering, Stateful Inspection, Inbound/Outbound Traffic Control, Default Deny Policy.
* **Tool Used:** UFW (Uncomplicated Firewall) on Linux/Ubuntu/Kali environments.

---

## ⚙️ Practical Implementation & Commands

In this lab, we explore how security administrators interact with firewalls to secure network interfaces. Below are the fundamental operations performed:

### 1. Check Firewall Status & Rules
To inspect whether the firewall is active and view current security rules (including default policies):
```bash
sudo ufw status verbose

```

### **2. Enable or Disable the Firewall**
Enforcing active state filtering on the system:
```bash
sudo ufw enable
```
(To disable for troubleshooting purposes: sudo ufw disable)

### **3. Setting Up Traffic Filtering Rules**
* **Allowing Specific Services/Ports:** 
  To permit incoming traffic on specific ports (e.g., SSH port 22 or Web traffic port 80):
  ```bash
  sudo ufw allow 22/tcp
  sudo ufw allow 80/tcp
  ```
* **Blocking Unauthorized Ports:**
  To restrict exposure on vulnerable or unused ports:
  ```bash
  sudo ufw deny 8080
  ```
* **Blocking Specific IP Addresses:**
  To prevent malicious or suspicious hosts from interacting with the system:
  ```bash
  sudo ufw deny from 192.168.1.100
  ```

### **4. Managing and Deleting Rules**
If a rule is no longer required or was misconfigured, it can be removed safely:
```Bash
sudo ufw delete allow 22/tcp
```

## 🚀 Key Takeaway
Learned that Proper firewall configuration acts as the first line of defense in network security. Implementing a "Default Deny" policy ensures that only authorized, necessary traffic is allowed into the system, drastically minimizing the attack surface.    
  

