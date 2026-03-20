DevOps Environment Setup Assignment
📌 Project Overview

This project demonstrates the setup of a secure and monitored development environment for two developers (Sarah & Mike), including system monitoring, user management, and automated backup configuration.

🔹 Task 1: System Monitoring

Installed htop and nmon

Monitored CPU, Memory, Processes

Disk usage checked using df -h and du -sh

Logs monitored using journalctl

🔹 Task 2: User Management

Created users: sarah and mike

Set permissions using:

chmod 700 /home/user

Applied password policies using:

/etc/login.defs

chage

🔹 Task 3: Backup Configuration
Apache (Sarah)

Config: /etc/httpd

Web root: /var/www/html

Nginx (Mike)

Config: /etc/nginx

Web root: /usr/share/nginx/html

Backup Features

Automated using cron (Tuesday 12 AM)

Compressed using tar

Verified using:

tar -tzf file.tar.gz
⏰ Cron Job
0 0 * * 2 /usr/local/bin/web_backup.sh
📁 Backup Location
/backups/
