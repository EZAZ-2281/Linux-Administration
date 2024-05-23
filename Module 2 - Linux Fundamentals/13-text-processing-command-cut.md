# Cut command

```
ikibria@DESKTOP-OPJUB1R:~$ mkdir folder-one
ikibria@DESKTOP-OPJUB1R:~$ cd folder-one
ikibria@DESKTOP-OPJUB1R:~/folder-one$ touch character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ echo "rahim" > character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ echo "karim" >> character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ echo "abdul" >> character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ echo "savar" >> character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ echo "golam kibria" >> character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ echo "tausif ahmed" >> character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ echo "bishal ahmed" >> character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cat character
rahim
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cut --version
cut (GNU coreutils) 8.30
Copyright (C) 2018 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <https://gnu.org/licenses/gpl.html>.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Written by David M. Ihnat, David MacKenzie, and Jim Meyering.
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cut -c1 character
r
k
a
s
g
t
b
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cut -c1,3,5 character
rhm
krm
adl
svr
glm
tui
bsa
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cut -c1-4 character
rahi
kari
abdu
sava
gola
taus
bish
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cut -c1-3,6-8 character
rah
kar
abd
sav
gol ki
tauf a
bisl a
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cut -b1-3 character
rah
kar
abd
sav
gol
tau
bis
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cut -d: -f 6 /etc/passwd
/root
/usr/sbin
/bin
/dev
/bin
/usr/games
/var/cache/man
/var/spool/lpd
/var/mail
/var/spool/news
/var/spool/uucp
/bin
/var/www
/var/backups
/var/list
/var/run/ircd
/var/lib/gnats
/nonexistent
/run/systemd
/run/systemd
/run/systemd
/nonexistent
/home/syslog
/nonexistent
/var/lib/tpm
/run/uuidd
/nonexistent
/run/sshd
/var/lib/landscape
/var/cache/pollinate
/run/systemd
/
/var/snap/lxd/common/lxd
/home/ikibria
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cut -d: -f 6-7 /etc/passwd
/root:/bin/bash
/usr/sbin:/usr/sbin/nologin
/bin:/usr/sbin/nologin
/dev:/usr/sbin/nologin
/bin:/bin/sync
/usr/games:/usr/sbin/nologin
/var/cache/man:/usr/sbin/nologin
/var/spool/lpd:/usr/sbin/nologin
/var/mail:/usr/sbin/nologin
/var/spool/news:/usr/sbin/nologin
/var/spool/uucp:/usr/sbin/nologin
/bin:/usr/sbin/nologin
/var/www:/usr/sbin/nologin
/var/backups:/usr/sbin/nologin
/var/list:/usr/sbin/nologin
/var/run/ircd:/usr/sbin/nologin
/var/lib/gnats:/usr/sbin/nologin
/nonexistent:/usr/sbin/nologin
/run/systemd:/usr/sbin/nologin
/run/systemd:/usr/sbin/nologin
/run/systemd:/usr/sbin/nologin
/nonexistent:/usr/sbin/nologin
/home/syslog:/usr/sbin/nologin
/nonexistent:/usr/sbin/nologin
/var/lib/tpm:/bin/false
/run/uuidd:/usr/sbin/nologin
/nonexistent:/usr/sbin/nologin
/run/sshd:/usr/sbin/nologin
/var/lib/landscape:/usr/sbin/nologin
/var/cache/pollinate:/bin/false
/run/systemd:/usr/sbin/nologin
/:/usr/sbin/nologin
/var/snap/lxd/common/lxd:/bin/false
/home/ikibria:/bin/bash
ikibria@DESKTOP-OPJUB1R:~/folder-one$ pwd
/home/ikibria/folder-one
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cd
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr | cut -c2-4
ota
rwx
r-x
rw-
rwx
rw-
rw-
rw-
rwx
rw-
ikibria@DESKTOP-OPJUB1R:~$ exit
ikibria@DESKTOP-OPJUB1R:~$
```
**[The End]**