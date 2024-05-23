# combine and spilit

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch country
ikibria@DESKTOP-OPJUB1R:~$ echo "bangladesh" > country
ikibria@DESKTOP-OPJUB1R:~$ echo "japan" >> country
ikibria@DESKTOP-OPJUB1R:~$ echo "canada" >> country
ikibria@DESKTOP-OPJUB1R:~$ echo "finland" >> country
ikibria@DESKTOP-OPJUB1R:~$ echo "turky" >> country
ikibria@DESKTOP-OPJUB1R:~$ cat country
bangladesh
japan
canada
finland
turky
ikibria@DESKTOP-OPJUB1R:~$ cat country | wc -l
5
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch separate
ikibria@DESKTOP-OPJUB1R:~$ split -l 2 country separate
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 64
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria    0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 one
drwxr-xr-x 2 ikibria ikibria 4096 May 21 19:30 savar
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:34 japan
-rw-r--r-- 1 ikibria ikibria 8192 May 21 19:34 typescript
drwxr-xr-x 2 ikibria ikibria 4096 May 22 10:06 folder-one
-rw-r--r-- 1 ikibria ikibria   38 May 23 09:35 superman1
-rw-r--r-- 1 ikibria ikibria   25 May 23 09:35 superman2
-rw-r--r-- 1 ikibria ikibria 8383 May 23 10:27 tar-gzip-gunzip.log
-rw-r--r-- 1 ikibria ikibria   30 May 23 10:36 captain
-rw-r--r-- 1 ikibria ikibria 1857 May 23 10:38 truncate.log
-rw-r--r-- 1 ikibria ikibria    0 May 23 14:02 combine-and-split.log
-rw-r--r-- 1 ikibria ikibria   38 May 23 14:03 country
-rw-r--r-- 1 ikibria ikibria    0 May 23 14:05 separate
-rw-r--r-- 1 ikibria ikibria    6 May 23 14:05 separateac
-rw-r--r-- 1 ikibria ikibria   15 May 23 14:05 separateab
-rw-r--r-- 1 ikibria ikibria   17 May 23 14:05 separateaa
```
```
ikibria@DESKTOP-OPJUB1R:~$ cat separateaa
bangladesh
japan
ikibria@DESKTOP-OPJUB1R:~$ cat separateab
canada
finland
ikibria@DESKTOP-OPJUB1R:~$ cat separateac
turky
ikibria@DESKTOP-OPJUB1R:~$ exit
```