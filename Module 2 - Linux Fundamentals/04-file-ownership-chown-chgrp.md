# Change ownership

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 12
-rw-rw-r-- 1 ikibria ikibria    0 May 19 19:43 one
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 two
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 three
-rw-r--r-- 1 ikibria ikibria 3817 May 19 19:45 syntax.log
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria    0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria 3645 May 20 20:29 numeric-permisson.log
-rw-r--r-- 1 ikibria ikibria    0 May 20 20:33 chown-grp.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ sudo -i
[sudo] password for ikibria:
root@DESKTOP-OPJUB1R:~# pwd
/root
root@DESKTOP-OPJUB1R:~# cd /home/ikibria
root@DESKTOP-OPJUB1R:/home/ikibria# pwd
/home/ikibria
root@DESKTOP-OPJUB1R:/home/ikibria# ls -ltr
total 12
-rw-rw-r-- 1 ikibria ikibria    0 May 19 19:43 one
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 two
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 three
-rw-r--r-- 1 ikibria ikibria 3817 May 19 19:45 syntax.log
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria    0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria 3645 May 20 20:29 numeric-permisson.log
-rw-r--r-- 1 ikibria ikibria    0 May 20 20:33 chown-grp.log
```
```
root@DESKTOP-OPJUB1R:/home/ikibria# chown root one

root@DESKTOP-OPJUB1R:/home/ikibria# chgrp root one

root@DESKTOP-OPJUB1R:/home/ikibria# ls -ltr one
-rw-rw-r-- 1 root root 0 May 19 19:43 one

root@DESKTOP-OPJUB1R:/home/ikibria# exit
logout
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr one
-rw-rw-r-- 1 root root 0 May 19 19:43 one
ikibria@DESKTOP-OPJUB1R:~$ rm one
rm: remove write-protected regular empty file 'one'? y
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr one
ls: cannot access 'one': No such file or directory
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
```
```
ikibria@DESKTOP-OPJUB1R:~$ cd ..
ikibria@DESKTOP-OPJUB1R:/home$ pwd
/home
ikibria@DESKTOP-OPJUB1R:/home$ ls -l
total 4
drwxr-xr-x 5 ikibria ikibria 4096 May 20 20:39 ikibria
ikibria@DESKTOP-OPJUB1R:/home$ cd /etc
ikibria@DESKTOP-OPJUB1R:/etc$ touch testfile
touch: cannot touch 'testfile': Permission denied
```
```
ikibria@DESKTOP-OPJUB1R:/etc$ cd
ikibria@DESKTOP-OPJUB1R:~$ sudo -i
root@DESKTOP-OPJUB1R:~# cd /etc
root@DESKTOP-OPJUB1R:/etc# touch test123
root@DESKTOP-OPJUB1R:/etc# ls -ltr test123
-rw-r--r-- 1 root root 0 May 20 20:42 test123
root@DESKTOP-OPJUB1R:/etc# exit
logout
```
```
ikibria@DESKTOP-OPJUB1R:~$ cd /etc/
ikibria@DESKTOP-OPJUB1R:/etc$ ls -ltr test123
-rw-r--r-- 1 root root 0 May 20 20:42 test123
ikibria@DESKTOP-OPJUB1R:/etc$ rm test123
rm: remove write-protected regular empty file 'test123'? y
rm: cannot remove 'test123': Permission denied
ikibria@DESKTOP-OPJUB1R:/etc$ cd
ikibria@DESKTOP-OPJUB1R:~$ 
```
**[The End]**