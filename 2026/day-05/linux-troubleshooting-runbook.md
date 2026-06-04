# Linux Troubleshooting Runbook

## Target Service

Service Selected: SSH

---

## Environment Basics

### Command

```bash
uname -a
```

### Observation

System kernel and architecture information verified.

### Command

```bash
cat /etc/os-release
```

### Observation

Verified Linux distribution and version.

---

## Filesystem Sanity Check

### Command

```bash
mkdir /tmp/runbook-demo
cp /etc/hosts /tmp/runbook-demo/hosts-copy
ls -l /tmp/runbook-demo
```

### Observation

Successfully created test directory and copied file.

---

## CPU & Memory Snapshot

### Command

```bash
free -h
```

### Observation

Checked available and used memory.

### Command

```bash
top -bn1 | head -15
```

### Observation

Verified CPU utilization and top running processes.

---

## Disk & IO Snapshot

### Command

```bash
df -h
```

### Observation

Disk usage is within acceptable limits.

### Command

```bash
du -sh /var/log
```

### Observation

Checked log directory size.

---

## Network Snapshot

### Command

```bash
ss -tulpn
```

### Observation

Verified listening ports and active services.

### Command

```bash
ping -c 4 google.com
```

### Observation

Network connectivity is working properly.

---

## Logs Reviewed

### Command

```bash
journalctl -u ssh -n 20 --no-pager
```

### Observation

Reviewed recent SSH service logs. No critical errors found.

### Command

```bash
systemctl status ssh
```

### Observation

SSH service is active and running successfully.

---

## Quick Findings

* SSH service is running normally.
* System memory usage is healthy.
* Disk usage is under control.
* Network connectivity is available.
* No critical errors observed in logs.

---

## If This Worsens

1. Restart the SSH service and monitor logs.
2. Increase log collection and review journal entries.
3. Use advanced tools such as strace, vmstat, and tcpdump for deeper troubleshooting.
