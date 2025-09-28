# ElevateLabs_CS_Task04
Setup and Use a Firewall on Windows/Linux
# Task 4: Setup and Use a Firewall on Kali Linux

## Objective
Configure and test basic firewall rules using **UFW** on Kali Linux to understand how host-based firewalls filter traffic.

---

## Steps Taken
1. Installed and enabled UFW.
2. Listed current firewall rules (`ufw status numbered`).
3. Added a rule to **block inbound traffic on port 23 (Telnet)**.
4. Tested the block with `nc -vz localhost 23` → connection refused.
5. Added a rule to **allow SSH (22/tcp)**.
6. Removed the test block rule and restored original state.
7. Documented all steps and results.

---

## Commands Used
```bash
sudo apt install ufw -y
sudo ufw enable
sudo ufw status verbose
sudo ufw deny 23/tcp
nc -vz localhost 23
sudo ufw allow 22/tcp
sudo ufw delete deny 23/tcp
