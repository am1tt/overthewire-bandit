## 🎯 Bandit Level 10 → Level 11
**Level Goal:**
The password for the next level is stored in the file data.txt, which contains base64 encoded data

---

### 🧰 Commands You Might Need
`grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`



---

### 🧭 Steps

1. 🔍 **Explore files**
   ```bash
   ls -alp
   ```
> tip : use man page for base64
2. 📄 **decode the file using base64**
   ```bash
   base64 -d data.txt 
   ```
 -d stands for decode
  you will get the password 

---

### 🔑 Password for Next Level
```
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```

## 💡 Notes 
* learned how to use base64 
* learned how to use its flags (options)
* understanding various ways to CTF