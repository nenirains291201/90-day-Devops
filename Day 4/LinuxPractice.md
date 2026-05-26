# Linux Practice

---

# Process Checks

## Command 1

```bash
ps aux | head
```

Output:

``` sandbox@playground:~$ ps
    PID TTY          TIME CMD
     13 pts/1    00:00:00 bash
     50 pts/1    00:00:00 ps
```  
Observation:

- Shows currently running processes
- Displays PID, CPU, and memory usage

---

## Command 2

```bash
top
```

Output:

```
top - 17:32:15 up 11 days,  6:45,  0 users,  load average: 0.24, 0.08, 0.02
Tasks:   3 total,   1 running,   2 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.4 us,  0.3 sy,  0.0 ni, 99.3 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
MiB Mem :  32096.1 total,  29063.0 free,    841.3 used,   2191.7 buff/cache
MiB Swap:      0.0 total,      0.0 free,      0.0 used.  30835.2 avail Mem 

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND                                                                       
      1 sandbox   20   0    4628   3684   3236 S   0.0   0.0   0:00.02 bash                                                                          
     13 sandbox   20   0    4628   3816   3204 S   0.0   0.0   0:00.08 bash                                                                          
     52 sandbox   20   0    7312   3468   2916 R   0.0   0.0   0:00.01 top
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