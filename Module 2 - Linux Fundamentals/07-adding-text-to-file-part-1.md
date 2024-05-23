# Add Text to File - Part 01
```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch pen
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr pen
-rw-r--r-- 1 ikibria ikibria 0 May 21 10:41 pen
```
```
ikibria@DESKTOP-OPJUB1R:~$ echo "This is first line" > pen
ikibria@DESKTOP-OPJUB1R:~$ cat pen
This is first line
ikibria@DESKTOP-OPJUB1R:~$ echo "This is second line" >> pen
ikibria@DESKTOP-OPJUB1R:~$ cat pen
This is first line
This is second line
```
```
ikibria@DESKTOP-OPJUB1R:~$ echo "This overwrite everything and create the file pen again" > pen
ikibria@DESKTOP-OPJUB1R:~$ cat pen
This overwrite everything and create the file pen again
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr pen
-rw-r--r-- 1 ikibria ikibria 56 May 21 10:42 pen
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch pen2
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr pen2
-rw-r--r-- 1 ikibria ikibria 0 May 21 10:43 pen2

ikibria@DESKTOP-OPJUB1R:~$ ls -ltr > pen2
ikibria@DESKTOP-OPJUB1R:~$ cat pen2
total 16
-rw-r--r--  1 ikibria ikibria    0 May 19 19:43 two
-rw-r--r--  1 ikibria ikibria    0 May 19 19:43 three
drwxr-xr-x  2 ikibria ikibria 4096 May 20 20:06 folder1
-r-x--x--x  1 ikibria ikibria    0 May 20 20:23 sam
-rw-rw-r--+ 1 ikibria ikibria    0 May 20 21:00 dhaka
-rw-r--r--  1 ikibria ikibria    6 May 20 21:11 one
-rw-r--r--  1 root    root       9 May 20 21:19 cumilla
-rw-r--r--  1 ikibria ikibria    0 May 21 10:41 addtexttofile.log
-rw-r--r--  1 ikibria ikibria   56 May 21 10:42 pen
-rw-r--r--  1 ikibria ikibria    0 May 21 10:43 pen2
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr pen2
-rw-r--r-- 1 ikibria ikibria 556 May 21 10:43 pen2
ikibria@DESKTOP-OPJUB1R:~$
```
**[The End]**