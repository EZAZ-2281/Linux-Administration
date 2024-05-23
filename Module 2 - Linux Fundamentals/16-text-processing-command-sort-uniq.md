# sort uniq

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 60
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria    0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 one
drwxr-xr-x 2 ikibria ikibria 4096 May 21 19:30 savar
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:34 japan
-rw-r--r-- 1 ikibria ikibria 8192 May 21 19:34 typescript
-rw-r--r-- 1 ikibria ikibria 9752 May 21 19:40 maintainence.log
drwxr-xr-x 2 ikibria ikibria 4096 May 22 10:06 folder-one
-rw-r--r-- 1 ikibria ikibria 5974 May 22 10:17 cut.log
-rw-r--r-- 1 ikibria ikibria 9797 May 22 11:04 awk.log
-rw-r--r-- 1 ikibria ikibria 5753 May 22 12:13 grep.log
-rw-r--r-- 1 ikibria ikibria    0 May 22 22:20 sort.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ cd folder-one/
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cat character
rahim
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
cumilla burichang
savar daffordil
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sort character
abdul
bishal ahmed
cumilla burichang
dhaka bangladesh
golam kibria
karim
rahim
savar
savar daffordil
tausif ahmed
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sort -r character
tausif ahmed
savar daffordil
savar
rahim
karim
golam kibria
dhaka bangladesh
cumilla burichang
bishal ahmed
abdul
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sort -k2 character
abdul
karim
rahim
savar
bishal ahmed
tausif ahmed
dhaka bangladesh
cumilla burichang
savar daffordil
golam kibria
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cd
ikibria@DESKTOP-OPJUB1R:~$ ls -l | sort
-r-x--x--x 1 ikibria ikibria    0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 one
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:34 japan
-rw-r--r-- 1 ikibria ikibria    0 May 22 22:20 sort.log
-rw-r--r-- 1 ikibria ikibria 5753 May 22 12:13 grep.log
-rw-r--r-- 1 ikibria ikibria 5974 May 22 10:17 cut.log
-rw-r--r-- 1 ikibria ikibria 8192 May 21 19:34 typescript
-rw-r--r-- 1 ikibria ikibria 9752 May 21 19:40 maintainence.log
-rw-r--r-- 1 ikibria ikibria 9797 May 22 11:04 awk.log
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
drwxr-xr-x 2 ikibria ikibria 4096 May 21 19:30 savar
drwxr-xr-x 2 ikibria ikibria 4096 May 22 10:06 folder-one
total 60
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -l | sort -k9
total 60
-rw-r--r-- 1 ikibria ikibria 9797 May 22 11:04 awk.log
-rw-r--r-- 1 ikibria ikibria 5974 May 22 10:17 cut.log
drwxr-xr-x 2 ikibria ikibria 4096 May 22 10:06 folder-one
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
-rw-r--r-- 1 ikibria ikibria 5753 May 22 12:13 grep.log
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:34 japan
-rw-r--r-- 1 ikibria ikibria 9752 May 21 19:40 maintainence.log
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 one
-r-x--x--x 1 ikibria ikibria    0 May 20 20:23 sam
drwxr-xr-x 2 ikibria ikibria 4096 May 21 19:30 savar
-rw-r--r-- 1 ikibria ikibria    0 May 22 22:20 sort.log
-rw-r--r-- 1 ikibria ikibria 8192 May 21 19:34 typescript
```
```
ikibria@DESKTOP-OPJUB1R:~$ cd folder-one/
ikibria@DESKTOP-OPJUB1R:~/folder-one$ uniq character
rahim
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
cumilla burichang
savar daffordil
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ echo "karim" >> character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ uniq character
rahim
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
cumilla burichang
savar daffordil
karim
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sort character | uniq
abdul
bishal ahmed
cumilla burichang
dhaka bangladesh
golam kibria
karim
rahim
savar
savar daffordil
tausif ahmed
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sort character | uniq -c
      1 abdul
      1 bishal ahmed
      1 cumilla burichang
      1 dhaka bangladesh
      1 golam kibria
      2 karim
      1 rahim
      1 savar
      1 savar daffordil
      1 tausif ahmed
ikibria@DESKTOP-OPJUB1R:~/folder-one$ sort character | uniq -d
karim
ikibria@DESKTOP-OPJUB1R:~/folder-one$
```
**[The End]**