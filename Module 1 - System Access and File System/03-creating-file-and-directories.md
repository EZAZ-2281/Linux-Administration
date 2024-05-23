## Create File

```
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ ls
arpath.log  createfile.log  one  one.txt
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch jerry
ikibria@DESKTOP-OPJUB1R:~$ touch kramer
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 8
-rw-r--r-- 1 ikibria ikibria    0 May 18 20:36 one.txt
drwxr-xr-x 3 ikibria ikibria 4096 May 19 13:38 one
-rw-r--r-- 1 ikibria ikibria 3349 May 19 13:39 arpath.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:44 createfile.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:44 jerry
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:45 kramer
```
```
ikibria@DESKTOP-OPJUB1R:~$ cp jerry jerry-copy
ikibria@DESKTOP-OPJUB1R:~$ cp jerry jerry-copy-2
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 8
-rw-r--r-- 1 ikibria ikibria    0 May 18 20:36 one.txt
drwxr-xr-x 3 ikibria ikibria 4096 May 19 13:38 one
-rw-r--r-- 1 ikibria ikibria 3349 May 19 13:39 arpath.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:44 createfile.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:44 jerry
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:45 kramer
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:46 jerry-copy ✅
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:47 jerry-copy-2 ✅
```
**After typing vi homer use shift colon wq! (:wq!)**
```
ikibria@DESKTOP-OPJUB1R:~$ vi homer
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 12
-rw-r--r-- 1 ikibria ikibria    0 May 18 20:36 one.txt
drwxr-xr-x 3 ikibria ikibria 4096 May 19 13:38 one
-rw-r--r-- 1 ikibria ikibria 3349 May 19 13:39 arpath.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:44 jerry
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:45 kramer
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:46 jerry-copy
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:47 jerry-copy-2
-rw-r--r-- 1 ikibria ikibria 4096 May 19 13:48 createfile.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:48 homer ✅
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch bart lisa march
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 16
-rw-r--r-- 1 ikibria ikibria    0 May 18 20:36 one.txt
drwxr-xr-x 3 ikibria ikibria 4096 May 19 13:38 one
-rw-r--r-- 1 ikibria ikibria 3349 May 19 13:39 arpath.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:44 jerry
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:45 kramer
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:46 jerry-copy
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:47 jerry-copy-2
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:48 homer
-rw-r--r-- 1 ikibria ikibria 8192 May 19 13:48 createfile.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:49 march
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:49 lisa
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:49 bart
```
```
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ mkdir seinfeld
ikibria@DESKTOP-OPJUB1R:~$ mkdir superman hulk
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 28
-rw-r--r-- 1 ikibria ikibria    0 May 18 20:36 one.txt
drwxr-xr-x 3 ikibria ikibria 4096 May 19 13:38 one
-rw-r--r-- 1 ikibria ikibria 3349 May 19 13:39 arpath.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:44 jerry
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:45 kramer
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:46 jerry-copy
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:47 jerry-copy-2
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:48 homer
-rw-r--r-- 1 ikibria ikibria 8192 May 19 13:48 createfile.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:49 march
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:49 lisa
-rw-r--r-- 1 ikibria ikibria    0 May 19 13:49 bart
drwxr-xr-x 2 ikibria ikibria 4096 May 19 13:49 seinfeld
drwxr-xr-x 2 ikibria ikibria 4096 May 19 13:50 superman
drwxr-xr-x 2 ikibria ikibria 4096 May 19 13:50 hulk
```
```
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ cd /
ikibria@DESKTOP-OPJUB1R:/$ pwd
/
ikibria@DESKTOP-OPJUB1R:/$ ls
bin   dev  home  lib    lib64   lost+found  mnt  proc  run   snap  sys  usr
boot  etc  init  lib32  libx32  media       opt  root  sbin  srv   tmp  var
```
```
ikibria@DESKTOP-OPJUB1R:/$ cd etc
ikibria@DESKTOP-OPJUB1R:/etc$ touch test123
touch: cannot touch 'test123': Permission denied
ikibria@DESKTOP-OPJUB1R:/etc$ cd
ikibria@DESKTOP-OPJUB1R:~$ sudo -i
[sudo] password for ikibria:
root@DESKTOP-OPJUB1R:~# pwd
/root
root@DESKTOP-OPJUB1R:~# cd /
root@DESKTOP-OPJUB1R:/# pwd
/
root@DESKTOP-OPJUB1R:/# ls
bin   dev  home  lib    lib64   lost+found  mnt  proc  run   snap  sys  usr
boot  etc  init  lib32  libx32  media       opt  root  sbin  srv   tmp  var
root@DESKTOP-OPJUB1R:/# cd etc
root@DESKTOP-OPJUB1R:/etc# touch test123
```
```
root@DESKTOP-OPJUB1R:/etc# ls -ltr
total 840
-rw-r--r-- 1 root root          0 May 19 13:54 test123
root@DESKTOP-OPJUB1R:/etc# cd
root@DESKTOP-OPJUB1R:~# pwd
/root
root@DESKTOP-OPJUB1R:~# exit
logout
ikibria@DESKTOP-OPJUB1R:~$
ikibria@DESKTOP-OPJUB1R:~$ exit
```
**[The End]**