#Linux-Handbook
---
#  Folder Structure & Hyperlinks
## **Level 1 – Basic (Foundational Linux Admin)**
###  Users & Groups
- [create_users.sh](level-1-basic/users/create_users.sh)
- Sudoers:
  - [alice-dev](level-1-basic/users/sudoers/alice-dev)
###  Directory Permissions
- [setup_project_dirs.sh](level-1-basic/permissions/setup_project_dirs.sh)
###  Package Installation
- [install_packages.sh](level-1-basic/packages/install_packages.sh)
---
## **Level 2 – Intermediate (Daily DevOps Tasks)**
###  Cron Jobs / Automation
- [backup_myapp.sh](level-2-intermediate/cron/backup_myapp.sh)
- [cleanup_logs.sh](level-2-intermediate/cron/cleanup_logs.sh)
- [app_health.sh](level-2-intermediate/cron/app_health.sh)
- [crontab_examples.txt](level-2-intermediate/cron/crontab_examples.txt)
###  Log Management
- [log_management_notes.md](level-2-intermediate/logs/log_management_notes.md)
###  Monitoring Commands
- [monitoring_commands.md](level-2-intermediate/monitoring/monitoring_commands.md)
---
## **Level 3 – Advanced (Production-Ready Setup)**
###  Systemd Service
- [myapp.service](level-3-advanced/systemd/myapp.service)
- [start.sh](level-3-advanced/systemd/start.sh)
###  SSH Hardening
- [sshd_config_changes.txt](level-3-advanced/ssh-hardening/sshd_config_changes.txt)
- [add_authorized_key.sh](level-3-advanced/ssh-hardening/add_authorized_key.sh)
###  LVM Storage Management
- [lvm_setup_commands.sh](level-3-advanced/lvm/lvm_setup_commands.sh)
###  Firewall Rules
- UFW Rules → [ufw_rules.sh](level-3-advanced/firewall/ufw_rules.sh)
- nftables Rules → [nftables_rules.sh](level-3-advanced/firewall/nftables_rules.sh)
###  Log Rotation
- [myapp.logrotate](level-3-advanced/logrotate/myapp.logrotate)
---
