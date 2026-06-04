# Day 07 - Linux File System Hierarchy & Scenario Practice

# Part 1: Linux File System Hierarchy

## /

Root directory is the starting point of the Linux file system. All files and directories originate from here.

I would use this when navigating the Linux file system.

---

## /home

Contains personal directories for normal users.

Example folders seen:

* user
* ubuntu

I would use this when managing user files.

---

## /root

Home directory of the root user.

Contains administrative files and configurations.

I would use this when performing system administration tasks.

---

## /etc

Stores system-wide configuration files.

Examples:

* hostname
* hosts
* ssh

I would use this when modifying service configurations.

---

## /var/log

Stores application and system log files.

Examples:

* syslog
* auth.log
* journal

I would use this when troubleshooting system issues.

---

## /tmp

Stores temporary files.

Files may be removed automatically after reboot.

I would use this when testing scripts or temporary data.

---

## /bin

Contains essential Linux command binaries.

Examples:

* ls
* cp
* mv

I would use this when running basic Linux commands.

---

## /usr/bin

Contains user-level executable programs.

Examples:

* vim
* python3
* curl

I would use this when working with installed applications.

---

## /opt

Stores third-party applications.

Examples:

* custom software
* vendor packages

I would use this when installing optional software.

---

# Hands-On Practice

## Largest Log Files

```bash
du -sh /var/log/* 2>/dev/null | sort -h | tail -5
```

Observation:
Identified the largest log files consuming disk space.

---

## Hostname Check

```bash
cat /etc/hostname
```

Observation:
Verified system hostname.

---

## Home Directory Check

```bash
ls -la ~
```

Observation:
Reviewed files and hidden configuration files.

---

# Part 2: Scenario-Based Practice

## Scenario 1 - Service Not Starting

### Step 1

```bash
systemctl status myapp
```

Why:
Check whether the service is failed, inactive, or running.

### Step 2

```bash
journalctl -u myapp -n 50
```

Why:
Review recent service logs.

### Step 3

```bash
systemctl is-enabled myapp
```

Why:
Verify if service starts automatically after reboot.

### Step 4

```bash
systemctl restart myapp
```

Why:
Attempt service restart after reviewing logs.

---

## Scenario 2 - High CPU Usage

### Step 1

```bash
top
```

Why:
Monitor live CPU usage.

### Step 2

```bash
ps aux --sort=-%cpu | head -10
```

Why:
Find top CPU-consuming processes.

### Step 3

```bash
pgrep process_name
```

Why:
Get the PID of a process.

### Step 4

```bash
ps -p PID -o pid,ppid,%cpu,%mem,cmd
```

Why:
Inspect detailed process information.

---

## Scenario 3 - Finding Service Logs

### Step 1

```bash
systemctl status docker
```

Why:
Verify service health.

### Step 2

```bash
journalctl -u docker -n 50
```

Why:
View recent service logs.

### Step 3

```bash
journalctl -u docker -f
```

Why:
Follow logs in real time.

---

## Scenario 4 - File Permission Issue

### Step 1

```bash
ls -l /home/user/backup.sh
```

Why:
Check current permissions.

### Step 2

```bash
chmod +x /home/user/backup.sh
```

Why:
Grant execute permission.

### Step 3

```bash
ls -l /home/user/backup.sh
```

Why:
Verify execute permission is added.

### Step 4

```bash
./backup.sh
```

Why:
Run the script again.

---

# What I Learned

* Linux file system hierarchy is important for troubleshooting.
* Logs are commonly found under /var/log.
* Configuration files are stored in /etc.
* Troubleshooting should follow a step-by-step approach instead of guessing.
* systemctl and journalctl are essential DevOps commands.
