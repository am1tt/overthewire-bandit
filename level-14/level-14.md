## 🎯 Bandit Level 14 → Level 15

**Level Goal:**  
The password for the next level can be retrieved by submitting the password of the current level to port **30000** on `localhost`.

---

### 🧰 Commands You Might Need
`ssh`, `telnet`, `nc`, `openssl`, `s_client`, `nmap`

---

### 🧭 Steps

## 📂 Explore
`ls`  
> Nothing useful here.

## 📄 Get the current level’s password
`cat /etc/bandit_pass/bandit14`  
(or use the password obtained after solving Level 13).

## 🔗 Submit password to localhost on port 30000
`nc localhost 30000`  
Paste the password with `Ctrl+Shift+V`, then press Enter.  
You will receive the next level’s password.

---

### 🔑 Password for Next Level
```
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```


---

## 💡 Notes
* Learned how to use `nc` (netcat) to send data over a port  
* Understood the concept of submitting current credentials to retrieve the next one  
* Important reminder: carefully read level descriptions to avoid confusion  
