# 🐝 Honeypot Server Project - Report

This report documents the deployment and analysis of a **Cowrie honeypot** on Kali Linux/Kali Purple to simulate vulnerable SSH/Telnet services, capture attacker behavior, and analyze attack patterns.

---

## 📖 Project Documentation
- Full setup details and screenshots are included in the PDF:
  docs/Honeypot Server Setup.pdf

- Additional evidence (logs, screenshots) are stored in:
  docs/screenshots

---

## ⚙️ Environment & Tools
- Operating System: Kali Linux / Kali Clone VM
- Honeypot Framework: Cowrie
- Language: Python 3 (with virtualenv)
- Virtualization: VirtualBox / VMware
- Additional Tools: Hydra, Medusa (for brute force simulation)

---

## 🚀 Implementation Steps

1. Installed and updated Kali Linux VM.
2. Installed Cowrie honeypot and configured Python virtual environment.
3. Modified cowrie.cfg to simulate a real SSH/Telnet server.
4. Applied iptables rules to redirect traffic from ports 22/23 to Cowrie.
5. Started Cowrie using Twisted.
6. Logged attacker connections, attempted commands, and login attempts.
7. Simulated brute-force attacks using Hydra and Medusa.
8. Analyzed captured logs in var/log/cowrie/.
9. Visualized results (IP origins, commands, attack frequency).
10. Stopped Cowrie and secured environment.

---

## 📊 Results & Findings
- **Login Attempts:** Multiple brute-force attempts captured using common usernames and passwords (`root`, `admin`, `123456`).
- **Commands Executed by Attackers:** 
  - `uname -a`
  - `cat /etc/passwd`
  - `wget malicious.sh`
- **Attack Sources:** Multiple IPs across different geolocations.
- **Defense Action:** Fail2ban and iptables rules applied to block persistent attackers.

---

## 📸 Evidence
- Logs: /home/kali/Honeypot/var/log/cowrie/
- Sample screenshots: docs/screenshots/

---

## 🛡️ Security Notes
- Honeypots should never be deployed in production.
- Always run Cowrie as a **non-root user**.
- Use isolated VMs to ensure attacks don’t affect real systems.

---

## 📜 References
- Cowrie GitHub: https://github.com/cowrie/cowrie
- Project Documentation (PDF): docs/Honeypot Server Setup.pdf
