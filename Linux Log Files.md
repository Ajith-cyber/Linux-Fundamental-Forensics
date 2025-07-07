#  Linux Log Files – Paths, Directory Structure & Types

---

## **Where Are Linux Logs Stored?**

###  Most Linux log files live under:

```
/var/log/
```

This is the central directory for logs on almost all Linux distros.

---

##  **Key Log Files and Their Purpose**

| Log File Name          | Path                  | Purpose / Contents                          |
|-----------------------|-----------------------|---------------------------------------------|
| `syslog` or `messages`| `/var/log/syslog` or `/var/log/messages` | General system activity and messages (daemon startup, shutdowns, kernel logs) |
| `auth.log` or `secure`| `/var/log/auth.log` (Debian/Ubuntu) or `/var/log/secure` (RedHat/CentOS) | Authentication logs: login attempts, sudo usage, ssh logins |
| `kern.log`            | `/var/log/kern.log`    | Kernel messages and events                    |
| `dmesg`               | `/var/log/dmesg`       | Kernel ring buffer messages (boot logs)      |
| `boot.log`            | `/var/log/boot.log`    | Boot process logs                             |
| `daemon.log`          | `/var/log/daemon.log`  | System daemon logs                            |
| `cron.log`            | `/var/log/cron.log` or `/var/log/cron` | Cron job activity                             |
| `apt/`                | `/var/log/apt/`        | Apt package manager logs (install, upgrade) |
| `yum.log`             | `/var/log/yum.log`     | Yum package manager logs (RedHat-based)      |
| `Xorg.0.log`          | `/var/log/Xorg.0.log`  | X server logs (GUI issues)                    |
| `faillog`             | `/var/log/faillog`     | Failed login attempts                         |
| `lastlog`             | `/var/log/lastlog`     | Records last login of each user               |
| `httpd/` or `apache2/`| `/var/log/httpd/` or `/var/log/apache2/` | Apache web server access and error logs       |
| `mysql/` or `mariadb/`| `/var/log/mysql/`      | MySQL/MariaDB logs                            |

---

##  **Log File Structure**

- Mostly **plain text** files, readable by editors like `cat`, `less`, `tail`, or `vim`.
- Format varies, but generally includes:
  - Timestamp
  - Hostname or service name
  - Log level (info, error, warning)
  - Message content

Example from `/var/log/auth.log`:
```
Jul  7 10:30:01 servername sshd[1234]: Accepted password for user from 192.168.1.100 port 53422 ssh2
```

---

##  **Special Logs & Binary Logs**

- `dmesg` output is also accessible via the `dmesg` command (kernel buffer).
- Some systems use **binary journald logs** managed by `systemd-journald`:

### Journal Logs:
- Location: `/run/log/journal/` or `/var/log/journal/`
- Use command:  
  ```bash
  journalctl
  ```
- Logs system, kernel, services, with powerful filtering options.

---

##  **Log Rotation**

Logs can get huge, so Linux uses **logrotate** to compress and archive old logs.

- Configuration: `/etc/logrotate.conf` and `/etc/logrotate.d/`
- Old logs are typically renamed with suffixes like `.1`, `.2.gz`, etc.
  Example:
  ```
  /var/log/syslog
  /var/log/syslog.1
  /var/log/syslog.2.gz
  ```

---

##  **Accessing Logs**

- View last 100 lines of syslog:
  ```bash
  tail -n 100 /var/log/syslog
  ```
- Follow live updates:
  ```bash
  tail -f /var/log/auth.log
  ```
- View journal logs:
  ```bash
  journalctl -xe
  ```

---

##  **Summary Table**

| Log Type           | File/Directory Path           | Notes/Use Case                       |
|--------------------|------------------------------|------------------------------------|
| System messages    | `/var/log/syslog` or `/var/log/messages` | General system info and errors     |
| Authentication     | `/var/log/auth.log` or `/var/log/secure` | Logins, sudo, ssh attempts         |
| Kernel             | `/var/log/kern.log`           | Kernel events                      |
| Boot               | `/var/log/boot.log`           | Boot-time logs                    |
| Package manager    | `/var/log/apt/` or `/var/log/yum.log` | Package installs/updates          |
| Cron jobs          | `/var/log/cron.log`           | Scheduled jobs                    |
| Web server         | `/var/log/apache2/` or `/var/log/httpd/` | Apache web server logs            |
| Database           | `/var/log/mysql/`             | MySQL/MariaDB logs                |

---
