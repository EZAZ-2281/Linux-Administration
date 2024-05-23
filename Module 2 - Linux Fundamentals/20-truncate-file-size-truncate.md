# truncate

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch captain
ikibria@DESKTOP-OPJUB1R:~$ echo "hello, how are you?" > captain
ikibria@DESKTOP-OPJUB1R:~$ cat captain
hello, how are you?
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr captain
-rw-r--r-- 1 ikibria ikibria 👉20 May 23 10:33 captain
ikibria@DESKTOP-OPJUB1R:~$ truncate -s 15 captain
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr captain
-rw-r--r-- 1 ikibria ikibria 👉15 May 23 10:34 captain
ikibria@DESKTOP-OPJUB1R:~$ cat captain
hello, how are ikibria@DESKTOP-OPJUB1R:~$
```
```
ikibria@DESKTOP-OPJUB1R:~$ truncate -s 30 captain
ikibria@DESKTOP-OPJUB1R:~$ cat captain
hello, how are ikibria@DESKTOP-OPJUB1R:~$
ikibria@DESKTOP-OPJUB1R:~$ 
```
**[The End]**