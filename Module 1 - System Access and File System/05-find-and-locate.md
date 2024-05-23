## Find 

```
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 44
-rw-r--r-- 1 ikibria ikibria     0 May 18 20:36 one.txt
drwxr-xr-x 3 ikibria ikibria  4096 May 19 13:38 one
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:44 jerry
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:45 kramer
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:46 jerry-copy
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:47 jerry-copy-2
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:48 homer
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:49 march
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:49 lisa
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:49 bart
drwxr-xr-x 2 ikibria ikibria  4096 May 19 13:49 seinfeld
drwxr-xr-x 2 ikibria ikibria  4096 May 19 13:50 hulk
drwxr-xr-x 2 ikibria ikibria  4096 May 19 14:01 foler-one
drwxr-xr-x 3 ikibria ikibria  4096 May 19 14:02 foler-two
drwxr-xr-x 2 ikibria ikibria  4096 May 19 14:09 superman
-rw-r--r-- 1 ikibria ikibria 18497 May 19 14:24 find.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ cd superman
ikibria@DESKTOP-OPJUB1R:~/superman$ ls
four  one  three  two  unique
ikibria@DESKTOP-OPJUB1R:~/superman$ cd
```
```
ikibria@DESKTOP-OPJUB1R:~$ find . -name "unique"
./superman/unique
ikibria@DESKTOP-OPJUB1R:~$
```
```
root@DESKTOP-OPJUB1R:/# find / -name "ifcfg-eth0"
```
**[The End]**