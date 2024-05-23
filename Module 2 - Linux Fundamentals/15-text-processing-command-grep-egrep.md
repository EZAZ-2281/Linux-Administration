# grep/egrep command

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ grep --version
grep (GNU grep) 3.4
Copyright (C) 2020 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <https://gnu.org/licenses/gpl.html>.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Written by Mike Haertel and others; see
<https://git.sv.gnu.org/cgit/grep.git/tree/AUTHORS>.
```
```
ikibria@DESKTOP-OPJUB1R:~$ cd folder-one/
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cat character
rahim
karim
abdul
savar
golam kibria
tausif ahmed
bishal ahmed
dhaka bangladesh
cumilla burichang
savar daffordil
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ grep ahmed character
tausif ahmed
bishal ahmed
ikibria@DESKTOP-OPJUB1R:~/folder-one$ grep ikibria /etc/passwr
grep: /etc/passwr: No such file or directory
ikibria@DESKTOP-OPJUB1R:~/folder-one$ grep ikibria /etc/passwd
ikibria:x:1000:1000:,,,:/home/ikibria:/bin/bash
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ grep -c ahmed character
2
ikibria@DESKTOP-OPJUB1R:~/folder-one$ grep Ahmed character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ grep -i Ahmed character
tausif ahmed
bishal ahmed
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ grep -n ahmed character
6:tausif ahmed
7:bishal ahmed
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ grep -v ahmed character
rahim
karim
abdul
savar
golam kibria
dhaka bangladesh
cumilla burichang
savar daffordil
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ grep vi Ahmed character
grep: Ahmed: No such file or directory
ikibria@DESKTOP-OPJUB1R:~/folder-one$ grep -vi Ahmed character
rahim
karim
abdul
savar
golam kibria
dhaka bangladesh
cumilla burichang
savar daffordil
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ grep -v ahmed character | awk '{print $1}'
rahim
karim
abdul
savar
golam
dhaka
cumilla
savar
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ grep -v ahmed character | awk '{print $1}' | cut -c1-3
rah
kar
abd
sav
gol
dha
cum
sav
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cd
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr | grep folder1
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
ikibria@DESKTOP-OPJUB1R:~$ cd folder-one
ikibria@DESKTOP-OPJUB1R:~/folder-one$ grep -i "ahmed|kibria" character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ egrep -i "ahmed|kibria" character
golam kibria
tausif ahmed
bishal ahmed
ikibria@DESKTOP-OPJUB1R:~/folder-one$ exit
ikibria@DESKTOP-OPJUB1R:~$
```
**[The End]**