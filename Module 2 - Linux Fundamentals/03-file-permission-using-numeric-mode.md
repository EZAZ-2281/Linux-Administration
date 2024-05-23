# File Permission - Numeric

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ touch sam
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 8
-rw-rw-r-- 1 ikibria ikibria    0 May 19 19:43 one
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 two
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 three
-rw-r--r-- 1 ikibria ikibria 3817 May 19 19:45 syntax.log
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
-rw-r--r-- 1 ikibria ikibria    0 May 20 20:23 numeric-permisson.log
-rw-r--r-- 1 ikibria ikibria    0 May 20 20:23 sam
```
```
ikibria@DESKTOP-OPJUB1R:~$ chmod 764 sam
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr sam
-rwxrw-r-- 1 ikibria ikibria 0 May 20 20:23 sam
```
```
ikibria@DESKTOP-OPJUB1R:~$ chmod 000 sam
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr sam
---------- 1 ikibria ikibria 0 May 20 20:23 sam
```
```
ikibria@DESKTOP-OPJUB1R:~$ chmod 600 sam
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr sam
-rw------- 1 ikibria ikibria 0 May 20 20:23 sam
```
```
ikibria@DESKTOP-OPJUB1R:~$ chmod 604 sam
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr sam
-rw----r-- 1 ikibria ikibria 0 May 20 20:23 sam
```
```
ikibria@DESKTOP-OPJUB1R:~$ chmod 111 sam
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr sam
---x--x--x 1 ikibria ikibria 0 May 20 20:23 sam
```
```
ikibria@DESKTOP-OPJUB1R:~$ chmod 511 sam
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr sam
-r-x--x--x 1 ikibria ikibria 0 May 20 20:23 sam
ikibria@DESKTOP-OPJUB1R:~$ 
```
**[The End]**