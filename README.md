Perfect. I will now **insert every script directly under each section** in your README — clean, simple, and perfect for live video demos.

Here is your **updated README with all scripts included**.

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

---

## 👤 Users & Groups

### 📌 Script: `create_users.sh`

```bash
#!/bin/bash

sudo groupadd devteam

for user in dev1 dev2 dev3; do
    sudo useradd -m -G devteam $user
    echo "User $user created and added to devteam"
done
```

### 📌 Sudoers Example (`alice-dev`)

```
alice ALL=(ALL) NOPASSWD: /usr/bin/systemctl restart nginx
```

---

## 📂 Directory Permissions

### 📌 Script: `setup_project_dirs.sh`

```bash
#!/bin/bash

sudo mkdir -p /project/app/{logs,config}

sudo groupadd projectgrp
sudo chgrp -R projectgrp /project/app

sudo chmod -R 770 /project/app
echo "Project directories configured."
```

---

## 📦 Package Installation

### 📌 Script: `install_packages.sh`

```bash
#!/bin/bash

sudo apt update -y
sudo apt install git nginx default-jdk -y

echo "Installed Git, Nginx, and Java."
```

---

# 🧱 Level 2 – Intermediate (Daily DevOps Operations)

---

## ⏱ Cron Jobs & Automation

### 📌 Script: `backup_myapp.sh`

```bash
#!/bin/bash

tar -czf /backups/myapp_$(date +%F).tar.gz /var/www/myapp
echo "Backup completed."
```

---

### 📌 Script: `cleanup_logs.sh`

```bash
#!/bin/bash

find /var/log/myapp/ -type f -mtime +7 -delete
echo "Old logs cleaned."
```

---

### 📌 Script: `app_health.sh`

```bash
#!/bin/bash

if systemctl is-active --quiet myapp; then
    echo "App is running."
else
    echo "App is DOWN!" | mail -s "myapp Alert" admin@example.com
fi
```

---

### 📌 Crontab Examples (`crontab_examples.txt`)

```
0 2 * * * /scripts/backup_myapp.sh
0 */6 * * * /scripts/app_health.sh
0 0 * * 0 /scripts/cleanup_logs.sh
```

---

## 📑 Log Management

### 📌 File: `log_management_notes.md`

```
Important log directories:
/var/log/syslog
/var/log/auth.log
/var/log/nginx/
/var/log/mysql/

Use journalctl for systemd:
journalctl -u nginx
journalctl -xe
```

---

## 📊 System Monitoring

### 📌 File: `monitoring_commands.md`

```
top
htop
vmstat
iostat
free -h
df -h
ss -tulnp
```

---

# 🔥 Level 3 – Advanced (Production-Ready Linux Administration)

---

## ⚙️ Systemd Service

### 📌 File: `myapp.service`

```
[Unit]
Description=My Application
After=network.target

[Service]
ExecStart=/usr/local/bin/start.sh
Restart=always
User=root

[Install]
WantedBy=multi-user.target
```

### 📌 Script: `start.sh`

```bash
#!/bin/bash
echo "Starting application..."
python3 /opt/myapp/app.py
```

---

## 🔐 SSH Hardening

### 📌 File: `sshd_config_changes.txt`

```
PermitRootLogin no
PasswordAuthentication no
AllowUsers dev1 dev2 sahith
```

### 📌 Script: `add_authorized_key.sh`

```bash
#!/bin/bash

USER=$1
mkdir -p /home/$USER/.ssh
cat key.pub >> /home/$USER/.ssh/authorized_keys

chmod 600 /home/$USER/.ssh/authorized_keys
chown -R $USER:$USER /home/$USER/.ssh
```

---

## 💾 LVM Storage

### 📌 Script: `lvm_setup_commands.sh`

```bash
pvcreate /dev/xvdb
vgcreate datavg /dev/xvdb
lvcreate -L 5G -n datalv datavg
mkfs.ext4 /dev/datavg/datalv
mount /dev/datavg/datalv /data
```

---

## 🔥 Firewall Rules

### 📌 Script: `ufw_rules.sh`

```bash
#!/bin/bash

ufw allow 22
ufw allow 80
ufw allow 443
ufw enable
```

---

### 📌 Script: `nftables_rules.sh`

```bash
#!/bin/bash
nft add table inet filter
nft add chain inet filter input { type filter hook input priority 0 ; }
nft add rule inet filter input tcp dport 22 accept
nft add rule inet filter input tcp dport 80 accept
```

---

## 🌀 Log Rotation

### 📌 Config: `myapp.logrotate`

```
/var/log/myapp/*.log {
    daily
    rotate 7
    compress
    missingok
}
```

---

# ⚙️ How to Run Scripts

```
chmod +x script.sh
./script.sh
```

---

# 📌 GitHub Upload Steps

```
git checkout linux-handbook
git add .
git commit -m "Added Linux handbook with scripts and documentation"
git push origin linux-handbook
```

---

# 🧠 Useful Linux Commands

| Purpose    | Command                    |
| ---------- | -------------------------- |
| Disk usage | `df -h`                    |
| Memory     | `free -m`                  |
| CPU load   | `top`, `htop`              |
| Ports      | `ss -tulnp`                |
| Services   | `systemctl --type=service` |
| Logs       | `journalctl -xe`           |

---

# 👨‍💻 Author

**Sahith**
DevOps Engineer | Linux

---

