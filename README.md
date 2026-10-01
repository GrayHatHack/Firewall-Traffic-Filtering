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
