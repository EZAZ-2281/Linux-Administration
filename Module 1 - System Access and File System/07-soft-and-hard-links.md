## Hardlink and Softlink

### Soft Link
```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
```
**ln stands for link**
```
ikibria@DESKTOP-OPJUB1R:~$ touch soft.txt
ikibria@DESKTOP-OPJUB1R:~$ cd /tmp
ikibria@DESKTOP-OPJUB1R:/tmp$ ln -s /home/ikibria/soft.txt
ikibria@DESKTOP-OPJUB1R:/tmp$ ls -ltr *soft*
lrwxrwxrwx 1 ikibria ikibria 22 May 19 19:21 soft.txt -> /home/ikibria/soft.txt
ikibria@DESKTOP-OPJUB1R:/tmp$
ikibria@DESKTOP-OPJUB1R:/tmp$ cd
```
```
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ echo "This is inside soft file" > soft.txt
ikibria@DESKTOP-OPJUB1R:~$ cat soft.txt
This is inside soft file
ikibria@DESKTOP-OPJUB1R:~$ cd /tmp
ikibria@DESKTOP-OPJUB1R:/tmp$ ls -ltr *soft*
lrwxrwxrwx 1 ikibria ikibria 22 May 19 19:21 soft.txt -> /home/ikibria/soft.txt
ikibria@DESKTOP-OPJUB1R:/tmp$ cat soft.txt
This is inside soft file
ikibria@DESKTOP-OPJUB1R:/tmp$ cd
```
**i means ilocator**
```
ikibria@DESKTOP-OPJUB1R:~$ ls -li *soft*
38048 -rw-r--r-- 1 ikibria ikibria 25 May 19 19:24 soft.txt
ikibria@DESKTOP-OPJUB1R:~$ cd /tmp
ikibria@DESKTOP-OPJUB1R:/tmp$ ls -ltr *soft*
lrwxrwxrwx 1 ikibria ikibria 22 May 19 19:21 soft.txt -> /home/ikibria/soft.txt
ikibria@DESKTOP-OPJUB1R:/tmp$ ls -li *soft*
38052 lrwxrwxrwx 1 ikibria ikibria 22 May 19 19:21 soft.txt -> /home/ikibria/soft.txt
ikibria@DESKTOP-OPJUB1R:/tmp$ cd
```
```
ikibria@DESKTOP-OPJUB1R:~$ rm soft.txt
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr *soft*
ls: cannot access '*soft*': No such file or directory
ikibria@DESKTOP-OPJUB1R:~$ cd tmp
bash: cd: tmp: No such file or directory
ikibria@DESKTOP-OPJUB1R:~$ cd /tmp
ikibria@DESKTOP-OPJUB1R:/tmp$ ls -ltr *soft*
lrwxrwxrwx 1 ikibria ikibria 22 May 19 19:21 soft.txt -> /home/ikibria/soft.txt
ikibria@DESKTOP-OPJUB1R:/tmp$ ls -li *soft*
38052 lrwxrwxrwx 1 ikibria ikibria 22 May 19 19:21 soft.txt -> /home/ikibria/soft.txt
ikibria@DESKTOP-OPJUB1R:/tmp$ cat soft.txt
cat: soft.txt: No such file or directory
ikibria@DESKTOP-OPJUB1R:/tmp$ rm soft.txt
ikibria@DESKTOP-OPJUB1R:/tmp$ ls -ltr *soft*
ls: cannot access '*soft*': No such file or directory
ikibria@DESKTOP-OPJUB1R:/tmp$ cd
ikibria@DESKTOP-OPJUB1R:~$
```
### Hard Link
```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch hard
ikibria@DESKTOP-OPJUB1R:~$ echo "Inside hard file" > hard
ikibria@DESKTOP-OPJUB1R:~$ cat hard
Inside hard file
ikibria@DESKTOP-OPJUB1R:~$ cd /tmp
ikibria@DESKTOP-OPJUB1R:/tmp$ ln /home/ikibria/hard
ikibria@DESKTOP-OPJUB1R:/tmp$ ls -ltr *hard*
-rw-r--r-- 2 ikibria ikibria 17 May 19 19:29 hard
ikibria@DESKTOP-OPJUB1R:/tmp$ ls -li *hard*
38048 -rw-r--r-- 2 ikibria ikibria 17 May 19 19:29 hard
ikibria@DESKTOP-OPJUB1R:/tmp$ cat hard
Inside hard file
ikibria@DESKTOP-OPJUB1R:/tmp$ cd
```
```
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr *hard*
-rw-r--r-- 1 ikibria ikibria 4096 May 19 19:28 hardlink.log
-rw-r--r-- 2 ikibria ikibria   17 May 19 19:29 hard
ikibria@DESKTOP-OPJUB1R:~$ echo "123" > hard
ikibria@DESKTOP-OPJUB1R:~$ cat hard
123
ikibria@DESKTOP-OPJUB1R:~$ cd /tmp
ikibria@DESKTOP-OPJUB1R:/tmp$ cat hard
123
ikibria@DESKTOP-OPJUB1R:/tmp$ ls -li *hard*
38048 -rw-r--r-- 2 ikibria ikibria 4 May 19 19:30 hard
ikibria@DESKTOP-OPJUB1R:/tmp$ cd
ikibria@DESKTOP-OPJUB1R:~$ ls -li *hard*
38048 -rw-r--r-- 2 ikibria ikibria    4 May 19 19:30 hard
37967 -rw-r--r-- 1 ikibria ikibria 4096 May 19 19:28 hardlink.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ rm hard
ikibria@DESKTOP-OPJUB1R:~$ cd /tmp
ikibria@DESKTOP-OPJUB1R:/tmp$ ls -ltr *hard*
-rw-r--r-- 1 ikibria ikibria 4 May 19 19:30 hard
ikibria@DESKTOP-OPJUB1R:/tmp$ ls -li *hard*
38048 -rw-r--r-- 1 ikibria ikibria 4 May 19 19:30 hard
ikibria@DESKTOP-OPJUB1R:/tmp$ rm hard
```
```
ikibria@DESKTOP-OPJUB1R:/tmp$ ls -ltr *hard*
ls: cannot access '*hard*': No such file or directory
ikibria@DESKTOP-OPJUB1R:/tmp$ ls -li *hard*
ls: cannot access '*hard*': No such file or directory
ikibria@DESKTOP-OPJUB1R:/tmp$ cd
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ exit
```
**[The End]**