# tee command 

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch practice-tee
ikibria@DESKTOP-OPJUB1R:~$ echo "This is first line" > practice-tee
ikibria@DESKTOP-OPJUB1R:~$ cat practice-tee
This is first line
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr practice-tee
-rw-r--r-- 1 ikibria ikibria 19 May 21 11:14 practice-tee
ikibria@DESKTOP-OPJUB1R:~$
```
```
ikibria@DESKTOP-OPJUB1R:~$ echo "This is another line" | tee practice-tee
This is another line
ikibria@DESKTOP-OPJUB1R:~$ echo "This is another line2" || tee practice-tee
This is another line2
ikibria@DESKTOP-OPJUB1R:~$ cat practice-tee
This is another line
ikibria@DESKTOP-OPJUB1R:~$ echo "this is another line3" | tee -a practice-tee
this is another line3
ikibria@DESKTOP-OPJUB1R:~$ cat practice-tee
This is another line
this is another line3
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr | tee practice-tee-2
total 24
drwxr-xr-x 2 ikibria ikibria  4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria     0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria  2917 May 21 10:43 addtexttofile.log
-rw-r--r-- 1 ikibria ikibria 11343 May 21 11:07 writetexttofile2.log
-rw-r--r-- 1 ikibria ikibria     0 May 21 11:14 tee.log
-rw-r--r-- 1 ikibria ikibria    43 May 21 11:17 practice-tee
-rw-r--r-- 1 ikibria ikibria     0 May 21 11:19 practice-tee-2
ikibria@DESKTOP-OPJUB1R:~$ cat practice-tee-2
total 24
drwxr-xr-x 2 ikibria ikibria  4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria     0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria  2917 May 21 10:43 addtexttofile.log
-rw-r--r-- 1 ikibria ikibria 11343 May 21 11:07 writetexttofile2.log
-rw-r--r-- 1 ikibria ikibria     0 May 21 11:14 tee.log
-rw-r--r-- 1 ikibria ikibria    43 May 21 11:17 practice-tee
-rw-r--r-- 1 ikibria ikibria     0 May 21 11:19 practice-tee-2
```
```
ikibria@DESKTOP-OPJUB1R:~$ ls -ltr | tee file1 file2
total 28
drwxr-xr-x 2 ikibria ikibria  4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria     0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria  2917 May 21 10:43 addtexttofile.log
-rw-r--r-- 1 ikibria ikibria 11343 May 21 11:07 writetexttofile2.log
-rw-r--r-- 1 ikibria ikibria     0 May 21 11:14 tee.log
-rw-r--r-- 1 ikibria ikibria    43 May 21 11:17 practice-tee
-rw-r--r-- 1 ikibria ikibria   432 May 21 11:19 practice-tee-2
-rw-r--r-- 1 ikibria ikibria     0 May 21 11:20 file2
-rw-r--r-- 1 ikibria ikibria     0 May 21 11:20 file1
ikibria@DESKTOP-OPJUB1R:~$ cat file1
total 28
drwxr-xr-x 2 ikibria ikibria  4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria     0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria  2917 May 21 10:43 addtexttofile.log
-rw-r--r-- 1 ikibria ikibria 11343 May 21 11:07 writetexttofile2.log
-rw-r--r-- 1 ikibria ikibria     0 May 21 11:14 tee.log
-rw-r--r-- 1 ikibria ikibria    43 May 21 11:17 practice-tee
-rw-r--r-- 1 ikibria ikibria   432 May 21 11:19 practice-tee-2
-rw-r--r-- 1 ikibria ikibria     0 May 21 11:20 file2
-rw-r--r-- 1 ikibria ikibria     0 May 21 11:20 file1
ikibria@DESKTOP-OPJUB1R:~$ cat file2
total 28
drwxr-xr-x 2 ikibria ikibria  4096 May 20 20:06 folder1
-r-x--x--x 1 ikibria ikibria     0 May 20 20:23 sam
-rw-r--r-- 1 ikibria ikibria  2917 May 21 10:43 addtexttofile.log
-rw-r--r-- 1 ikibria ikibria 11343 May 21 11:07 writetexttofile2.log
-rw-r--r-- 1 ikibria ikibria     0 May 21 11:14 tee.log
-rw-r--r-- 1 ikibria ikibria    43 May 21 11:17 practice-tee
-rw-r--r-- 1 ikibria ikibria   432 May 21 11:19 practice-tee-2
-rw-r--r-- 1 ikibria ikibria     0 May 21 11:20 file2
-rw-r--r-- 1 ikibria ikibria     0 May 21 11:20 file1
ikibria@DESKTOP-OPJUB1R:~$
```
```
ikibria@DESKTOP-OPJUB1R:~$ tee --help
Usage: tee [OPTION]... [FILE]...
Copy standard input to each FILE, and also to standard output.

  -a, --append              append to the given FILEs, do not overwrite
  -i, --ignore-interrupts   ignore interrupt signals
  -p                        diagnose errors writing to non pipes
      --output-error[=MODE]   set behavior on write error.  See MODE below
      --help     display this help and exit
      --version  output version information and exit

MODE determines behavior with write errors on the outputs:
  'warn'         diagnose errors writing to any output
  'warn-nopipe'  diagnose errors writing to any output not a pipe
  'exit'         exit on error writing to any output
  'exit-nopipe'  exit on error writing to any output not a pipe
The default MODE for the -p option is 'warn-nopipe'.
The default operation when --output-error is not specified, is to
exit immediately on error writing to a pipe, and diagnose errors
writing to non pipe outputs.

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Report tee translation bugs to <https://translationproject.org/team/>
Full documentation at: <https://www.gnu.org/software/coreutils/tee>
or available locally via: info '(coreutils) tee invocation'
ikibria@DESKTOP-OPJUB1R:~$
```
```
ikibria@DESKTOP-OPJUB1R:~$ tee --version
tee (GNU coreutils) 8.30
Copyright (C) 2018 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <https://gnu.org/licenses/gpl.html>.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Written by Mike Parker, Richard M. Stallman, and David MacKenzie.
ikibria@DESKTOP-OPJUB1R:~$ exit
exit

Script done on 2024-05-21 11:22:44+06:00 [COMMAND_EXIT_CODE="0"]
ikibria@DESKTOP-OPJUB1R:~$
```
**[The End]**