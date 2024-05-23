## Absoulute and Relative Path
```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ hostname
DESKTOP-OPJUB1R
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ ls
arpath.log  one.txt
```
```
ikibria@DESKTOP-OPJUB1R:~$ mkdir one
ikibria@DESKTOP-OPJUB1R:~$ ls
arpath.log  one  one.txt
ikibria@DESKTOP-OPJUB1R:~$ cd one
ikibria@DESKTOP-OPJUB1R:~/one$ mkdir inside-one
ikibria@DESKTOP-OPJUB1R:~/one$ cd inside-one
ikibria@DESKTOP-OPJUB1R:~/one/inside-one$ mkdir core
ikibria@DESKTOP-OPJUB1R:~/one/inside-one$ ls
core
```
```
ikibria@DESKTOP-OPJUB1R:~/one/inside-one$ cd
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ ls
arpath.log  one  one.txt
```
**Absolute Path**
```
ikibria@DESKTOP-OPJUB1R:~$ cd one/inside-one/core
ikibria@DESKTOP-OPJUB1R:~/one/inside-one/core$ ls
ikibria@DESKTOP-OPJUB1R:~/one/inside-one/core$ cd ..
ikibria@DESKTOP-OPJUB1R:~/one/inside-one$ cd ../
ikibria@DESKTOP-OPJUB1R:~/one$ cd ../
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
```
**Relative Path**
```
ikibria@DESKTOP-OPJUB1R:~$ cd one
ikibria@DESKTOP-OPJUB1R:~/one$ cd inside-one
ikibria@DESKTOP-OPJUB1R:~/one/inside-one$ cd core
ikibria@DESKTOP-OPJUB1R:~/one/inside-one/core$ cd ..
ikibria@DESKTOP-OPJUB1R:~/one/inside-one$ cd ..
ikibria@DESKTOP-OPJUB1R:~/one$ cd ..
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
```
**[The End]**