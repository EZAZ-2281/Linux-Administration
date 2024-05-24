# user account

```
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ sudo -i
[sudo] password for ikibria:
root@DESKTOP-OPJUB1R:~# pwd
/root
```
```
root@DESKTOP-OPJUB1R:~# useradd -m hulk
root@DESKTOP-OPJUB1R:~# cd /home/
root@DESKTOP-OPJUB1R:/home# ls -ltr
total 12
drwxr-xr-x 2 spiderman2 spiderman2 4096 May 24 19:40 spiderman2
drwxr-xr-x 7 ikibria    ikibria    4096 May 24 19:41 ikibria
drwxr-xr-x 2 hulk       hulk       4096 May 24 19:42 hulk
```
```
root@DESKTOP-OPJUB1R:/home# groupadd superheroes
root@DESKTOP-OPJUB1R:/home# cat /etc/group
root:x:0:
hulk:x:1003:
superheroes:x:1004:
root@DESKTOP-OPJUB1R:/home# ls -ltr
total 12
drwxr-xr-x 2 spiderman2 spiderman2 4096 May 24 19:40 spiderman2
drwxr-xr-x 7 ikibria    ikibria    4096 May 24 19:41 ikibria
drwxr-xr-x 2 hulk       hulk       4096 May 24 19:42 hulk
```
```
root@DESKTOP-OPJUB1R:/home# userdel -r spiderman2
userdel: spiderman2 mail spool (/var/mail/spiderman2) not found
root@DESKTOP-OPJUB1R:/home# userdel -r spiderman2
userdel: user 'spiderman2' does not exist
root@DESKTOP-OPJUB1R:/home# ls -ltr
total 8
drwxr-xr-x 7 ikibria ikibria 4096 May 24 19:41 ikibria
drwxr-xr-x 2 hulk    hulk    4096 May 24 19:42 hulk
```
```
root@DESKTOP-OPJUB1R:/home# groupadd for-delete
root@DESKTOP-OPJUB1R:/home# cat /etc/group
root:x:0:
for-delete:x:1005:
```
```
root@DESKTOP-OPJUB1R:/home# groupdel for-delete
root@DESKTOP-OPJUB1R:/home# cat /etc/group
root:x:0:
superheroes:x:1004:
root@DESKTOP-OPJUB1R:/home# 
```
```
root@DESKTOP-OPJUB1R:~# cd /home/
root@DESKTOP-OPJUB1R:/home# ls -ltr
total 8
drwxr-xr-x 2 hulk    hulk    4096 May 24 19:42 hulk
drwxr-xr-x 7 ikibria ikibria 4096 May 24 19:57 ikibria
```
```
root@DESKTOP-OPJUB1R:/home# id hulk
uid=1003(hulk) gid=1003(hulk) groups=1003(hulk)
```
```
root@DESKTOP-OPJUB1R:/home# usermod -G superheroes hulk
root@DESKTOP-OPJUB1R:/home# grep hulk/ /etc/group
root@DESKTOP-OPJUB1R:/home# grep hulk /etc/group
hulk:x:1003:
superheroes:x:1004:hulk
```
```
root@DESKTOP-OPJUB1R:/home# ls -ltr
total 8
drwxr-xr-x 2 hulk    hulk    4096 May 24 19:42 hulk
drwxr-xr-x 7 ikibria ikibria 4096 May 24 19:57 ikibria
```
```
root@DESKTOP-OPJUB1R:/home# chgrp -R superheroes hulk
root@DESKTOP-OPJUB1R:/home# ls -ltr
total 8
drwxr-xr-x 2 hulk    superheroes 4096 May 24 19:42 hulk
drwxr-xr-x 7 ikibria ikibria     4096 May 24 19:57 ikibria
```
```
root@DESKTOP-OPJUB1R:/home# grep hulk /etc/passwd
hulk:x:1003:1003::/home/hulk:/bin/sh
```
```
root@DESKTOP-OPJUB1R:/home# useradd -g superheroes -s /bin/bash -c "a character" -m -d /home/hulk ironman
useradd: warning: the home directory /home/hulk already exists.
useradd: Not copying any file from skel directory into it.
```
```
root@DESKTOP-OPJUB1R:/home# ls -ltr
total 8
drwxr-xr-x 2 hulk    superheroes 4096 May 24 19:42 hulk
drwxr-xr-x 7 ikibria ikibria     4096 May 24 19:57 ikibria
root@DESKTOP-OPJUB1R:/home# id ironman
uid=1004(ironman) gid=1004(superheroes) groups=1004(superheroes)
```
```
root@DESKTOP-OPJUB1R:/home# grep ironman /etc/passwd
ironman:x:1004:1004:a character:/home/hulk:/bin/bash
ironman2:x:1005:1004:a character:/home/hulk:/bin/bash
root@DESKTOP-OPJUB1R:/home# passwd ironman
New password:
Retype new password:
passwd: password updated successfully
root@DESKTOP-OPJUB1R:/home# exit
```
**[The End]**