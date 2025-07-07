
## 🔐 1. **User Activity & History Forensics**

Track who did what, and when.

|Command|Purpose|Real-Life Use|
|---|---|---|
|`last`|See who logged in and when|Detect unauthorized access|
|`lastb`|See failed login attempts|Brute-force detection|
|`w` / `who`|Check active users|Identify suspicious sessions|
|`history`|View user’s command history|See what was executed|
|`utmpdump /var/log/wtmp`|Dump login records|Full login audit trail|

---

## 📂 2. **File Metadata & Timeline Analysis**

|Command|Purpose|Real-Life Use|
|---|---|---|
|`stat file.txt`|Shows access, modify, and change timestamps|Timeline reconstruction|
|`ls -lu`, `ls -lc`|Shows access/change time specifically|Find suspicious changes|
|`md5sum`, `sha256sum`|Create file hash|Detect tampering|
|`diff file1 file2`|Compare versions of a file|Spot unauthorized changes|
|`lsattr`|Check file attributes (e.g., immutable)|Detect hidden files|

---

## 💾 3. **File Recovery / Deleted File Tracing**

|Command|Purpose|Real-Life Use|
|---|---|---|
|`debugfs`|Forensic tool for ext filesystems|Recover deleted files manually|
|`extundelete`|Recover deleted files from ext3/ext4|Accident or malicious deletion|
|`testdisk`|Partition recovery|Disk corruption or tampering|

---

## 🧠 4. **Memory & Process Analysis**

|Command|Purpose|Real-Life Use|
|---|---|---|
|`ps aux`, `top`, `htop`|Check running processes|Detect malware or unusual apps|
|`lsof`|List open files & sockets|Catch hidden file usage|
|`vmstat`, `free`|See memory usage|Detect memory-based attacks|
|`volatility`|Analyze memory dumps|Full memory forensics (needs dump)|

---

## 📡 5. **Network Activity & Connections**

|Command|Purpose|Real-Life Use|
|---|---|---|
|`netstat -tulnp`, `ss -tulnp`|View open ports & listening services|Detect unauthorized servers|
|`tcpdump`|Capture network packets|Spy on network activity|
|`iftop`, `nethogs`|Bandwidth monitoring|Who’s using the network heavily|
|`nmap`|Scan ports & services|Discover exposed attack surfaces|

---

## 📜 6. **Log File Forensics**

|File/Command|Purpose|Real-Life Use|
|---|---|---|
|`/var/log/auth.log`|Authentication logs|Detect SSH brute-force|
|`/var/log/syslog`, `/var/log/messages`|General system logs|Detect system tampering|
|`journalctl`|View systemd logs|Complete system activity|
|`ausearch`, `auditctl`|Audit framework|Real-time policy & tracking|

---

## 🧩 7. **Rootkit & Malware Detection**

|Tool|Purpose|Real-Life Use|
|---|---|---|
|`chkrootkit`|Check for known rootkits|Common root-level malware|
|`rkhunter`|Scan for rootkits, backdoors|Automated integrity checks|
|`clamav`, `lynis`|Malware and system audit tools|Anti-malware from CLI|

---

## 🔍 8. **Hidden or Suspicious File Discovery**

|Command|Purpose|Real-Life Use|
|---|---|---|
|`find / -name ".*"`|Finds hidden files|Look for hidden backdoors|
|`du -sh *`|Check folder sizes|Spot hidden data hoarding|
|`strings`|Extract readable text from binaries|Analyze suspicious files|

---

## 🔐 9. **Secure File Timeline Tools**

- `log2timeline` (Plaso): Full timeline creation from system artifacts
    
- `Timesketch`: Visual interface for analyzing timeline (used with `log2timeline`)
    

---

## ✅ Tools You Should Install for Real-World Use

|Tool|Function|
|---|---|
|`Volatility`|Full memory forensics|
|`Autopsy` / `Sleuthkit`|Disk forensics|
|`Wireshark`|Network packet analysis|
|`Plaso` + `Timesketch`|Timeline creation|
|`TheHarvester`, `Maltego`|Info gathering (OSINT)|
