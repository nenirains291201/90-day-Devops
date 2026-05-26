# Linux Practice

---

# Process Checks

## Command 1

```bash
ps aux | head
```

Output:

```bash
```   sandbox@playground:~$ ps
    PID TTY          TIME CMD
     13 pts/1    00:00:00 bash
     50 pts/1    00:00:00 ps

Observation:

- Shows currently running processes
- Displays PID, CPU, and memory usage

---

## Command 2

```bash
top
```

Output:

```bash
```

Observation:

- Displays live system performance
- Shows CPU and RAM usage

---

# Service Checks

## Command 3

```bash
systemctl list-units --type=service
```

Output:

```bash
```

Observation:

- Lists active system services

---

## Command 4

```bash
systemctl status ssh
```

Output:

```bash
```

Observation:

- SSH service status checked
- Service is active/running

---

# Log Checks

## Command 5

```bash
journalctl -u ssh --since today
```

Output:

```bash
```

Observation:

- Displays SSH service logs
- Used for troubleshooting

---

## Command 6

```bash
tail -n 20 /var/log/syslog
```

Output:

```bash
```

Observation:

- Shows recent system log entries

---

# Mini Troubleshooting Steps

1. Checked running processes using `ps` and `top`
2. Verified SSH service status
3. Viewed SSH logs using `journalctl`
4. Checked system logs using `tail`
5. No major errors found

---

# Summary

- Practiced Linux process monitoring
- Practiced systemd service inspection
- Practiced basic log troubleshooting
- Learned how to inspect service health and logs