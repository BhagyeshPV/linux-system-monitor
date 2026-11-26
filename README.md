# 🖥️ Linux Server Health Check & System Monitor

A lightweight, dependency-free Bash utility designed for **L2/L3 Linux Administrators and Site Reliability Engineers** 
to rapidly audit server health, resource utilization, top processes, and OS patch compliance across enterprise Linux distributions.

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
║          Generated: 2026-09-01 08:00       ║
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

## 👤 Author
**Bhagyesh Prakash Vanarse**  
Senior Infrastructure Consultant | Linux Lead | DevOps  
🔗 [LinkedIn] - https://www.linkedin.com/in/bhagyeshv-devopslinux/

