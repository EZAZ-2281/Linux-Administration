# File Permission
```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ hostname
DESKTOP-OPJUB1R
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 4
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 one
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 two
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 three
-rw-r--r-- 1 ikibria ikibria 3817 May 19 19:45 syntax.log
ikibria@DESKTOP-OPJUB1R:~$ ls -l one
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:43 one
```
```
ikibria@DESKTOP-OPJUB1R:~$ chmod g-w one
ikibria@DESKTOP-OPJUB1R:~$ ls -l one
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:43 one

ikibria@DESKTOP-OPJUB1R:~$ chmod a-r one
ikibria@DESKTOP-OPJUB1R:~$ ls -l one
--w------- 1 ikibria ikibria 0 May 19 19:43 one

ikibria@DESKTOP-OPJUB1R:~$ chmod u-w one
ikibria@DESKTOP-OPJUB1R:~$ ls -l one
---------- 1 ikibria ikibria 0 May 19 19:43 one
```
```
ikibria@DESKTOP-OPJUB1R:~$ rm one
rm: remove write-protected regular empty file 'one'? n
ikibria@DESKTOP-OPJUB1R:~$ cat one
cat: one: Permission denied
```
```
ikibria@DESKTOP-OPJUB1R:~$ chmod u+rw one
ikibria@DESKTOP-OPJUB1R:~$ ls -l one
-rw------- 1 ikibria ikibria 0 May 19 19:43 one
ikibria@DESKTOP-OPJUB1R:~$ chmod g+rw one
ikibria@DESKTOP-OPJUB1R:~$ ls -l one
-rw-rw---- 1 ikibria ikibria 0 May 19 19:43 one
ikibria@DESKTOP-OPJUB1R:~$ chmod o+r one
ikibria@DESKTOP-OPJUB1R:~$ ls -l one
-rw-rw-r-- 1 ikibria ikibria 0 May 19 19:43 one
```
```
ikibria@DESKTOP-OPJUB1R:~$ mkdir folder1
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 8
-rw-rw-r-- 1 ikibria ikibria    0 May 19 19:43 one
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 two
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 three
-rw-r--r-- 1 ikibria ikibria 3817 May 19 19:45 syntax.log
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
ikibria@DESKTOP-OPJUB1R:~$ chmod a-x folder1/
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 8
-rw-rw-r-- 1 ikibria ikibria    0 May 19 19:43 one
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 two
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 three
-rw-r--r-- 1 ikibria ikibria 3817 May 19 19:45 syntax.log
drw-r--r-- 2 ikibria ikibria 4096 May 20 20:06 folder1 ✅
```
```
ikibria@DESKTOP-OPJUB1R:~$ cd folder1/
-bash: cd: folder1/: Permission denied
ikibria@DESKTOP-OPJUB1R:~$ chmod a+x folder1/
ikibria@DESKTOP-OPJUB1R:~$ cd folder1/
ikibria@DESKTOP-OPJUB1R:~/folder1$ cd
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 8
-rw-rw-r-- 1 ikibria ikibria    0 May 19 19:43 one
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 two
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 three
-rw-r--r-- 1 ikibria ikibria 3817 May 19 19:45 syntax.log
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
ikibria@DESKTOP-OPJUB1R:~$
```

**[The End]**