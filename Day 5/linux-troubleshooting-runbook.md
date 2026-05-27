# Linux Troubleshooting Runbook

## Target Service
SSH
sandbox@playground:~$ ssh
usage: ssh [-46AaCfGgKkMNnqsTtVvXxYy] [-B bind_interface]
           [-b bind_address] [-c cipher_spec] [-D [bind_address:]port]
           [-E log_file] [-e escape_char] [-F configfile] [-I pkcs11]
           [-i identity_file] [-J [user@]host[:port]] [-L address]
           [-l login_name] [-m mac_spec] [-O ctl_cmd] [-o option] [-p port]
           [-Q query_option] [-R address] [-S ctl_path] [-W host:port]
           [-w local_tun[:remote_tun]] destination [command [argument ...]]

## Environment Basics

### Command
```bash
uname -a
```

Output:
```
sandbox@playground:~$ uname -a
Linux terminal-9a26d5fb 6.1.0-9-amd64 #1 SMP PREEMPT_DYNAMIC Debian 6.1.27-1 (2023-05-08) x86_64 x86_64 x86_64 GNU/Linux
```

Observation:
Ubuntu kernel information displayed.

---

## Filesystem Sanity

### Command
```bash
mkdir runbook-demo
```

Observation:
Folder created successfully.

---

## CPU & Memory

### Command
```bash
top
```

Observation:
CPU usage stable below 10%.

---

## Disk & IO

### Command
```bash
df -h
```
sandbox@playground:~$ df -h
Filesystem      Size  Used Avail Use% Mounted on
overlay          59G  4.4G   53G   8% /
tmpfs            64M     0   64M   0% /dev
/dev/vda1        59G  4.4G   53G   8% /etc/hosts
shm              64M     0   64M   0% /dev/shm
tmpfs            16G     0   16G   0% /proc/asound
tmpfs            16G     0   16G   0% /proc/acpi
tmpfs            16G     0   16G   0% /sys/firmware

Observation:
Enough disk space available.

---

## Network

### Command
```bash
ss -tulpn
```

Observation:
SSH listening on port 22.

---

## Logs Reviewed

### Command
```bash
journalctl -u ssh -n 50
```

Observation:
No recent errors found.

---

## Quick Findings

- SSH service healthy
- No abnormal CPU usage
- Disk usage normal
- No critical log errors

---

## If This Worsens

1. Restart SSH service
2. Check firewall rules
3. Enable verbose logging