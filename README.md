
---

# 🌍 Linux Administration & DevOps Automation Handbook

This project provides a **real-time, production-ready Linux Administration & Automation setup**, organized across **three levels** — Basic, Intermediate, and Advanced.

It serves as a complete guide for DevOps engineers working with Linux servers, covering:

🧩 Server setup
🔐 Security hardening
⚙️ Automation with shell scripts
📁 File system & permission management
📊 Monitoring & troubleshooting
🔥 Production-ready configurations (systemd, firewall, logrotate, SSH)


---

# 📂 Folder Structure

```
linux-handbook/
│
├── README.md
│
├── level-1-basic/
│   ├── users/
│   │   ├── create_users.sh
│   │   └── sudoers/
│   │       └── alice-dev
│   ├── permissions/
│   │   └── setup_project_dirs.sh
│   └── packages/
│       └── install_packages.sh
│
├── level-2-intermediate/
│   ├── cron/
│   │   ├── backup_myapp.sh
│   │   ├── cleanup_logs.sh
│   │   ├── app_health.sh
│   │   └── crontab_examples.txt
│   ├── logs/
│   │   └── log_management_notes.md
│   └── monitoring/
│       └── monitoring_commands.md
│
└── level-3-advanced/
    ├── systemd/
    │   ├── myapp.service
    │   └── start.sh
    ├── ssh-hardening/
    │   ├── sshd_config_changes.txt
    │   └── add_authorized_key.sh
    ├── lvm/
    │   └── lvm_setup_commands.sh
    ├── firewall/
    │   ├── ufw_rules.sh
    │   └── nftables_rules.sh
    └── logrotate/
        └── myapp.logrotate
```

---

# 🧩 Level 1 – Basic (Foundational Linux Administration)

### 👤 Users & Groups
- **Create users & groups** → [create_users.sh](./level-1-basic/users/create_users.sh)
- **Sudoers example** → [alice-dev](./level-1-basic/users/sudoers/alice-dev)

### 📂 Directory Permissions
- **Setup project directories** → [setup_project_dirs.sh](./level-1-basic/permissions/setup_project_dirs.sh)

### 📦 Package Installation
- **Install Git, Nginx, Java** → [install_packages.sh](./level-1-basic/packages/install_packages.sh)

---

# 🧱 Level 2 – Intermediate (Daily DevOps Operations)

### ⏱ Cron Jobs & Automation
- **Backup script** → [backup_myapp.sh](./level-2-intermediate/cron/backup_myapp.sh)
- **Log cleanup** → [cleanup_logs.sh](./level-2-intermediate/cron/cleanup_logs.sh)
- **Application health check** → [app_health.sh](./level-2-intermediate/cron/app_health.sh)
- **Crontab examples** → [crontab_examples.txt](./level-2-intermediate/cron/crontab_examples.txt)

### 📑 Log Management
- **Understanding /var/log** → [log_management_notes.md](./level-2-intermediate/logs/log_management_notes.md)

### 📊 System Monitoring
- **Troubleshooting commands** → [monitoring_commands.md](./level-2-intermediate/monitoring/monitoring_commands.md)

---

# 🔥 Level 3 – Advanced (Production-Ready Linux Administration)

### ⚙️ Systemd Service
- **Systemd unit file** → [myapp.service](./level-3-advanced/systemd/myapp.service)
- **App startup script** → [start.sh](./level-3-advanced/systemd/start.sh)

### 🔐 SSH Hardening
- **Secure SSH configurations** → [sshd_config_changes.txt](./level-3-advanced/ssh-hardening/sshds_config_changes.txt)
- **Add authorized SSH key** → [add_authorized_key.sh](./level-3-advanced/ssh-hardening/add_authorized_key.sh)

### 💾 LVM Storage
- **LVM setup commands** → [lvm_setup_commands.sh](./level-3-advanced/lvm/lvm_setup_commands.sh)

### 🔥 Firewall Rules
- **UFW firewall rules** → [ufw_rules.sh](./level-3-advanced/firewall/ufw_rules.sh)
- **nftables rules** → [nftables_rules.sh](./level-3-advanced/firewall/nftables_rules.sh)

### 🌀 Log Rotation
- **Logrotate config** → [myapp.logrotate](./level-3-advanced/logrotate/myapp.logrotate)

---

# ⚙️ How to Run Scripts

Make a script executable:

```bash
chmod +x script.sh
```

Run:

```bash
./script.sh
```

---

# 📌 GitHub Upload Steps

Push this assignment to your **linux-handbook** branch:

```bash
git checkout linux-handbook
git add .
git commit -m "Added Linux handbook with scripts and documentation"
git push origin linux-handbook
```

---

# 🧠 Useful Linux Commands

| Purpose               | Command                    |
| --------------------- | -------------------------- |
| Check disk usage      | `df -h`                    |
| Check memory usage    | `free -m`                  |
| Check CPU load        | `top`, `htop`              |
| View open ports       | `ss -tulnp`                |
| List running services | `systemctl --type=service` |
| Logs                  | `journalctl -xe`           |

---


# 👨‍💻 Author

**Sahith**
DevOps Engineer | Linux 
