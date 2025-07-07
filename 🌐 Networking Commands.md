# 🌐 **Networking Commands**



### 📡 `ifconfig`

- **Meaning**: Shows network interfaces (like Wi-Fi, Ethernet) and their IP addresses.
    
- **Purpose**: Check or configure your IP, MAC address, and active interfaces.
    
- **Real-Life Use**: Know your IP when troubleshooting internet issues.
    
- **Example**:
    
    ```bash
    ifconfig
    ```
    
    **Output** (example):
    
    ```
    wlan0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  
            inet 192.168.1.101  netmask 255.255.255.0  broadcast 192.168.1.255
    ```
    

---

### 📥 `tcpdump`

- **Meaning**: Captures **network traffic packets** going through your system.
    
- **Purpose**: Deep analysis for network issues, attacks, or debugging.
    
- **Example**:
    
    ```bash
    sudo tcpdump
    ```
    
    Shows live packet capture. Press `Ctrl + C` to stop.
    

---

### 📡 `sudo tcpdump -i wlan0/eth0`

- **Meaning**: Captures packets only on the **Wi-Fi (wlan0)** or **Ethernet (eth0)** interface.
    
- **Purpose**: Focus on a specific network source.
    
- **Example**:
    
    ```bash
    sudo tcpdump -i wlan0
    ```
    

---

### 🔐 `sudo tcpdump -i wlan0 'port 22'`

- **Meaning**: Captures only **SSH traffic (port 22)** on Wi-Fi interface.
    
- **Real-Life Use**: Monitor secure login sessions or check if SSH is working.
    
- **Example**:
    
    ```bash
    sudo tcpdump -i wlan0 'port 22'
    ```
    

---

### 🧑 `arp`

- **Meaning**: Displays the **Address Resolution Protocol** table.
    
- **Purpose**: Shows IP-to-MAC address mappings in your LAN.
    
- **Real-Life Use**: Debug local connectivity, especially static IP issues.
    
- **Example**:
    
    ```bash
    arp
    ```
    

---

### 📘 `resolvconf -u`

- **Meaning**: Refreshes DNS configuration.
    
- **Purpose**: Apply changes in `/etc/resolv.conf` (DNS resolver file).
    
- **Real-Life Use**: When DNS is not working after VPN or network change.
    
- **Example**:
    
    ```bash
    sudo resolvconf -u
    ```
    

---

### 🛰️ `mtr google.com`

- **Meaning**: A combo of `ping` and `traceroute`.
    
- **Purpose**: Diagnoses where a network issue is happening hop-by-hop.
    
- **Example**:
    
    ```bash
    mtr google.com
    ```
    

---

### 🔑 `ssh-keygen`

- **Meaning**: Generates **SSH key pairs** for secure login.
    
- **Purpose**: Used for passwordless SSH connections.
    
- **Real-Life Use**: Deploy servers, remote access without typing password every time.
    
- **Example**:
    
    ```bash
    ssh-keygen
    ```
    
    Follow the prompts to generate keys.
    

---

### 📶 `nmcli device wifi list`

- **Meaning**: Lists available Wi-Fi networks via terminal.
    
- **Purpose**: Useful when managing wireless networks through scripts or servers.
    
- **Example**:
    
    ```bash
    nmcli device wifi list
    ```
    

---

### 📊 `nload`

- **Meaning**: Real-time visual of **incoming/outgoing bandwidth usage**.
    
- **Purpose**: Instantly see how much network is being used.
    
- **Example**:
    
    ```bash
    nload
    ```
    

---

### 📡 `iperf`

- **Meaning**: Measures **network speed** between two systems.
    
- **Purpose**: Bandwidth and latency testing.
    
- **Use Case**: Compare Wi-Fi vs LAN speeds.
    
- **Example**:  
    On server:
    
    ```bash
    iperf -s
    ```
    
    On client:
    
    ```bash
    iperf -c 192.168.1.10
    ```
    

---

### 🎯 `fping`

- **Meaning**: Like `ping`, but can test **multiple IPs** at once.
    
- **Real-Life Use**: Check availability of a whole subnet quickly.
    
- **Example**:
    
    ```bash
    fping 192.168.1.1 192.168.1.2
    ```
    

---

### 🧭 `nmtui`

- **Meaning**: **Text-based UI** to configure networks (IP, Wi-Fi).
    
- **Purpose**: Easy for beginners and servers without GUI.
    
- **Example**:
    
    ```bash
    nmtui
    ```
    
    Use arrow keys and Enter to configure.
    

---

### 🆔 `id`

- **Meaning**: Displays **user ID (UID)** and **group ID (GID)** of the current or given user.
    
- **Purpose**: Check which groups a user belongs to.
    
- **Real-Life Use**: Useful when troubleshooting permission issues.
    
- **Example**:
    
    ```bash
    id
    ```
    
    **Output**:
    
    ```
    uid=1000(joy) gid=1000(joy) groups=1000(joy),27(sudo)
    ```
    

