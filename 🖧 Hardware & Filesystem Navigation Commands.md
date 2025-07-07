# 🖧 **Hardware & Filesystem Navigation Commands**



### 📁 `/` — Root Directory

- **Meaning**: The **top-level directory** in Linux. All folders and files start from here.
    
- **Purpose**: Think of it as the "main gate" or starting point of everything in Linux.
    
- **Real-Life Use**: System-level files like `/etc`, `/bin`, `/home` all live here.
    
- **Example**:  
    When you run:
    
    ```bash
    cd /
    ls
    ```
    
    You’ll see:
    
    ```
    bin  boot  dev  etc  home  lib  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
    ```
    

---

### 🏠 `~` — Home Directory

- **Meaning**: Shortcut to the current user's personal folder.
    
- **Purpose**: It's where your personal files, settings, downloads, etc. are stored.
    
- **Real-Life Use**: You’ll be here by default when you open terminal.
    
- **Example**:
    
    ```bash
    cd ~
    pwd
    ```
    
    Output:
    
    ```
    /home/joy
    ```
    

---

### 🧭 `cd Co*`

- **Meaning**: `cd` changes the current directory. Using `Co*` means match anything starting with "Co".
    
- **Purpose**: Navigate quickly using **wildcards**.
    
- **Real-Life Use**: Saves time. Example, `cd Co*` matches "Code", "Config", etc.
    
- **Example**:
    
    ```bash
    cd Co*
    ```
    
    If a folder named **Code** exists, it enters that directory.
    

---

### 📍 `pwd`

- **Meaning**: Stands for **Print Working Directory**.
    
- **Purpose**: Tells you where you are inside the system.
    
- **Example**:
    
    ```bash
    pwd
    ```
    
    Output:
    
    ```
    /home/joy/Documents/Projects
    ```
    

---

### 📂 `ls -l`

- **Meaning**: Lists files and folders in **long format**.
    
- **Purpose**: Shows details like size, permissions, owner, date, etc.
    
- **Example**:
    
    ```bash
    ls -l
    ```
    
    Output:
    
    ```
    -rw-r--r-- 1 joy joy   129 Jul 5 22:00 notes.txt
    drwxr-xr-x 2 joy joy  4096 Jul 4 18:00 Code/
    ```
    

---

### 🕵️ `touch .filename`

- **Meaning**: Creates a **hidden file** (starts with a dot).
    
- **Purpose**: Hidden files usually store config or secret info.
    
- **Example**:
    
    ```bash
    touch .secretfile
    ls
    ```
    
    Output:  
    File won’t show. To view:
    
    ```bash
    ls -a
    ```
    

---

### 🔍 `ls -la`

- **Meaning**: Lists **all files** (including hidden) in **long format**.
    
- **Purpose**: Useful when you want to inspect all content in a folder.
    
- **Example**:
    
    ```bash
    ls -la
    ```
    
    Output:
    
    ```
    drwxr-xr-x 3 joy joy 4096 Jul 5 22:30 .
    drwxr-xr-x 6 joy joy 4096 Jul 5 20:00 ..
    -rw-r--r-- 1 joy joy    0 Jul 5 22:00 .secretfile
    ```
    

---

### 📤 `echo "zesu" > filename.txt`

- **Meaning**: Sends text `"zesu"` into a new file.
    
- **Purpose**: Quickly create files with content.
    
- **Example**:
    
    ```bash
    echo "zesu" > file1.txt
    cat file1.txt
    ```
    
    Output:
    
    ```
    zesu
    ```
    

---

### 📚 `ls -lah`

- **Meaning**: Combines `ls -l`, `-a`, and `-h` for **long format, all files, human-readable size**.
    
- **Example**:
    
    ```bash
    ls -lah
    ```
    
    Output:
    
    ```
    -rw-r--r-- 1 joy joy 2.5K Jul 5 22:30 .hiddenlog
    ```
    

---

### 🧽 `rm`

- **Meaning**: Deletes (removes) a file.
    
- **Caution**: No recycle bin! Once deleted = gone.
    
- **Example**:
    
    ```bash
    rm file1.txt
    ```
    

---

### 💣 `rm -rf filename`

- **Meaning**: Removes folder/file **recursively and forcefully**.
    
- **Purpose**: Deletes folders with files without asking.
    
- **Example**:
    
    ```bash
    rm -rf myfolder
    ```
    
- **⚠️ Warning**: Dangerous. Double-check path before using!
    

---

### 🎨 `lsd`

> _(If installed)_

- **Meaning**: An enhanced version of `ls` with colors, icons.
    
- **Example**:
    
    ```bash
    lsd
    ```
    

---

### 🌳 `lsd --tree --depth 1`

- **Meaning**: Tree view of files/folders up to 1 level deep.
    
- **Purpose**: Visual directory structure.
    
- **Example**:
    
    ```bash
    lsd --tree --depth 1
    ```
    

---

### 🌲 `lsd --tree --depth 2`

- **Meaning**: Same as above, but shows subfolders up to 2 levels.
    
- **Great For**: Project organization previews.
    

---

### ⚡ `fastfetch`

- **Meaning**: Displays **stylized system info** (OS, CPU, RAM, etc.).
    
- **Real-Life Use**: Cool overview, often used in screenshots or blogs.
    
- **Example**:
    
    ```bash
    fastfetch
    ```
    

---

### 📊 `htop`

- **Meaning**: Visual real-time **process monitor**.
    
- **Purpose**: Check CPU, RAM, processes — interactive.
    
- **Example**:
    
    ```bash
    htop
    ```
    

---

### 💹 `btop --utf-force`

- **Meaning**: Enhanced `htop` with UI/graph support.
    
- **Example**:
    
    ```bash
    btop --utf-force
    ```
    

---

### 🧠 `free -h`

- **Meaning**: Displays memory usage in human-readable form.
    
- **Purpose**: Know how much RAM is used/free.
    
- **Example**:
    
    ```bash
    free -h
    ```
    
    Output:
    
    ```
                  total        used        free
    Mem:           7.7G        2.5G        4.2G
    ```
    

---

### 🔌 `lsusb -tv`

- **Meaning**: Shows USB devices connected in **tree view**.
    
- **Purpose**: Useful for checking external devices (mouse, USB stick).
    
- **Example**:
    
    ```bash
    lsusb -tv
    ```
    

---

### 💻 `cat /proc/cpuinfo`

- **Meaning**: Displays **CPU details**.
    
- **Example**:
    
    ```bash
    cat /proc/cpuinfo
    ```
    

---

### 🧮 `cat /proc/meminfo`

- **Meaning**: Displays detailed **memory stats** (more than `free`).
    
- **Use**: Deep memory analysis.
    

---

### 📈 `mpstat 1`

- **Meaning**: Shows **CPU usage per second**.
    
- **Example**:
    
    ```bash
    mpstat 1
    ```
    

---

### 📊 `vmstat 1`

- **Meaning**: Reports system performance (CPU, memory, I/O).
    
- **Example**:
    
    ```bash
    vmstat 1
    ```
    

---

