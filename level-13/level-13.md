## 🎯 Bandit Level 13 → Level 14

**Level Goal:**  
The password for the next level is stored in `/etc/bandit_pass/bandit14` and can only be read by user **bandit14**. For this level, you don’t get the next password directly, but you get a private SSH key that can be used to log into the next level.  
Note: `localhost` is a hostname that refers to the machine you are working on.

---

### 🧰 Commands You Might Need
`ssh`, `telnet`, `nc`, `openssl`, `s_client`, `nmap`

---

### 🧭 Steps

#### 📂 List files
`ls`  
> you will find `sshkey.private`

#### 🔑 Use the SSH key to login
`ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220`

#### 🚪 Logged into bandit14
> Now you are inside bandit14

#### 📄 Check password file
`cat /etc/bandit_pass/bandit14`

---

### 🔑 Password for Next Level
```
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
```

---

## 💡 Notes
* Learned how to use a private SSH key for authentication  
* Understood the use of `-i` flag in ssh  
* Explored the concept of accessing restricted files as a different user  
