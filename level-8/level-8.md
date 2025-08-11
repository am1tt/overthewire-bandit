## 🎯 Bandit Level 8 → Level 9

**Level Goal:**
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once
---

### 🧰 Commands You Might Need
`grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd`

---

### 🧭 Steps

1. 🔍 **Explore files**
   ```bash
   ls -al
   ```
    you will find **data.txt** containing strings 

2. 📄 **use sort to list out sorted list**
   ```bash
   sort data.txt 
   ```
    turns out it is sorted , but the strings are alot fo read manually 

3. 🦄 **Use UNIQ with flag -c**
   ```bash
   sort data.txt | uniq -c
   ```
    -c is a flag of uniq to give count of occurence , whils sorting using a **pipe grep**
    copy the flag with 1 occurance 

---

### 🔑 Password for Next Level
```
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```

## 💡 Notes
* Learned how to use uniq and its flag also using a man page of it 
* Learned how to sort the strings using sort 
* Learned to refine the use of pipe grep `|`
