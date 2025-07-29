## 🎯 Bandit Level 4 → Level 5


**Level Goal:**
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.
---

### 🧰 Commands You Might Need
`ls`, `cd`, `cat`, `file`, `du`, `find`

---

### 🧭 Steps

1. 🔍 **Explore files**
   ```bash
   ls -al
   ```

2. 💱 **Change Directory**
   ```bash
   cd ./inhere
   ```
> you will notice there are mutiple files here , but only one contains password 

3. 👁️ **use Find to get human redeable file**
> tip : use `man xargs` to get more detailed commands 

   ```bash 
   find . -type f | xargs file 
   ```
> turns out -file07 is : ASCII text so its human redeable and contains pass

4. 💥 **Cat the -file07**
   ```bash 
   cat ./-file07
   ```

---

### 🔑 Password for Next Level
```
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```

## 💡Notes 
* learned how to use `find` and also using `xargs` with `type f` for human redeable or more 
verbose output

* Learned how to there can be many different files stored and not a single file each time , during CTF'S