
# 🐧 Linux Server Health Monitoring System

A hands-on Linux system administration project built using Bash scripting to automate essential server health checks, monitor resource utilization, identify resource-intensive processes, and generate timestamp-based monitoring logs.

## 🎯 Project Overview

The objective of this project is to simplify routine Linux server health checks by automating system information collection and resource monitoring through a Bash script.

The script monitors essential system resources, identifies potential disk and memory utilization issues, and generates a daily health monitoring report.

## 🚀 Key Features

- **Server Information:** Collects hostname and system uptime.
- **Disk Monitoring:** Monitors root filesystem disk utilization.
- **Memory Monitoring:** Calculates RAM utilization percentage.
- **CPU Load Monitoring:** Collects 1-minute, 5-minute, and 15-minute load averages.
- **Process Monitoring:** Identifies the top 5 CPU-consuming processes.
- **Threshold-Based Warnings:** Generates warnings when disk usage reaches 80% or memory usage reaches 85%.
- **Timestamp-Based Logging:** Records monitoring results with date and time.
- **Automated Log Management:** Creates log directories and daily log files automatically.

## 🛠️ Technologies & Tools Used

- Ubuntu Linux (WSL2)
- Bash Scripting
- Git & GitHub

### Linux Commands Used

| Command | Purpose |
|---|---|
| `hostname` | Retrieves server hostname |
| `uptime` | Checks system uptime |
| `df` | Monitors disk utilization |
| `free` | Retrieves memory information |
| `awk` | Extracts and processes command output |
| `ps` | Displays running processes |
| `head` | Displays top process entries |
| `tee` | Displays and appends log output |
| `date` | Generates timestamps |

## 📂 Project Structure

```text
linux-health-monitor/
│
├── logs/
│   └── health-YYYY-MM-DD.log
│
├── health-monitor.sh
│
└── README.md
```

## ⚙️ Installation & Execution

### 1. Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
```

### 2. Navigate to the Project Directory

```bash
cd linux-health-monitor
```

### 3. Give Execution Permission

```bash
chmod +x health-monitor.sh
```

### 4. Execute the Monitoring Script

```bash
./health-monitor.sh
```

## 📊 Sample Output

```text
========== SERVER HEALTH CHECK STARTED ==========

Hostname: ubuntu-server
Uptime: up 5 days, 3 hours

Disk Usage: 70%
OK: Disk utilization normal.

Memory Usage: 50%
OK: Memory utilization normal.

CPU Load Average: 0.45 0.60 0.75

Top 5 CPU-consuming processes:

PID   COMMAND   %CPU   %MEM
1234  python    35.2    5.5
2345  java      20.1   15.0

========== SERVER HEALTH CHECK COMPLETED ==========

Monitoring completed successfully!
```

*Note: Sample values are illustrative. Actual output depends on system resources and running processes.*

## 📝 Log Management

The script automatically creates a `logs` directory and generates a separate log file for each day.

Example:

```text
logs/health-YYYY-MM-DD.log
```

To view the daily monitoring report:

```bash
cat logs/health-$(date +%F).log
```

## 📚 Key Learnings

Through this project, I gained practical experience in:

- Linux command-line operations and system administration.
- Bash scripting, variables, functions, and conditional statements.
- Disk and memory resource monitoring.
- Linux process identification and monitoring.
- Text processing using AWK.
- Log generation and basic troubleshooting.
- Automating repetitive system health checks.

## 🔮 Future Improvements

- CPU utilization percentage monitoring.
- Automated monitoring using Cron.
- Email or notification alerts for critical resource utilization.
- Monitoring multiple filesystems.
- Improved error handling and monitoring reports.

## 👨‍💻 Author

Developed as a hands-on learning project to strengthen Linux system administration, infrastructure monitoring, and DevOps fundamentals.

**Technologies:** Linux | Bash | Git | GitHub

