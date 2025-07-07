# ⚙️ **Process & System Monitoring Commands**



### 🔍 `ps`

- **Meaning**: Shows **current processes** running in the current shell/session.
    
- **Example**:
    
    ```bash
    ps
    ```
    
    Output (example):
    
    ```
      PID TTY          TIME CMD
     2142 pts/0    00:00:00 bash
     2301 pts/0    00:00:00 ps
    ```
    

---

### 📋 `ps -ef`

- **Meaning**: Shows **all running processes** with full details.
    
- **Real-Life Use**: Monitor what's running in background/server.
    
- **Example**:
    
    ```bash
    ps -ef
    ```
    

---

### 📊 `ps aux`

- **Meaning**: Another format to show **all system processes**.
    
- **Purpose**: Preferred by many for easy filtering.
    
- **Example**:
    
    ```bash
    ps aux
    ```
    

---

### 🔍 `ps -ef | grep -i "firefox"`

- **Meaning**: Filters for any process related to **Firefox**.
    
- **Purpose**: Find specific programs running.
    
- **Example**:
    
    ```bash
    ps -ef | grep -i "firefox"
    ```
    

---

### ❌ `kill PID`

- **Meaning**: Kills (ends) a process by its **Process ID (PID)**.
    
- **Purpose**: Close apps that are frozen or misbehaving.
    
- **Example**:
    
    ```bash
    kill 2301
    ```
    

---

### 🤖 `obi`

- **Note**: Possibly a typo or custom command — no standard `obi` in Linux.
    
- If you meant something else (like `ob` or `obx`), let me know.
    

---

### ⏸️ `jobs`

- **Meaning**: Shows **background or suspended jobs** in your shell.
    
- **Example**:
    
    ```bash
    jobs
    ```
    
    Output:
    
    ```
    [1]+  Stopped                 gedit file1.txt
    ```
    

---

### ▶️ `%fg` or `%[1]`

- **Meaning**: Resumes a **paused (stopped) job** in the foreground.
    
- **Example**:
    
    ```bash
    %1
    ```
    
    or
    
    ```bash
    fg
    ```
    

---

### ⏳ `uptime`

- **Meaning**: Shows how **long the system has been running**, with load average.
    
- **Example**:
    
    ```bash
    uptime
    ```
    
    Output:
    
    ```
    22:44:15 up  5:45,  2 users,  load average: 0.03, 0.05, 0.01
    ```
    

---

### 🛣️ `route`

- **Meaning**: Displays or modifies the **IP routing table**.
    
- **Purpose**: Helps configure how your system sends/receives network traffic.
    
- **Example**:
    
    ```bash
    route
    ```
    

---

### 📡 `ss`

- **Meaning**: Shows active **network sockets** (like netstat but faster).
    
- **Use**: View open ports, established connections.
    
- **Example**:
    
    ```bash
    ss -tuln
    ```
    

---

### 🔐 `sshd`

- **Meaning**: The **OpenSSH Daemon**, responsible for SSH server-side connection.
    
- **Purpose**: Runs in the background to allow secure remote login.
    
- **Real-Life Use**: Must be running for others to SSH into your machine.
    

---

### 📤 `scp`

- **Meaning**: Securely **copies files** between systems via SSH.
    
- **Example**:
    
    ```bash
    scp file.txt user@192.168.1.10:/home/user/
    ```
    

---

### 📈 `iptraf`

- **Meaning**: Real-time **network traffic monitor** (colorful and interactive).
    
- **Example**:
    
    ```bash
    sudo iptraf
    ```
    

---

### 🌐 `iftop`

- **Meaning**: Live **bandwidth usage viewer** for network interfaces.
    
- **Example**:
    
    ```bash
    sudo iftop
    ```
    

---

### 📂 `lsof -i :80`

- **Meaning**: Lists open files or programs using **port 80** (typically HTTP).
    
- **Purpose**: Check if a port is in use and by which process.
    
- **Example**:
    
    ```bash
    sudo lsof -i :80
    ```
    

---


