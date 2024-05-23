## Navigation File System

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ hostname
DESKTOP-OPJUB1R
```
```
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ cd
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ cd ../
ikibria@DESKTOP-OPJUB1R:/home$ pwd
/home
ikibria@DESKTOP-OPJUB1R:/home$ cd ../
ikibria@DESKTOP-OPJUB1R:/$ pwd
/
ikibria@DESKTOP-OPJUB1R:/$ cd
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
```
```
ikibria@DESKTOP-OPJUB1R:~$ cd /
ikibria@DESKTOP-OPJUB1R:/$ pwd
/
```
```
ikibria@DESKTOP-OPJUB1R:/$ pwd
/
ikibria@DESKTOP-OPJUB1R:/$ ls
bin   dev  home  lib    lib64   lost+found  mnt  proc  run   snap  sys  usr
boot  etc  init  lib32  libx32  media       opt  root  sbin  srv   tmp  var
ikibria@DESKTOP-OPJUB1R:/$ cd etc
```
```
ikibria@DESKTOP-OPJUB1R:/etc$ clear
```
```
ikibria@DESKTOP-OPJUB1R:/etc$ pwd
/etc
ikibria@DESKTOP-OPJUB1R:/etc$ cd
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ ls
one.txt
ikibria@DESKTOP-OPJUB1R:~$ ls -l
total 0
-rw-r--r-- 1 ikibria ikibria 0 May 18 20:36 one.txt
```
```
ikibria@DESKTOP-OPJUB1R:~$ sudo -i
root@DESKTOP-OPJUB1R:~# passwd ikibria
New password:
Retype new password:
passwd: password updated successfully
```
### Summary 
```
bash
whoami
hostname
pwd
cd
cd ../
cd /
ls
cd etc
clear
ls -l
sudo -i
passwd ikibria
```
**[The End]**