---

### 👥 `who`

- **Meaning**: Shows who is currently **logged into the system**.
    
- **Purpose**: Monitor active user sessions.
    
- **Example**:
    
    ```bash
    who
    ```
    
    **Output**:
    
    ```
    joy     tty1         2025-07-05 20:00
    admin   pts/0        2025-07-05 21:15 (192.168.1.20)
    ```
    

---

### 📜 `last`

- **(Already documented in System Section)**
    
- Shows **login/logout history** of users.
    

---

### ➕ `groupadd groupname`

- **Meaning**: Creates a **new group**.
    
- **Purpose**: Organize users with same permissions.
    
- **Real-Life Use**: Add developers to a `dev` group to manage shared files.
    
- **Example**:
    
    ```bash
    sudo groupadd devteam
    ```
    

---

### ➕ `useradd -c "" username`

- **Meaning**: Adds a new user with a comment (`-c`) to describe the user.
    
- **Purpose**: Create user accounts for different team members.
    
- **Example**:
    
    ```bash
    sudo useradd -c "Developer account" dev1
    ```
    

---

### 🔐 `usermod -aG root username`

- **Meaning**: Adds a user to a specific group (`-aG`), like `root` or `sudo`.
    
- **Purpose**: Give admin rights or group access to a user.
    
- **Real-Life Use**: Allow a new developer to install software.
    
- **Example**:
    
    ```bash
    sudo usermod -aG sudo dev1
    ```
    

---

### 📝 `gedit`

- **Meaning**: Launches the **GUI text editor** in Linux (like Notepad).
    
- **Purpose**: Open and edit files in a graphical interface.
    
- **Example**:
    
    ```bash
    gedit mynote.txt
    ```
    

---


### 🌐 `ifconfig -a`

- **Meaning**: Shows **all** network interfaces (active & inactive).
    
- **Purpose**: Full view of your network devices.
    
- **Example**:
    
    ```bash
    ifconfig -a
    ```
    

---

### ⚙️ `ethtool eth0`

- **Meaning**: Shows **hardware settings** of the Ethernet interface.
    
- **Purpose**: Check link speed, cable status.
    
- **Example**:
    
    ```bash
    sudo ethtool eth0
    ```
    

---

### 📶 `ethtool wlan0`

- **Same as above**, but for wireless interface.
    
- **Example**:
    
    ```bash
    sudo ethtool wlan0
    ```
    

---

### 📡 `ping`

- **Meaning**: Checks if a host (like a website or server) is reachable.
    
- **Purpose**: Basic **internet test**.
    
- **Example**:
    
    ```bash
    ping google.com
    ```
    

---

### 🌍 `whois google.com`

- **Meaning**: Shows domain info like owner, registrar, expiry.
    
- **Purpose**: Investigate websites or IP ownership.
    
- **Example**:
    
    ```bash
    whois google.com
    ```
    

---

### 🧠 `dig google.com`

- **Meaning**: DNS lookup – shows how your system finds the IP address.
    
- **Purpose**: Troubleshoot domain issues.
    
- **Example**:
    
    ```bash
    dig google.com
    ```
    

---

### 🔁 `dig -x 142.21.1.4`

- **Meaning**: **Reverse DNS lookup** – IP → Domain name.
    
- **Example**:
    
    ```bash
    dig -x 142.21.1.4
    ```
    

---

### 🔎 `nslookup`

- **Meaning**: Another DNS tool like `dig`.
    
- **Example**:
    
    ```bash
    nslookup google.com
    ```
    

---

### 📨 `host google.com`

- **Meaning**: Shows domain's IP, mail server (MX), and DNS.
    
- **Example**:
    
    ```bash
    host google.com
    ```
    

---

### 📊 `netstat -nul`

- **Meaning**: Shows **open UDP ports**.
    
- **Use**: Check what services are listening.
    
- **Example**:
    
    ```bash
    netstat -nul
    ```
    

---

### 🌐 `ftp ftp.server.com`

- **Meaning**: Connects to a remote **FTP server**.
    
- **Example**:
    
    ```bash
    ftp ftp.gnu.org
    ```
    

---

### 🔄 `tftp`

- **Meaning**: Lightweight version of FTP, used in embedded systems.
    
- **Example**:
    
    ```bash
    tftp
    ```
    

---

### 🔐 `sftp`

- **Meaning**: Secure File Transfer Protocol (over SSH).
    
- **Example**:
    
    ```bash
    sftp user@host
    ```
    

---

### 🧵 `telnet`

- **Meaning**: Connect to another computer via **terminal session**.
    
- **Use**: Used to test open ports.
    
- **Example**:
    
    ```bash
    telnet google.com 80
    ```
    

---

### 🌐 `curl`

- **Meaning**: Fetches data from a website via CLI.
    
- **Purpose**: API testing, downloading files.
    
- **Example**:
    
    ```bash
    curl https://example.com
    ```
    

---



