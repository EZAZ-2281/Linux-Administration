## Wildcard

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
````
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 0
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:02 wildcard.log
ikibria@DESKTOP-OPJUB1R:~$
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch abcd1-xyz
ikibria@DESKTOP-OPJUB1R:~$ touch abcd2-xyz
ikibria@DESKTOP-OPJUB1R:~$ touch abcd3-xyz
ikibria@DESKTOP-OPJUB1R:~$ touch abcd4-xyz
ikibria@DESKTOP-OPJUB1R:~$ ls
abcd1-xyz  abcd2-xyz  abcd3-xyz  abcd4-xyz  wildcard.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ rm abcd1-xyz
ikibria@DESKTOP-OPJUB1R:~$ ls
abcd2-xyz  abcd3-xyz  abcd4-xyz  wildcard.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ rm abcd*
ikibria@DESKTOP-OPJUB1R:~$ ls
wildcard.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch abcd{1..5}-xyz

ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 0
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:02  wildcard.log
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:06 'abcd[1..5]-xyz'
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:07  abcd{1-5}-xyz
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:07  abcd5-xyz
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:07  abcd4-xyz
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:07  abcd3-xyz
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:07  abcd2-xyz
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:07  abcd1-xyz

ikibria@DESKTOP-OPJUB1R:~$ ls -ltr abc*
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:06 'abcd[1..5]-xyz'
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:07  abcd{1-5}-xyz
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:07  abcd5-xyz
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:07  abcd4-xyz
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:07  abcd3-xyz
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:07  abcd2-xyz
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:07  abcd1-xyz
```
```
ikibria@DESKTOP-OPJUB1R:~$ rm abcd*
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 0
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:02 wildcard.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch abcd{1..5}-xyz
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 4
-rw-r--r-- 1 ikibria ikibria 4096 May 19 19:09 wildcard.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:10 abcd5-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:10 abcd4-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:10 abcd3-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:10 abcd2-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:10 abcd1-xyz

ikibria@DESKTOP-OPJUB1R:~$ rm *xyz
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 4
-rw-r--r-- 1 ikibria ikibria 4096 May 19 19:09 wildcard.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch abcd{1..5}-xyz
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 4
-rw-r--r-- 1 ikibria ikibria 4096 May 19 19:09 wildcard.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:11 abcd5-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:11 abcd4-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:11 abcd3-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:11 abcd2-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:11 abcd1-xyz

ikibria@DESKTOP-OPJUB1R:~$ ls -ltr ?bc*
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:11 abcd5-xyz
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:11 abcd4-xyz
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:11 abcd3-xyz
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:11 abcd2-xyz
-rw-r--r-- 1 ikibria ikibria 0 May 19 19:11 abcd1-xyz

ikibria@DESKTOP-OPJUB1R:~$ ls -ltr *[bcd]*
-rw-r--r-- 1 ikibria ikibria 4096 May 19 19:09 wildcard.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:11 abcd5-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:11 abcd4-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:11 abcd3-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:11 abcd2-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:11 abcd1-xyz

ikibria@DESKTOP-OPJUB1R:~$ ls -ltr *[bcd]* | more
-rw-r--r-- 1 ikibria ikibria 4096 May 19 19:09 wildcard.log
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:11 abcd5-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:11 abcd4-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:11 abcd3-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:11 abcd2-xyz
-rw-r--r-- 1 ikibria ikibria    0 May 19 19:11 abcd1-xyz
```
```
ikibria@DESKTOP-OPJUB1R:~$ rm *xy*
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 4
-rw-r--r-- 1 ikibria ikibria 4096 May 19 19:09 wildcard.log
```
**[The End]**