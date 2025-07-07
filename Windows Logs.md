# Windows Directory Structure

| Folder                         | Purpose                                                             |
| ------------------------------ | ------------------------------------------------------------------- |
| `C:\Windows`                   | Contains OS system files, DLLs, drivers, kernel, WinSxS, etc.       |
| `C:\Program Files`             | Default install location for 64-bit programs                        |
| `C:\Program Files (x86)`       | Default install location for 32-bit programs on 64-bit systems      |
| `C:\Users`                     | Stores user profiles and their data (Desktop, Documents, Downloads) |
| `C:\ProgramData`               | Hidden folder used by apps to store shared data/settings            |
| `C:\$Recycle.Bin`              | System recycle bin (deleted files go here)                          |
| `C:\System Volume Information` | Used by System Restore and shadow copies (protected)                |

| Subfolder   | Description                                                                     |
| ----------- | ------------------------------------------------------------------------------- |
| `System32`  | Core 64-bit system files (DLLs, EXEs, drivers)                                  |
| `SysWOW64`  | 32-bit compatibility layer on 64-bit systems                                    |
| `WinSxS`    | Windows Side-by-Side assemblies, holds all OS versions                          |
| `Temp`      | Temporary files for Windows processes                                           |
| `Fonts`     | Installed system fonts                                                          |
| `Resources` | Sounds, themes, icons                                                           |
| `Logs`      | OS-level logs                                                                   |
| `Prefetch`  | Startup and application cache (used to speed up boot)                           |


| Pref Logs                                                             | Typical Log Files & Paths (Windows / Linux)                                                                                                                              |
| --------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| System crashed, network disconnected, drive corrupted, high CPU usage | Windows: Event Viewer (System.evtx), Minidump, Netsh logs, Disk and Perf logs; Linux: /var/log/syslog, /var/log/kern.log, /var/log/NetworkManager/, dmesg, smartctl logs |

| File Name      | Purpose                                          |
| -------------- | ------------------------------------------------ |
| `ntoskrnl.exe` | Windows NT kernel, controls hardware interaction |
| `explorer.exe` | Windows Explorer UI (taskbar, start menu)        |
| `winlogon.exe` | Manages login and user sessions                  |
| `lsass.exe`    | Security and authentication                      |
| `smss.exe`     | Session manager subsystem                        |
| `csrss.exe`    | Client/server runtime subsystem                  |
| `pagefile.sys` | Paging file for virtual memory                   |
| `hiberfil.sys` | Stores system state during hibernation           |


|Purpose|Path|
|---|---|
|**Windows Setup Logs**|`C:\Windows\Panther\`|
|**CBS Logs (SFC/Updates)**|`C:\Windows\Logs\CBS\CBS.log`|
|**DISM Logs**|`C:\Windows\Logs\DISM\dism.log`|
|**Windows Update Logs**|`C:\Windows\WindowsUpdate.log` _(older versions)_|
|**Firewall Logs**|`C:\Windows\System32\LogFiles\Firewall\pfirewall.log`|
|**Group Policy Logs**|`C:\Windows\Debug\UserMode\`|
|**Driver Install Logs**|`C:\Windows\inf\setupapi.dev.log`|
|**Windows Defender Logs**|`%ProgramData%\Microsoft\Windows Defender\`|

|Log File|Purpose|
|---|---|
|`CBS.log`|Shows what `sfc /scannow` or update installs do|
|`dism.log`|Logs DISM operations (cleanup, image repair)|
|`setupapi.dev.log`|Driver install failures|
|`pfirewall.log`|Firewall activity (blocked/allowed packets)|
|`WindowsUpdate.log`|Logs update attempts (converted from ETL files)|
|`Windows Defender\*.log`|Threat detection and scan reports|

|Type|Path|
|---|---|
|**Audit Logs**|`C:\Windows\System32\winevt\Logs\Security.evtx`|
|**Firewall Logs**|`C:\Windows\System32\LogFiles\Firewall\pfirewall.log`|
|**Defender Logs**|`%ProgramData%\Microsoft\Windows Defender\Support\`|
|**BitLocker Logs**|`C:\Windows\Logs\BitLocker\BitLockerEventLog.etl` (if enabled)|

|App/Service|Log Path Example|
|---|---|
|**IIS Web Server**|`C:\inetpub\logs\LogFiles\W3SVC1\`|
|**SQL Server**|`C:\Program Files\Microsoft SQL Server\...\LOG\`|
|**VPN Software**|`C:\ProgramData\YourVPNName\Logs\`|
|**Antivirus Logs**|`C:\ProgramData\Kaspersky Lab\` (varies by AV vendor)|

|Tool|Description|
|---|---|
|**Event Viewer**|View `.evtx` files (built-in)|
|**Notepad++**|For viewing `.log` and `.txt` files|
|**Log Parser Studio**|Advanced log search and visualization|
|**PowerShell**|Use `Get-WinEvent`, `Get-EventLog`, etc.|
|**ELK / Splunk**|In enterprise/SOC setups for centralized logging|


---
