## 🎯 Bandit Level 12 → Level 13

**Level Goal:**  
The password for the next level is stored in the file `data.txt`, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under `/tmp` in which you can work. Use `mkdir` with a hard to guess directory name. Or better, use the command `mktemp -d`. Then copy the datafile using `cp`, and rename it using `mv` (read the manpages!)

---

### 🧰 Commands You Might Need
`grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`, `mkdir`, `cp`, `mv`, `file`

---

### 🧭 Steps

## make dir
`mkdir /tmp/am1t`

## copy data.txt to created directory
`cp data.txt /tmp/am1t`

## reverse hex dump using xxd
`xxd -r data.txt > data`

## check the file type of data
`file data`  
> you will get that its gzip compressed

## change extension before using gzip to decompress
`mv data file.gz`

## decompress gzip
`gzip -d file.gz`

## check the file type
`file file`  
> now you will get that its bzip2 compressed

## change extension to bz2
`mv file file.bz2`

## decompress bz2
`bzip2 -d file.bz2`

## check the file type
`file file`  
> now you will see gzip again

## change extension and decompress gzip
`mv file file.gz`  
`gzip -d file.gz`

## check the file type
`file file`  
> now you will get POSIX tar archive

## change to .tar and extract
`mv file file.tar`  
`tar xf file.tar`

## check contents
`ls`  
> you will get `data5.bin` (tar again)

## change extension and extract tar
`mv data5.bin data.tar`  
`tar xf data.tar`

## check with file
`file data6.bin`  
> it’s bzip2 compressed

## change extension and decompress bz2
`mv data6.bin data.bz2`  
`bzip2 -d data.bz2`

## check file type
`file file`  
> it’s tar archive again

## extract tar
`mv file file.tar`  
`tar xf file.tar`

## check contents
`ls`  
> now you get `data8.bin` which is gzip

## change extension and decompress gzip
`mv data8.bin data.gz`  
`gzip -d data.gz`

## check file type
`file data`  
> now it is ASCII text

## view the password
`cat data`

---

### 🔑 Password for Next Level
```
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```

---

## 💡 Notes
* Learned how the decompression works  
* Understood patience is key, not just quick flags  
* Learned various decompression techniques and how to identify them  
* Learned extension changing and how to utilize it  
* Explored gzip, tar, bz2 and their usage  
* A very long lab — taught patience and persistence
