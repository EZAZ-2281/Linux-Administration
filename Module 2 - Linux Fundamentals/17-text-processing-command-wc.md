# wc

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ wc --version
wc (GNU coreutils) 8.30
Copyright (C) 2018 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <https://gnu.org/licenses/gpl.html>.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Written by Paul Rubin and David MacKenzie.
```
```
ikibria@DESKTOP-OPJUB1R:~$ cd folder-one/
ikibria@DESKTOP-OPJUB1R:~/folder-one$ wc character
 11  17 120 character

ikibria@DESKTOP-OPJUB1R:~/folder-one$ wc -l character
11 character

ikibria@DESKTOP-OPJUB1R:~/folder-one$ wc -w character
17 character

ikibria@DESKTOP-OPJUB1R:~/folder-one$ wc -b character
wc: invalid option -- 'b'
Try 'wc --help' for more information.
ikibria@DESKTOP-OPJUB1R:~/folder-one$ wc -c character
120 character
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cd
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 68
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
-rw-r--r-- 1 ikibria ikibria 5747 May 22 22:37 sort.log
-rw-r--r-- 1 ikibria ikibria    0 May 23 09:14 wc.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ wc folder1
wc: folder1: Is a directory
      0       0       0 folder1
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ls | wc -l
14
ikibria@DESKTOP-OPJUB1R:~$ ls -ld
drwxr-xr-x 7 ikibria ikibria 4096 May 23 09:14 .
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr | grep drw
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
drwxr-xr-x 2 ikibria ikibria 4096 May 21 19:30 savar
drwxr-xr-x 2 ikibria ikibria 4096 May 22 10:06 folder-one
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr | grep drw | wc -l
3
```
```
ikibria@DESKTOP-OPJUB1R:~$ cd folder-one
ikibria@DESKTOP-OPJUB1R:~/folder-one$ grep ahmed character
tausif ahmed
bishal ahmed
ikibria@DESKTOP-OPJUB1R:~/folder-one$ grep ahmed character | wc -l
2
ikibria@DESKTOP-OPJUB1R:~/folder-one$
```
**[The End]**