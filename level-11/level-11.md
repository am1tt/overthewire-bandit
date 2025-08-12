## 🎯 Bandit Level 11 → Level 12

**Level Goal:**
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

---

### 🧰 Commands You Might Need
`ep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

---

### 🧭 Steps

1. 🔍 **Explore files**
   ```bash
   ls -alp
   ```
- you will get data.txt but its rotated
2. 📄 **Rotate the file using ROT13 (13 index)**
   ```bash
   cat data.txt | tr A-Za-z N-ZA-Mn-za-m
   ```
   
> this rotates the N-Z (13) to first section of 13 and the others of A-M (12) to right side of 13 , making it a ROT(13)

> you will get the password correctly rotated now 
---

### 🔑 Password for Next Level
```
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```


## 💡 Notes : 
* Learned how to use `tr`
* Learned new about concept of ROT13
* Learned how to rotate the strings chars 
