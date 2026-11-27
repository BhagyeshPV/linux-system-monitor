# 🖥️ Linux Server Health Check & System Monitor

![Bash](https://img.shields.io/badge/Bash-Scripting-green?logo=gnu-bash)
![RHEL](https://img.shields.io/badge/RHEL-7%2F8%2F9%2F10-red)
![Ubuntu](https://img.shields.io/badge/Ubuntu-20.04%2F22.04%2F24.04-orange)
![CentOS](https://img.shields.io/badge/CentOS-7%2F8%2F9%2F10-red)
![SUSE](https://img.shields.io/badge/SUSE-12%2F15%2F16-red)

A lightweight, dependency-free Bash utility designed for **L2/L3 Linux Administrators and Site Reliability Engineers** 
to rapidly audit server health, resource utilization, top processes, and OS patch compliance across enterprise Linux distributions.

---
## 📌 Business Problem

In enterprise environments, Linux administrators manage multiple servers supporting business-critical applications.
Manual health checks require administrators to log in to individual servers and run several commands to collect system information.

This approach leads to:

- Increased troubleshooting effort
- Delayed incident resolution
- Inconsistent health assessments
- Risk of missing performance bottlenecks
- Reduced operational efficiency
---
## 🎯 Objectives

The project aims to:

- Automate Linux server health checks
- Standardise monitoring procedures
- Reduce manual troubleshooting effort
- Improve visibility into system performance
- Identify capacity issues proactively
- Generate consolidated health reports
- Support production operations teams
---

## 🚀 Features

* **System & Kernel Identification  :** Displays hostname, OS release (`PRETTY_NAME`), kernel version, architecture, uptime, and last reboot timestamp.
* **CPU & Load Diagnostics          :** Reports core count, CPU model, real-time CPU utilization percentage, and 1/5/15-minute load averages.
* **Memory & Disk Utilization       :** Summarizes RAM/Swap consumption (`free -h`) and mounted filesystem usage (`df -hP`).
* **Top Resource Consumers          :** Lists the top 5 running processes by CPU and Memory footprint.
* **Multi-Distro Patch Audit        :** Automatically detects package manager logs across **RHEL/CentOS (`yum`/`dnf`)**, **SUSE Linux (`zypper`)**, and **Debian/Ubuntu (`apt`)** to verify the most recent OS patch/update timestamp.
* **Automated Health Threshold Alerts:** Flags warnings if CPU (>80%), Memory (>80%), or Disk (>85%) thresholds are breached.

---

## 🛠️ Supported Distributions

* Red Hat Enterprise Linux (RHEL 7 / 8 / 9) & CentOS / Rocky / AlmaLinux
* SUSE Linux Enterprise Server (SLES 12 / 15) & openSUSE
* Ubuntu & Debian

---
## 📋 Quick Start & Usage

1. **Clone the repository:**
   ```bash
   # git clone https://github.com
   # cd linux-system-monitor
   # cd script
   ```

2. **Make the script executable:**
   ```bash
   # chmod +x system_monitor.sh
   ```

3. **Run the health check:**
   ```bash
   # ./system_monitor.sh
   ```

*(Optional)* Schedule via `cron` to log daily health reports:
```bash
0 8 * * * /path/to/system_monitor.sh >> /var/log/server_health.log 2>&1
```

---

## 📊 Sample Output

```text
╔════════════════════════════════════════════╗
║     Linux Server Health Check Report       ║
║       Generated: 2026-09-01 08:00          ║
╚════════════════════════════════════════════╝

--- SYSTEM DETAILS ---
Hostname (Server Name): prod-app-01
Operating System:       Red Hat Enterprise Linux 9.4 (Plow)
Kernel Version:         5.14.0-427.el9.x86_64
Architecture:           x86_64
System Uptime Details:  up 42 days, 6 hours, 15 minutes

--- SYSTEM HEALTH SUMMARY ---
Memory Usage: 44%
CPU Usage:    12%

✓ Memory Usage is Normal (44%)
✓ CPU Usage is Normal (12%)
✓ All Disk Partitions are Below 85% Threshold
```

---

## ⚠️ Professional Disclaimer
This repository contains a self-developed Linux monitoring solution created as part of a personal technical portfolio.

While the design is inspired by real-world Linux administration and infrastructure operations practices, the implementation, code, documentation, and examples have been independently created and do not contain any proprietary information, confidential business data, customer information, or intellectual property from any current or former employer.

This project is intended exclusively to showcase technical skills in Linux Administration, Shell Scripting, System Monitoring, Troubleshooting, and Infrastructure Automation.

---

## 👤 Author
**Bhagyesh Prakash Vanarse**  
Senior Infrastructure Consultant | Linux Lead | DevOps  
🔗 [LinkedIn] - https://www.linkedin.com/in/bhagyeshv-devopslinux/

