
## 🎯 Bandit Level 5 → Level 6


**Level Goal:**
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

human-readable
1033 bytes in size
not executable
---

### 🧰 Commands You Might Need
`ls`, `cd`, `cat`, `file`, `du`, `find`

---

### 🧭 Steps

1. 🔍 **Explore files**
   ```bash
   ls -al
   ```

2. 👽 **Change Directory to inhere**
   ```bash
   ls -alp 
   cd ./inhere 
   ```

3. 👁️ **use Find to get the file , with some flags mentioned**
   ```bash 
   find . -type f -size 1033c ! -executable
   ```

4. 🙃 **Cat the file you found in the result** 
  ```bash 
  cat ./maybhere07/.file2
  ```
---

### 🔑 Password for Next Level
```
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```

## 💡Notes 
* Learned how to use different flags mentioned such as , `size` , `executables` 
* `c` after 1033 is `bytes`
* `!` is used to denote the executable mentioned 
