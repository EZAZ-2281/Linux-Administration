# File Maintanaince Command

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 4
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria    0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 typescript
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 maintainence.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch one
ikibria@DESKTOP-OPJUB1R:~$ cp one two
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 4
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria    0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 typescript
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 maintainence.log
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 one
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 two
ikibria@DESKTOP-OPJUB1R:~$ echo "hello how are you" > two
ikibria@DESKTOP-OPJUB1R:~$ cat two
hello how are you
```
```
ikibria@DESKTOP-OPJUB1R:~$ mkdir savar
ikibria@DESKTOP-OPJUB1R:~$ cp two savar
ikibria@DESKTOP-OPJUB1R:~$ cd savar
ikibria@DESKTOP-OPJUB1R:~/savar$ ls -ltr
total 4
-rw-r--r-- 1 ikibria ikibria 18 May 21 19:26 two
ikibria@DESKTOP-OPJUB1R:~/savar$ cat two
hello how are you
```
```
ikibria@DESKTOP-OPJUB1R:~/savar$ cd
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch try
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr try
-rw-r--r-- 1 ikibria ikibria 0 May 21 19:28 try
ikibria@DESKTOP-OPJUB1R:~$ rm try
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr try
ls: cannot access 'try': No such file or directory
ikibria@DESKTOP-OPJUB1R:~$
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr two
-rw-r--r-- 1 ikibria ikibria 18 May 21 19:24 two
ikibria@DESKTOP-OPJUB1R:~$ mv two new-two
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr two
ls: cannot access 'two': No such file or directory
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr new-two
-rw-r--r-- 1 ikibria ikibria 18 May 21 19:24 new-two
ikibria@DESKTOP-OPJUB1R:~$
ikibria@DESKTOP-OPJUB1R:~$ cat new-two
hello how are you
```
```
ikibria@DESKTOP-OPJUB1R:~$ mv new-two savar
ikibria@DESKTOP-OPJUB1R:~$ cd savar
ikibria@DESKTOP-OPJUB1R:~/savar$ ls -ltr
total 8
-rw-r--r-- 1 ikibria ikibria 18 May 21 19:24 new-two
-rw-r--r-- 1 ikibria ikibria 18 May 21 19:26 two
ikibria@DESKTOP-OPJUB1R:~/savar$ cd
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$
```
```
ikibria@DESKTOP-OPJUB1R:~$ mkdir testp
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr testp/
total 0
ikibria@DESKTOP-OPJUB1R:~$ rmdir testp/
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr testp/
ls: cannot access 'testp/': No such file or directory
ikibria@DESKTOP-OPJUB1R:~$ mkdir testp2
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr testp2/
total 0
ikibria@DESKTOP-OPJUB1R:~$ rm -r testp2/
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr testp2/
ls: cannot access 'testp2/': No such file or directory
ikibria@DESKTOP-OPJUB1R:~$
```
```
ikibria@DESKTOP-OPJUB1R:~$
ikibria@DESKTOP-OPJUB1R:~$ touch japan
ikibria@DESKTOP-OPJUB1R:~$ chgrp root japan
chgrp: changing group of 'japan': Operation not permitted
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ sudo -i
[sudo] password for ikibria:
root@DESKTOP-OPJUB1R:~# pwd
/root
```
```
root@DESKTOP-OPJUB1R:~# cd /home/ikibria/
root@DESKTOP-OPJUB1R:/home/ikibria# ls -ltr japan
-rw-r--r-- 1 ikibria ikibria 0 May 21 19:34 japan
root@DESKTOP-OPJUB1R:/home/ikibria# chgrp root japan
root@DESKTOP-OPJUB1R:/home/ikibria# ls -ltr japan
-rw-r--r-- 1 ikibria root 0 May 21 19:34 japan
root@DESKTOP-OPJUB1R:/home/ikibria#
```
```
root@DESKTOP-OPJUB1R:/home/ikibria# chown root japan
root@DESKTOP-OPJUB1R:/home/ikibria# ls -ltr japan
-rw-r--r-- 1 root root 0 May 21 19:34 japan
root@DESKTOP-OPJUB1R:/home/ikibria#
```
```
root@DESKTOP-OPJUB1R:/home/ikibria# chown ikibria:ikibria japan
root@DESKTOP-OPJUB1R:/home/ikibria# ls -ltr japan
-rw-r--r-- 1 ikibria ikibria 0 May 21 19:34 japan
root@DESKTOP-OPJUB1R:/home/ikibria# exit
logout
ikibria@DESKTOP-OPJUB1R:~$ exit
exit
```

**[The End]**