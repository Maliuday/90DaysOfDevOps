# Linux Practice - Processes and Services

## Process Checks

### Command 1

```bash
ps aux | head
```

### Output

(Add your actual output here)

### Command 2

```bash
pgrep sshd
```

### Output

(Add your actual output here)

---

## Service Checks

### Command 3

```bash
systemctl status ssh
```

### Observation

* Service status: Active/Inactive
* Main PID:
* Loaded:

### Command 4

```bash
systemctl list-units --type=service
```

### Observation

* Verified running services on the system.

---

## Log Checks

### Command 5

```bash
journalctl -u ssh --no-pager | tail -10
```

### Observation

* Checked recent SSH service logs.

### Command 6

```bash
tail -n 20 /var/log/syslog
```

### Observation

* Reviewed latest system log entries.

---

## Mini Troubleshooting

Service Checked: SSH

Steps Performed:

1. Verified process using pgrep.
2. Checked service status using systemctl.
3. Reviewed logs using journalctl.
4. Confirmed service is running correctly.

## What I Learned

* How to inspect running processes.
* How to verify service health using systemctl.
* How to check logs for troubleshooting.
* Basic Linux troubleshooting workflow.
