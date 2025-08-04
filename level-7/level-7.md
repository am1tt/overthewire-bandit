
## 🎯 Bandit Level 7 → Level 8 

**Level Goal:**
The password for the next level is stored in the file data.txt next to the word millionth

---

### 🧰 Commands You Might Need
`man, grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd`

---

### 🧭 Steps

1. 🔍 **Explore files**
   ```bash
   ls -alp
   ```
   you will find a data.txt file

2. 📄 **Read target file**
   ```bash
   cat data.txt
   ```
   its filled with multiple strings , which makes harder to find the flag

3. 🧛 **getting the flag with strings and grep**
   ```bash 
   strings data.txt | grep "millionth"
   ```
   as it consist of strings , and grep will find the word "millionth" mentioned you will get the flag
---

### 🔑 Password for Next Level
```
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```


## 💡Notes 
* learned and revised how to use `grep` and how important it is
* learned how to use `strings` as its new to me 
* learned how to handle txt filled with multiple strings 
* learned how we can use this in pentesting purposes to find such data or flags 
