## Linux Syntax

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch one
ikibria@DESKTOP-OPJUB1R:~$ touch two three
ikibria@DESKTOP-OPJUB1R:~$ ls
hardlink.log  one  syntax.log  three  two  wildcard.log

ikibria@DESKTOP-OPJUB1R:~$ ls -l
total 20
-rw-r--r-- 1 ikibria ikibria 8487 May 19 19:33 hardlink.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 one
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:42 syntax.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 three
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 two
-rw-r--r-- 1 ikibria ikibria 7417 May 19 19:15 wildcard.log

ikibria@DESKTOP-OPJUB1R:~$ ls -lt
total 20
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 three
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 two
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 one
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:42 syntax.log
-rw-r--r-- 1 ikibria ikibria 8487 May 19 19:33 hardlink.log
-rw-r--r-- 1 ikibria ikibria 7417 May 19 19:15 wildcard.log

ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 20
-rw-r--r-- 1 ikibria ikibria 7417 May 19 19:15 wildcard.log
-rw-r--r-- 1 ikibria ikibria 8487 May 19 19:33 hardlink.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:42 syntax.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 one
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 two
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 three
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -l three
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:43 three
ikibria@DESKTOP-OPJUB1R:~$ ls -l two
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:43 two
```
```
ikibria@DESKTOP-OPJUB1R:~$ mkdir new
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 24
-rw-r--r-- 1 ikibria ikibria 7417 May 19 19:15 wildcard.log
-rw-r--r-- 1 ikibria ikibria 8487 May 19 19:33 hardlink.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:42 syntax.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 one
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 two
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 three
drwxr-xr-x 2 ikibria ikibria 4096 May 19 19:45 new

ikibria@DESKTOP-OPJUB1R:~$ rm -f new
rm: cannot remove 'new': Is a directory
ikibria@DESKTOP-OPJUB1R:~$ rm -r new

ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 20
-rw-r--r-- 1 ikibria ikibria 7417 May 19 19:15 wildcard.log
-rw-r--r-- 1 ikibria ikibria 8487 May 19 19:33 hardlink.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:42 syntax.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 one
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 two
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:43 three
ikibria@DESKTOP-OPJUB1R:~$ exit
```
**[The End]**