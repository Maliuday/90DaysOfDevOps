# Linux Architecture Notes

## 1. Core Components of Linux

### Kernel

* Kernel is the core of Linux.
* It manages CPU, Memory, Devices and Processes.
* Acts as a bridge between hardware and software.

### User Space

* Area where users and applications run.
* Programs cannot directly access hardware.
* Requests are sent to the kernel.

### Init / systemd

* First process started by Linux after booting.
* Process ID (PID) = 1
* Manages services and system startup.

---

## 2. Process Management

A process is a running instance of a program.

### Process States

* Running (R) – Process is currently executing.
* Sleeping (S) – Waiting for an event or resource.
* Stopped (T) – Process execution is paused.
* Zombie (Z) – Process has finished but still exists in process table.
* Waiting (D) – Waiting for I/O operations.

### Process Creation

* A process is created using fork().
* Parent process creates a child process.
* Each process gets a unique PID.

---

## 3. What is systemd?

systemd is the default service manager in most Linux distributions.

### Why systemd Matters

* Starts services during boot.
* Stops and restarts services.
* Manages system resources.
* Maintains logs through journald.

### Common systemd Commands

```bash
systemctl status nginx
systemctl start nginx
systemctl stop nginx
systemctl restart nginx
systemctl enable nginx
```

## 4. Five Daily Linux Commands

```bash
ps aux        # View running processes
top           # Monitor system resources
systemctl     # Manage services
journalctl    # View logs
kill -9 PID   # Terminate a process
```

## Summary

Linux consists of Kernel, User Space and systemd. Processes are managed using PIDs and different process states. systemd is responsible for booting and managing services, making it an essential tool for DevOps engineers.
