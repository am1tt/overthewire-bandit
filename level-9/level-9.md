## 🎯 Bandit Level 9 → Level 10

**Level Goal:**
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

---

### 🧰 Commands You Might Need
`grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

---

### 🧭 Steps

1. 🔍 **Explore files**
   ```bash
   ls -alp
   ```
> as the file (data.txt) is in binary

2. 📄 **Getting the password**
   ```bash
   strings data.txt | grep "=="
   ```
> you will get the password 

---

### 🔑 Password for Next Level
```
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```

## 💡 Notes : 
* revised to use strings and grep 
