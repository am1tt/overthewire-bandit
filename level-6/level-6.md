
## 🎯 Bandit Level 6 → Level 7


**Level Goal:**
The password for the next level is stored somewhere on the server and has all of the following properties:

owned by user bandit7
owned by group bandit6
33 bytes in size

---

### 🧰 Commands You Might Need
`ls`, `cd`, `cat`, `file`, `du`, `find` , `grep`

---

### 🧭 Steps

1. 🔍 **Explore files**
   ```bash
   ls -al
   ```


2. 👁️ **use Find to get the file , with some flags mentioned**
   ```bash 
   find / -type f -user bandit7 -group bandit6 -size 33c 
   ```

4. 👓 **alot of logs but you will see this log result** 
  ```bash 
  c/var/lib/dpkg/info/bandit7.password
  ```
5 😺 **Cat the path to get the password**
  ```bash 
  cat c/var/lib/dpkg/info/bandit7.password
  ```

---

### 🔑 Password for Next Level
```
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```

## 💡Notes 
* learned how to use / for paths based `find`
* revised the `find` command
* learned how to use flags such as `-user` and `-group` 
* revised again how to use `-size` with c bytes
