## 📁 **File Handling & Utilities**

---

### 🔍 `awk`

- **Meaning**: A tool for **searching and processing text line-by-line**.
    
- **Purpose**: Extract or format text from files and command outputs.
    
- **Real-Life Use**: Pick specific columns from a log or CSV.
    
- **Example**:
    
    ```bash
    awk '{print $1}' file.txt
    ```
    
    👉 Prints the **first word** of each line from `file.txt`.
    

---

### ⚖️ `cmp` – Compare 2 Files

- **Meaning**: Compares two files **byte by byte**.
    
- **Purpose**: Check if two files are **exactly the same**.
    
- **Example**:
    
    ```bash
    cmp file1.txt file2.txt
    ```
    
    Output if same:  
    _(no output – means identical)_  
    Output if different:
    
    ```
    file1.txt file2.txt differ: byte 15, line 1
    ```
    

---

### 🔤 `sort`

- **Meaning**: Sorts lines in text files alphabetically or numerically.
    
- **Purpose**: Organize data neatly.
    
- **Example**:
    
    ```bash
    sort names.txt
    ```
    

---

### 🔢 `wc`, `wc -l`, `wc -c`

- **Meaning**: Counts **lines**, **words**, and **characters**.
    
- **Purpose**: Get stats on file size or contents.
    
- **Examples**:
    
    ```bash
    wc file.txt       # lines, words, characters
    wc -l file.txt    # lines only
    wc -c file.txt    # character count
    ```
    

---

### 🔍 `look`

- **Meaning**: Finds words in a file that **start with a given string**.
    
- **Purpose**: Quick dictionary-style lookup.
    
- **Example**:
    
    ```bash
    look comp
    ```
    
    Output:
    
    ```
    compact
    compare
    compile
    ```
    

---

### 🔎 `find`

- **Meaning**: Searches for **files and folders**.
    
- **Purpose**: Locate anything, anywhere in the system.
    
- **Example**:
    
    ```bash
    find /home -name "*.txt"
    ```
    

---

### 📦 `gzip`

- **Meaning**: Compresses a file into `.gz` format.
    
- **Purpose**: Save disk space.
    
- **Example**:
    
    ```bash
    gzip file.txt
    ```
    
    Creates `file.txt.gz`.
    

---

### 🗃️ `gunzip filename`

- **Meaning**: Decompresses a `.gz` file.
    
- **Purpose**: Get original file back.
    
- **Example**:
    
    ```bash
    gunzip file.txt.gz
    ```
    

---

### 📂 `open .`

- **Meaning**: Opens the current folder in GUI (macOS/Linux with GUI).
    
- **Example**:
    
    ```bash
    open .
    ```
    
    _(In GNOME, you may use: `xdg-open .`)_
    

---

### 🔍 `locate`

- **Meaning**: Instantly finds file paths by name.
    
- **Purpose**: Much faster than `find`.
    
- **Example**:
    
    ```bash
    locate file.txt
    ```
    

---

### 🖥️ `tmux`

- **Meaning**: Terminal multiplexer – run **multiple terminal sessions** in one window.
    
- **Real-Life Use**: Useful on remote servers.
    
- **Example**:
    
    ```bash
    tmux
    ```
    

---

### 💻 `cmatrix`

- **Meaning**: Fun command that shows **Matrix-style green falling code**.
    
- **Just for fun** 😄
    
- **Example**:
    
    ```bash
    cmatrix
    ```
    

---
