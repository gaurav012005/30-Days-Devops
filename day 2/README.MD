
# 🚀 Day 2 – linux

## 🧠 Focus: Linux, Ubuntu CLI & WSL (Windows Subsystem for Linux)

---

## 🔍 Why Linux is Essential for DevOps Engineers

Linux is the **core of modern DevOps**. Here's why every DevOps engineer must master it:

- 🐧 **Most DevOps tools run natively on Linux** (Docker, Kubernetes, Jenkins, etc.)
- ☁️ **Cloud servers (AWS, Azure, GCP)** usually run Ubuntu or Debian
- 🔧 **Automation via Shell scripting** is Linux-native (Bash)
- 🔐 **Security, Permissions, Networking** control is CLI-driven
- 💡 **Performance and simplicity** of Linux make it ideal for DevOps tasks

---

## 💻 Installing Ubuntu on Windows using WSL

### 🛠️ Step 1: Enable WSL

Open **PowerShell as Administrator** and run:

```bash
wsl --install
````

If this fails (older Windows):

```bash
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

➡️ **Restart your computer after running above.**

---

### 🏬 Step 2: Install Ubuntu from Microsoft Store

1. Open Microsoft Store 🛍️
2. Search **Ubuntu 22.04 LTS**
3. Click **Install** and **Launch**
4. Set your **Linux username and password**

---

### 🧪 Step 3: Verify WSL Version

```bash
wsl --list --verbose
```

✅ Ensure version is **2**, or convert:

```bash
wsl --set-version Ubuntu 2
```

---

### 🔄 Step 4: Update Ubuntu and Install Basic Tools

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install curl wget git nano htop unzip -y
```

---

## 🧑‍💻 Ubuntu CLI – Essential Commands

### 📂 Navigation

| Task              | Command    |
| ----------------- | ---------- |
| Current directory | `pwd`      |
| List files        | `ls -la`   |
| Change directory  | `cd /home` |
| Go back           | `cd ..`    |

---

### 📝 File & Directory Operations

| Task          | Command                  |
| ------------- | ------------------------ |
| Create file   | `touch file.txt`         |
| Create folder | `mkdir folder`           |
| Copy file     | `cp file1.txt file2.txt` |
| Move file     | `mv file.txt /folder/`   |
| Delete file   | `rm file.txt`            |

---

### 🔍 View/Edit Files

| Task           | Command         |
| -------------- | --------------- |
| View content   | `cat file.txt`  |
| Scroll content | `less file.txt` |
| Edit (basic)   | `nano file.txt` |

---

### 🔐 Permissions and Ownership

| Task             | Command                     |
| ---------------- | --------------------------- |
| View permissions | `ls -l`                     |
| Make executable  | `chmod +x script.sh`        |
| Change owner     | `chown user:group file.txt` |

🧮 Linux Permission Structure:

```
-rwxr-xr--  (owner | group | others)
```

---

### 📦 APT Package Management (Ubuntu/Debian)

| Task            | Command                  |
| --------------- | ------------------------ |
| Update index    | `sudo apt update`        |
| Upgrade system  | `sudo apt upgrade`       |
| Install package | `sudo apt install nginx` |
| Remove package  | `sudo apt remove nginx`  |

---

### 📊 System Monitoring & Networking

| Task              | Command         |
| ----------------- | --------------- |
| CPU/RAM Usage     | `top` or `htop` |
| Disk usage        | `df -h`         |
| Memory usage      | `free -m`       |
| Running processes | `ps aux`        |
| Uptime            | `uptime`        |

---

## ✅  Tasks

Try these hands-on commands 👇

```bash
# Create folder
mkdir devops-day2
cd devops-day2

# Create and write to file
echo "Linux is essential for DevOps" > summary.txt

# Make it executable
chmod +x summary.txt

# Create new user and assign ownership
sudo adduser devopsuser
sudo chown devopsuser:devopsuser summary.txt
```

---

