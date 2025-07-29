## 🎯 Bandit Level 1 → Level 2

**Level Goal**:  
The password for the next level is stored in a file called `readme` located in the home directory. Use this password to log into `bandit1` using SSH (port `2220`).

---

### 🛠️ Commands You May Need  
```bash
ls
cd
cat
file
du
find
```
---


### ✅ Solution

🔎 Step 1: List files in the directory
```ls -alp```
📄 Step 2: Read the contents of the file

```cat ./-```
The file is named -, so you have to use ./- to avoid confusion with command-line flags.
---

### 🔐 Password Retrieved

[anyStringndginwginx02]

### 💡 Notes
    Files starting with - can be tricky. Use ./ prefix to tell the shell it's a file, not a flag.