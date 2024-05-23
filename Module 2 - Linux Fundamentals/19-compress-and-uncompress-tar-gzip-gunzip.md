# tar gzip gunzip

```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 28
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria    0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 one
drwxr-xr-x 2 ikibria ikibria 4096 May 21 19:30 savar
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:34 japan
-rw-r--r-- 1 ikibria ikibria 8192 May 21 19:34 typescript
drwxr-xr-x 2 ikibria ikibria 4096 May 22 10:06 folder-one
-rw-r--r-- 1 ikibria ikibria   38 May 23 09:35 superman1
-rw-r--r-- 1 ikibria ikibria   25 May 23 09:35 superman2
-rw-r--r-- 1 ikibria ikibria    0 May 23 10:10 tar-gzip-gunzip.log
```
```
ikibria@DESKTOP-OPJUB1R:~$ tar cvf all-in-one.tar /home/ikibria/
tar: Removing leading `/' from member names
/home/ikibria/
/home/ikibria/superman2
/home/ikibria/.viminfo
/home/ikibria/one
/home/ikibria/superman1
/home/ikibria/.sudo_as_admin_successful
/home/ikibria/.landscape/
/home/ikibria/.landscape/sysinfo.log
/home/ikibria/.dhaka.swp
/home/ikibria/.bash_history
/home/ikibria/savar/
/home/ikibria/savar/new-two
/home/ikibria/savar/two
/home/ikibria/.cache/
/home/ikibria/.cache/motd.legal-displayed
/home/ikibria/.cache/xsel.log
/home/ikibria/folder1/
/home/ikibria/.bash_logout
/home/ikibria/.one.swp
tar: /home/ikibria/all-in-one.tar: file is the archive; not dumped
/home/ikibria/sam
/home/ikibria/.bashrc
/home/ikibria/tar-gzip-gunzip.log
/home/ikibria/.two.swp
/home/ikibria/typescript
/home/ikibria/.motd_shown
/home/ikibria/.profile
/home/ikibria/folder-one/
/home/ikibria/folder-one/character
/home/ikibria/japan
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 120
drwxr-xr-x 2 ikibria ikibria  4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria     0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria     0 May 21 19:23 one
drwxr-xr-x 2 ikibria ikibria  4096 May 21 19:30 savar
-rw-r--r-- 1 ikibria ikibria     0 May 21 19:34 japan
-rw-r--r-- 1 ikibria ikibria  8192 May 21 19:34 typescript
drwxr-xr-x 2 ikibria ikibria  4096 May 22 10:06 folder-one
-rw-r--r-- 1 ikibria ikibria    38 May 23 09:35 superman1
-rw-r--r-- 1 ikibria ikibria    25 May 23 09:35 superman2
-rw-r--r-- 1 ikibria ikibria     0 May 23 10:10 tar-gzip-gunzip.log
-rw-r--r-- 1 ikibria ikibria 92160 May 23 10:12 all-in-one.tar
```
```
ikibria@DESKTOP-OPJUB1R:~$ mkdir dir
ikibria@DESKTOP-OPJUB1R:~$ mv all-in-one.tar dir/
ikibria@DESKTOP-OPJUB1R:~$ cd dir/
ikibria@DESKTOP-OPJUB1R:~/dir$ ls -ltr
total 92
-rw-r--r-- 1 ikibria ikibria 92160 May 23 10:12 all-in-one.tar
```
```
ikibria@DESKTOP-OPJUB1R:~/dir$ tar xvf all-in-one.tar
home/ikibria/
home/ikibria/superman2
home/ikibria/.viminfo
home/ikibria/one
home/ikibria/superman1
home/ikibria/.sudo_as_admin_successful
home/ikibria/.landscape/
home/ikibria/.landscape/sysinfo.log
home/ikibria/.dhaka.swp
home/ikibria/.bash_history
home/ikibria/savar/
home/ikibria/savar/new-two
home/ikibria/savar/two
home/ikibria/.cache/
home/ikibria/.cache/motd.legal-displayed
home/ikibria/.cache/xsel.log
home/ikibria/folder1/
home/ikibria/.bash_logout
home/ikibria/.one.swp
home/ikibria/sam
home/ikibria/.bashrc
home/ikibria/tar-gzip-gunzip.log
home/ikibria/.two.swp
home/ikibria/typescript
home/ikibria/.motd_shown
home/ikibria/.profile
home/ikibria/folder-one/
home/ikibria/folder-one/character
home/ikibria/japan
```
```
ikibria@DESKTOP-OPJUB1R:~/dir$ ls -ltr
total 96
-rw-r--r-- 1 ikibria ikibria 92160 May 23 10:12 all-in-one.tar
drwxr-xr-x 3 ikibria ikibria  4096 May 23 10:15 home
ikibria@DESKTOP-OPJUB1R:~/dir$ cd home
ikibria@DESKTOP-OPJUB1R:~/dir/home$ ls -ltr
total 4
drwxr-xr-x 7 ikibria ikibria 4096 May 23 10:12 ikibria
ikibria@DESKTOP-OPJUB1R:~/dir/home$ cd ikibria/
ikibria@DESKTOP-OPJUB1R:~/dir/home/ikibria$ ls -lt
total 28
-rw-r--r-- 1 ikibria ikibria    0 May 23 10:10 tar-gzip-gunzip.log
-rw-r--r-- 1 ikibria ikibria   25 May 23 09:35 superman2
-rw-r--r-- 1 ikibria ikibria   38 May 23 09:35 superman1
drwxr-xr-x 2 ikibria ikibria 4096 May 22 10:06 folder-one
-rw-r--r-- 1 ikibria ikibria 8192 May 21 19:34 typescript
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:34 japan
drwxr-xr-x 2 ikibria ikibria 4096 May 21 19:30 savar
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 one
-r-x--x--x 1 ikibria ikibria    0 May 20 20:23 sam
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
```
```
ikibria@DESKTOP-OPJUB1R:~/dir/home/ikibria$ cd ../../
ikibria@DESKTOP-OPJUB1R:~/dir$ ls -ltr
total 96
-rw-r--r-- 1 ikibria ikibria 92160 May 23 10:12 all-in-one.tar
drwxr-xr-x 3 ikibria ikibria  4096 May 23 10:15 home
```
```
ikibria@DESKTOP-OPJUB1R:~/dir$ gzip all-in-one.tar
ikibria@DESKTOP-OPJUB1R:~/dir$ ls -ltr
total 16
-rw-r--r-- 1 ikibria ikibria 8772 May 23 10:12 all-in-one.tar.gz
drwxr-xr-x 3 ikibria ikibria 4096 May 23 10:15 home
```
We can also use `gzip -d` instead of gunzip
```
ikibria@DESKTOP-OPJUB1R:~/dir$ gunzip all-in-one.tar.gz
ikibria@DESKTOP-OPJUB1R:~/dir$ ls -ltr
total 96
-rw-r--r-- 1 ikibria ikibria 92160 May 23 10:12 all-in-one.tar
drwxr-xr-x 3 ikibria ikibria  4096 May 23 10:15 home
```
```
ikibria@DESKTOP-OPJUB1R:~/dir$ cd
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ rm dir/
rm: cannot remove 'dir/': Is a directory
ikibria@DESKTOP-OPJUB1R:~$ rm -f dir/
rm: cannot remove 'dir/': Is a directory
ikibria@DESKTOP-OPJUB1R:~$ rm -rf dir/
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr
total 32
drwxr-xr-x 2 ikibria ikibria 4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria    0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:23 one
drwxr-xr-x 2 ikibria ikibria 4096 May 21 19:30 savar
-rw-r--r-- 1 ikibria ikibria    0 May 21 19:34 japan
-rw-r--r-- 1 ikibria ikibria 8192 May 21 19:34 typescript
drwxr-xr-x 2 ikibria ikibria 4096 May 22 10:06 folder-one
-rw-r--r-- 1 ikibria ikibria   38 May 23 09:35 superman1
-rw-r--r-- 1 ikibria ikibria   25 May 23 09:35 superman2
-rw-r--r-- 1 ikibria ikibria 4096 May 23 10:15 tar-gzip-gunzip.log
ikibria@DESKTOP-OPJUB1R:~$ exit
```
**[The End]**