# 🐝 Honeypot Server Project

This project demonstrates how to set up a **Cowrie honeypot** on Kali Linux/Kali clone to simulate vulnerable SSH/Telnet services, capture attacker behavior, and analyze attack patterns.

---

## 📖 Documentation
The full step-by-step setup guide is included in:
- docs/Honeypot Server Setup.pdf

Screenshots of the environment, logs, and attack simulations are in:
- [`docs/screenshots/`](docs/screenshots/)

---

## ⚙️ Setup Instructions

### Prerequisites
- Kali Linux (or Kali clone VM)
- Python 3 with virtualenv
- Git
- VirtualBox or VMware

### Quick Install
Clone the repo and run the installer:
```bash
git clone https://github.com/<your-username>/honeypot-server.git
cd honeypot-server/setup
bash install.sh
