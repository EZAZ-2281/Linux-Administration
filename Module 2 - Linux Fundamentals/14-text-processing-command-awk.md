# awk command

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 40
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria    0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 one
drwxr-xr-x 2 ikibria ikibria 4096 May 21 19:30 savar
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:34 japan
-rw-r--r-- 1 ikibria ikibria 8192 May 21 19:34 typescript
-rw-r--r-- 1 ikibria ikibria 9752 May 21 19:40 maintainence.log
drwxr-xr-x 2 ikibria ikibria 4096 May 22 10:06 folder-one
-rw-r--r-- 1 ikibria ikibria 5974 May 22 10:17 cut.log
-rw-r--r-- 1 ikibria ikibria    0 May 22 10:43 awk.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ cd folder-one/
ikibria@DESKTOP-OPJUB1R:~/folder-one$ echo "dhaka bangladesh" >> character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ echo "cumilla burichang" >> character
ikibria@DESKTOP-OPJUB1R:~/folder-one$ echo "savar daffordil" >> character
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
ikibria@DESKTOP-OPJUB1R:~/folder-one$ awk '{print $1}' character
rahim
karim
abdul
savar
golam
tausif
bishal
dhaka
cumilla
savar
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ awk '{print $2}' character




kibria
ahmed
ahmed
bangladesh
burichang
daffordil
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cd
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr | awk '{print $1, $3}'
total
drwxr-xr-x ikibria
-r-x--x--x ikibria
-rw-r--r-- ikibria
drwxr-xr-x ikibria
-rw-r--r-- ikibria
-rw-r--r-- ikibria
-rw-r--r-- ikibria
drwxr-xr-x ikibria
-rw-r--r-- ikibria
-rw-r--r-- ikibria
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr | awk '{print $9}'

folder1
sam
one
savar
japan
typescript
maintainence.log
folder-one
cut.log
awk.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr | awk '{print $nf}'
total 40
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria    0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 one
drwxr-xr-x 2 ikibria ikibria 4096 May 21 19:30 savar
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:34 japan
-rw-r--r-- 1 ikibria ikibria 8192 May 21 19:34 typescript
-rw-r--r-- 1 ikibria ikibria 9752 May 21 19:40 maintainence.log
drwxr-xr-x 2 ikibria ikibria 4096 May 22 10:06 folder-one
-rw-r--r-- 1 ikibria ikibria 5974 May 22 10:17 cut.log
-rw-r--r-- 1 ikibria ikibria    0 May 22 10:43 awk.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr | awk '{print $NF}'
40
folder1
sam
one
savar
japan
typescript
maintainence.log
folder-one
cut.log
awk.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ cd folder-one/
ikibria@DESKTOP-OPJUB1R:~/folder-one$ awk '/savar/ {print}' character
savar
savar daffordil
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cd
ikibria@DESKTOP-OPJUB1R:~$ awk -F: '{print $1}' /etc/passwd
root
daemon
bin
sys
sync
games
man
lp
mail
news
uucp
proxy
www-data
backup
list
irc
gnats
nobody
systemd-network
systemd-resolve
systemd-timesync
messagebus
syslog
_apt
tss
uuidd
tcpdump
sshd
landscape
pollinate
fwupd-refresh
systemd-coredump
lxd
ikibria
ikibria@DESKTOP-OPJUB1R:~$ echo "Hello Tom"
Hello Tom
ikibria@DESKTOP-OPJUB1R:~$ echo "Hello Tom" | awk '{$2="Adam";print $0}'
Hello Adam
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
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cat character | awk '{$2="kibria";print $0}'
rahim kibria
karim kibria
abdul kibria
savar kibria
golam kibria
tausif kibria
bishal kibria
dhaka kibria
cumilla kibria
savar kibria
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ awk 'length($0) > 3' character
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
ikibria@DESKTOP-OPJUB1R:~/folder-one$ awk 'length($0) > 15' character
dhaka bangladesh
cumilla burichang
```
```
ikibria@DESKTOP-OPJUB1R:~/folder-one$ cd
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 48
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria    0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 one
drwxr-xr-x 2 ikibria ikibria 4096 May 21 19:30 savar
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:34 japan
-rw-r--r-- 1 ikibria ikibria 8192 May 21 19:34 typescript
-rw-r--r-- 1 ikibria ikibria 9752 May 21 19:40 maintainence.log
drwxr-xr-x 2 ikibria ikibria 4096 May 22 10:06 folder-one
-rw-r--r-- 1 ikibria ikibria 5974 May 22 10:17 cut.log
-rw-r--r-- 1 ikibria ikibria 8192 May 22 11:01 awk.log

ikibria@DESKTOP-OPJUB1R:~$ ls -ltr | awk '{if($9=="japan") print $0;}'
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:34 japan
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr | awk '{print NF}'
2
9
9
9
9
9
9
9
9
9
9
ikibria@DESKTOP-OPJUB1R:~$ exit
ikibria@DESKTOP-OPJUB1R:~$
```
```
$ ls -ltr
total 20
-rw-r--r--  1 user user 1234 May 15 08:12 file1.txt
-rw-r--r--  1 user user 5678 May 15 08:15 file2.txt
drwxr-xr-x  2 user user 4096 May 15 08:20 directory1

এই আউটপুটে, total 20 মানে হল এই ডিরেক্টরিতে থাকা ফাইল ও ডিরেক্টরিগুলোর জন্য মোট 20 ব্লক ব্যবহৃত হয়েছে। UNIX এবং Linux ফাইল সিস্টেমে, প্রতিটি ফাইল একটি বা একাধিক ডাটা ব্লকে সংরক্ষিত থাকে। total মানটি সেই ব্লকগুলির সংযোজন করে দেখায়।

total কিভাবে গণনা করা হয়
প্রতিটি ফাইলের আকার এবং তারা যে ব্লক দখল করে তা যোগ করে এই মানটি নির্ধারণ করা হয়।

এইভাবে, total মানটি ডিরেক্টরির স্থান ব্যবহার সম্পর্কে ধারণা দেয় এবং এটি নির্ধারণ করতে সাহায্য করে যে একটি নির্দিষ্ট ডিরেক্টরি কতটা স্থান দখল করছে।
```