# Linux Commands Cheat Sheet

## Process Management

| Command     | Usage                        |
| ----------- | ---------------------------- |
| ps aux      | Show all running processes   |
| top         | Monitor CPU and memory usage |
| htop        | Interactive process viewer   |
| pidof nginx | Get process ID               |
| kill PID    | Terminate a process          |
| kill -9 PID | Force kill a process         |
| pkill nginx | Kill process by name         |
| jobs        | Show background jobs         |
| bg          | Run job in background        |
| fg          | Bring job to foreground      |

---

## File System Commands

| Command               | Usage                        |
| --------------------- | ---------------------------- |
| pwd                   | Show current directory       |
| ls -la                | List files with details      |
| cd directory          | Change directory             |
| mkdir test            | Create directory             |
| rm file.txt           | Delete file                  |
| rm -rf folder         | Delete directory recursively |
| cp file1 file2        | Copy file                    |
| mv old new            | Move or rename file          |
| find / -name file.txt | Search file                  |
| df -h                 | Check disk usage             |
| du -sh folder         | Check folder size            |

---

## Networking Commands

| Command                 | Usage                   |
| ----------------------- | ----------------------- |
| ping google.com         | Check connectivity      |
| ip addr                 | View IP address         |
| curl https://google.com | Test web endpoint       |
| dig google.com          | DNS lookup              |
| nslookup google.com     | Query DNS server        |
| traceroute google.com   | Trace network path      |
| netstat -tulnp          | View listening ports    |
| ss -tulnp               | Show active connections |
| hostname -I             | Show system IP          |
| wget URL                | Download file from URL  |

---

## Log & Service Commands

| Command                 | Usage                  |
| ----------------------- | ---------------------- |
| journalctl -xe          | View system logs       |
| tail -f /var/log/syslog | Monitor log file       |
| systemctl status nginx  | Check service status   |
| systemctl restart nginx | Restart service        |
| systemctl enable nginx  | Enable service at boot |

---

## My Most Used Commands

1. ls -la
2. pwd
3. ps aux
4. top
5. ping
6. curl
7. journalctl
8. systemctl status
9. df -h
10. find

## Summary

This cheat sheet contains commonly used Linux commands for process management, file system operations, networking troubleshooting, logging and service management. These commands are essential for daily DevOps and system administration tasks.
