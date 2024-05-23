## Copy Folder

```
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ mkdir foler-one
ikibria@DESKTOP-OPJUB1R:~$ mkdir foler-two
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 60
-rw-r--r-- 1 ikibria ikibria     0 May 18 20:36 one.txt
drwxr-xr-x 3 ikibria ikibria  4096 May 19 13:38 one
-rw-r--r-- 1 ikibria ikibria  3349 May 19 13:39 arpath.log
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:44 jerry
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:45 kramer
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:46 jerry-copy
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:47 jerry-copy-2
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:48 homer
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:49 march
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:49 lisa
-rw-r--r-- 1 ikibria ikibria     0 May 19 13:49 bart
drwxr-xr-x 2 ikibria ikibria  4096 May 19 13:49 seinfeld
drwxr-xr-x 2 ikibria ikibria  4096 May 19 13:50 superman
drwxr-xr-x 2 ikibria ikibria  4096 May 19 13:50 hulk
-rw-r--r-- 1 ikibria ikibria 32026 May 19 13:55 createfile.log
-rw-r--r-- 1 ikibria ikibria     0 May 19 14:00 cpfoler.log
drwxr-xr-x 2 ikibria ikibria  4096 May 19 14:01 foler-one ✅
drwxr-xr-x 2 ikibria ikibria  4096 May 19 14:01 foler-two ✅
```
```
ikibria@DESKTOP-OPJUB1R:~$ cd foler-one
ikibria@DESKTOP-OPJUB1R:~/foler-one$ touch one two three
ikibria@DESKTOP-OPJUB1R:~/foler-one$ ls -ltr
total 0
-rw-r--r-- 1 ikibria ikibria 0 May 19 14:01 two
-rw-r--r-- 1 ikibria ikibria 0 May 19 14:01 three
-rw-r--r-- 1 ikibria ikibria 0 May 19 14:01 one
```
```
ikibria@DESKTOP-OPJUB1R:~/foler-one$ cd
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
```
```
ikibria@DESKTOP-OPJUB1R:~$ cp foler-one foler-two
cp: -r not specified; omitting directory 'foler-one'
ikibria@DESKTOP-OPJUB1R:~$ cp -r foler-one foler-two
```
```
ikibria@DESKTOP-OPJUB1R:~$ cd foler-two
ikibria@DESKTOP-OPJUB1R:~/foler-two$ ls
foler-one
ikibria@DESKTOP-OPJUB1R:~/foler-two$ cd foler-one
ikibria@DESKTOP-OPJUB1R:~/foler-two/foler-one$ ls
one  three  two
```
**[The End]**