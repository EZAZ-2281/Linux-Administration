# Add Text to File - Part 02

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ ls -la
total 104
drwxr-xr-x  5 ikibria ikibria  4096 May 21 10:59 .
drwxr-xr-x  3 root    root     4096 May 18 20:22 ..
-rw-------  1 ikibria ikibria  6762 May 21 10:44 .bash_history
-rw-r--r--  1 ikibria ikibria   220 May 18 20:22 .bash_logout
-rw-r--r--  1 ikibria ikibria  3771 May 18 20:22 .bashrc
drwx------  2 ikibria ikibria  4096 May 18 20:22 .cache
-rw-r--r--  1 ikibria ikibria 12288 May 20 21:07 .dhaka.swp
drwxr-xr-x  2 ikibria ikibria  4096 May 18 20:22 .landscape
-rw-r--r--  1 ikibria ikibria     0 May 21 08:57 .motd_shown
-rw-r--r--  1 ikibria ikibria 12288 May 20 21:11 .one.swp
-rw-r--r--  1 ikibria ikibria   807 May 18 20:22 .profile
-rw-r--r--  1 ikibria ikibria     0 May 18 20:24 .sudo_as_admin_successful
-rw-r--r--  1 ikibria ikibria 12288 May 20 21:08 .two.swp
-rw-------  1 ikibria ikibria  4888 May 20 21:11 .viminfo
-rw-r--r--  1 ikibria ikibria  2917 May 21 10:43 addtexttofile.log
-rw-r--r--  1 root    root        9 May 20 21:19 cumilla
-rw-rw-r--+ 1 ikibria ikibria     0 May 20 21:00 dhaka
drwxr-xr-x  2 ikibria ikibria  4096 May 20 20:06 folder1
-rw-r--r--  1 ikibria ikibria     6 May 20 21:11 one
-rw-r--r--  1 ikibria ikibria    56 May 21 10:42 pen
-rw-r--r--  1 ikibria ikibria   556 May 21 10:43 pen2
-r-x--x--x  1 ikibria ikibria     0 May 20 20:23 sam
-rw-r--r--  1 ikibria ikibria     0 May 19 19:43 three
-rw-r--r--  1 ikibria ikibria     0 May 19 19:43 two
-rw-r--r--  1 ikibria ikibria     0 May 21 10:59 writetexttofile2.log
ikibria@DESKTOP-OPJUB1R:~$
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch badda
ikibria@DESKTOP-OPJUB1R:~$ ls -la > badda
ikibria@DESKTOP-OPJUB1R:~$ cat badda
total 104
drwxr-xr-x  5 ikibria ikibria  4096 May 21 11:01 .
drwxr-xr-x  3 root    root     4096 May 18 20:22 ..
-rw-------  1 ikibria ikibria  6762 May 21 10:44 .bash_history
-rw-r--r--  1 ikibria ikibria   220 May 18 20:22 .bash_logout
-rw-r--r--  1 ikibria ikibria  3771 May 18 20:22 .bashrc
drwx------  2 ikibria ikibria  4096 May 18 20:22 .cache
-rw-r--r--  1 ikibria ikibria 12288 May 20 21:07 .dhaka.swp
drwxr-xr-x  2 ikibria ikibria  4096 May 18 20:22 .landscape
-rw-r--r--  1 ikibria ikibria     0 May 21 08:57 .motd_shown
-rw-r--r--  1 ikibria ikibria 12288 May 20 21:11 .one.swp
-rw-r--r--  1 ikibria ikibria   807 May 18 20:22 .profile
-rw-r--r--  1 ikibria ikibria     0 May 18 20:24 .sudo_as_admin_successful
-rw-r--r--  1 ikibria ikibria 12288 May 20 21:08 .two.swp
-rw-------  1 ikibria ikibria  4888 May 20 21:11 .viminfo
-rw-r--r--  1 ikibria ikibria  2917 May 21 10:43 addtexttofile.log
-rw-r--r--  1 ikibria ikibria     0 May 21 11:01 badda
-rw-r--r--  1 root    root        9 May 20 21:19 cumilla
-rw-rw-r--+ 1 ikibria ikibria     0 May 20 21:00 dhaka
drwxr-xr-x  2 ikibria ikibria  4096 May 20 20:06 folder1
-rw-r--r--  1 ikibria ikibria     6 May 20 21:11 one
-rw-r--r--  1 ikibria ikibria    56 May 21 10:42 pen
-rw-r--r--  1 ikibria ikibria   556 May 21 10:43 pen2
-r-x--x--x  1 ikibria ikibria     0 May 20 20:23 sam
-rw-r--r--  1 ikibria ikibria     0 May 19 19:43 three
-rw-r--r--  1 ikibria ikibria     0 May 19 19:43 two
-rw-r--r--  1 ikibria ikibria     0 May 21 10:59 writetexttofile2.log
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr badda
-rw-r--r-- 1 ikibria ikibria 1521 May 21 11:01 badda
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr /root
ls: cannot open directory '/root': Permission denied

ikibria@DESKTOP-OPJUB1R:~$ ls -ltr /root 2> badda2
ikibria@DESKTOP-OPJUB1R:~$ cat badda2
ls: cannot open directory '/root': Permission denied


ikibria@DESKTOP-OPJUB1R:~$ telnet localhost
Trying 127.0.0.1...
telnet: Unable to connect to remote host: Connection refused
ikibria@DESKTOP-OPJUB1R:~$ telnet localhost 2> last
Trying 127.0.0.1...
ikibria@DESKTOP-OPJUB1R:~$ cat last
telnet: Unable to connect to remote host: Connection refused
```
```
ikibria@DESKTOP-OPJUB1R:~$ tenet locahost 2>> badda
ikibria@DESKTOP-OPJUB1R:~$ cat badda

Command 'tenet' not found, did you mean:

  command 'telnet' from deb telnet (0.17-41.2build1)
  command 'telnet' from deb inetutils-telnet (2:1.9.4-11ubuntu0.1)
  command 'telnet' from deb telnet-ssl (0.17.41+0.2-3.2build1)

Try: sudo apt install <deb name>

ikibria@DESKTOP-OPJUB1R:~$ cat badda

Command 'tenet' not found, did you mean:

  command 'telnet' from deb telnet (0.17-41.2build1)
  command 'telnet' from deb inetutils-telnet (2:1.9.4-11ubuntu0.1)
  command 'telnet' from deb telnet-ssl (0.17.41+0.2-3.2build1)

Try: sudo apt install <deb name>

ikibria@DESKTOP-OPJUB1R:~$ 
```
**[The End]**