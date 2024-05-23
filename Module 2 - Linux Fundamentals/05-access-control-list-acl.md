# Access Control List

```
ikibria@DESKTOP-OPJUB1R:~$ sudo -i
[sudo] password for ikibria:
root@DESKTOP-OPJUB1R:~# pwd
/root
root@DESKTOP-OPJUB1R:~# whoami
root
root@DESKTOP-OPJUB1R:~# pwd
/root
root@DESKTOP-OPJUB1R:~# ls -ltr
total 4
drwx------ 3 root root 4096 May 18 20:22 snap
```
```
root@DESKTOP-OPJUB1R:~# cd
root@DESKTOP-OPJUB1R:~# pwd
/root
root@DESKTOP-OPJUB1R:~# cd /home/ikibria
root@DESKTOP-OPJUB1R:/home/ikibria# pwd
/home/ikibria
```
```
root@DESKTOP-OPJUB1R:/home/ikibria# touch cumilla
root@DESKTOP-OPJUB1R:/home/ikibria# ls -ltr cumilla
-rw-r--r-- 1 root root 0 May 20 21:15 cumilla
root@DESKTOP-OPJUB1R:/home/ikibria# getfacl cumilla
# file: cumilla
# owner: root
# group: root
user::rw-
group::r--
other::r--
```
```
root@DESKTOP-OPJUB1R:/home/ikibria# setfacl -m u:ikibria:rw /home/ikibria/cumilla
root@DESKTOP-OPJUB1R:/home/ikibria# getfacl cumilla
# file: cumilla
# owner: root
# group: root
user::rw-
user:ikibria:rw-
group::r--
mask::rw-
other::r--
```
```
root@DESKTOP-OPJUB1R:/home/ikibria# exit
logout
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr cumilla
-rw-rw-r--+ 1 root root 0 May 20 21:15 cumilla
ikibria@DESKTOP-OPJUB1R:~$ cat cumilla
ikibria@DESKTOP-OPJUB1R:~$ echo "Hello..!" >cumilla
ikibria@DESKTOP-OPJUB1R:~$ cat cumilla
Hello..!
```
```
ikibria@DESKTOP-OPJUB1R:~$ sudo -i
root@DESKTOP-OPJUB1R:~# setfacl -m g:ikibria:rw /home/ikibria/cumilla

root@DESKTOP-OPJUB1R:~# getfacl /home/ikibria/cumilla
getfacl: Removing leading '/' from absolute path names
# file: home/ikibria/cumilla
# owner: root
# group: root
user::rw-
user:ikibria:rw-
group::r--
group:ikibria:rw-
mask::rw-
other::r--
```
```
root@DESKTOP-OPJUB1R:~# setfacl -x u:ikibria /home/ikibria/cumilla
root@DESKTOP-OPJUB1R:~# getfacl /home/ikibria/cumilla
getfacl: Removing leading '/' from absolute path names
# file: home/ikibria/cumilla
# owner: root
# group: root
user::rw-
group::r--
group:ikibria:rw-
mask::rw-
other::r--
```
The -b option allows you to quickly clear all the extended ACLs.
```
root@DESKTOP-OPJUB1R:~# setfacl -b /home/ikibria/cumilla
root@DESKTOP-OPJUB1R:~# getfacl /home/ikibria/cumilla
getfacl: Removing leading '/' from absolute path names
# file: home/ikibria/cumilla
# owner: root
# group: root
user::rw-
group::r--
other::r--

root@DESKTOP-OPJUB1R:~# exit
logout
ikibria@DESKTOP-OPJUB1R:~$ exit
exit
```


**[The End]**