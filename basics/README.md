# Shell Basics Project  
> Repository created to work on shell related tasks - 08.02.2023  <br>
Holberton Dev Bootcamp - Montevideo
## Learned Topics  
* What is the Shell
* Shell Navigation (cd, pwd, ls commands)
* Looking Around (ls, less, file commands)
* Manipulating Files (cp, mv, rm, mkdir commands)
* Working with Commands (type, which, help, man commands)
## Requirements
* Allowed editors: `vi`, `vim`, `emacs`
* All your scripts will be tested on Ubuntu 20.04 LTS
* All your scripts should be exactly two lines long (`$ wc -l file` should print 2)
* All your files should end with a new line [why?](https://unix.stackexchange.com/questions/18743/whats-the-point-in-adding-a-new-line-to-the-end-of-a-file/18789)
* The first line of all your files should be exactly `#!/bin/bash`
* A `README.md` file at the root of the repo, containing a description of the repository
* A `README.md` file, at the root of the folder of this project, describing what each script is doing
* You are not allowed to use backticks, &&, || or ;
* All your scripts must be executable. To make your file executable, use the `chmod` command: `chmod u+x file`. Later, we’ll learn more about how to utilize this command.
## Tasks completed
- [x] [0-current_working_directory](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/0-current_working_directory)
	- Script that prints the absolute path name of the current working directory.<br>
Example:
```
$ ./0-current_working_directory
/0x00-shell_basics
$
```
- [x] [1-listit](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/1-listit)
	- Script that displays the contents list of your current directory. <br>
Example:
```
$ ./1-listit
Applications    Documents   Dropbox Movies Pictures
Desktop Downloads   Library Music Public
$
```
- [x] [2-bring_me_home](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/2-bring_me_home)
	- Script that changes the working directory to the user’s home directory.<br>
Example:
```
julien@ubuntu:/tmp$ pwd
/tmp
julien@ubuntu:/tmp$ echo $HOME
/home/julien
julien@ubuntu:/tmp$ source ./2-bring_me_home
julien@ubuntu:~$ pwd
/home/julien
julien@ubuntu:~$ 
```
- [x] [3-listfiles](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/3-listfiles)    
	- Script that displays current directory contents in a long format.<br>
Example:
```
$ ./3-listfiles
total 32
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
$
```
- [x] [4-listmorefiles](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/4-listmorefiles)    
	- Script that displays current directory contents, including hidden files (starting with `.`). Use the long format. <br>
Example:
```
$ ./4-listmorefiles
total 32
drwxr-xr-x@ 6 sylvain staff 204 Jan 25 00:29 .
drwxr-xr-x@ 43 sylvain staff 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:41 4-listmorefiles
$
```
- [x] [5-listfilesdigitonly](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/5-listfilesdigitonly)
	- Script that displays current directory contents.<br>
		- Long format
		- with user and group IDs displayed numerically
		- And hidden files (starting with .) <br>
Example:
```
$ ./5-listfilesdigitonly
total 32
drwxr-xr-x@ 6 501 20 204 Jan 25 00:29 .
drwxr-xr-x@ 43 501 20 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:23 1-listfiles
-rwxr-xr-x@ 1 501 20 19 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 501 20 20 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:41 4-listmorefiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:43 5-listfilesdigitonly
$
```
- [x] [6-firstdirectory](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/6-firstdirectory)
	- Script that creates a directory named ``my_first_directory`` in the ``/tmp/`` directory.<br>
Example:
```
$ ./6-firstdirectory
$ file /tmp/my_first_directory/
/tmp/my_first_directory/: directory
$
```
- [x] [7-movethatfile](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/7-movethatfile)
	- Script that moves the file ``betty`` from ``/tmp/`` to ``/tmp/my_first_directory``.<br>
Example:
```
$ ./7-movethatfile
$ ls /tmp/my_first_directory/
betty
$
```
- [x] [8-firstdelete](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/8-firstdelete)
	- Script that deletes the file ``betty``.<br>
		- The file ``betty`` is in ``/tmp/my_first_directory``
Example:
```
$ ./8-firstdelete
$ ls /tmp/my_first_directory/
$
```
- [x] [9-firstdirdeletion](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/9-firstdirdeletion)
	- Script that deletes the directory ``my_first_directory`` that is in the ``/tmp`` directory.<br>
Example:
```
$ ./9-firstdirdeletion
$ file /tmp/my_first_directory
/tmp/my_first_directory: cannot open `/tmp/my_first_directory' (No such file or directory)
$
```
- [x] [10-back](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/10-back)
	- Script that changes the working directory to the previous one.<br>
Example:
```
julien@ubuntu:/tmp$ pwd
/tmp
julien@ubuntu:/tmp$ cd /var
julien@ubuntu:/var$ pwd
/var
julien@ubuntu:/var$ source ./10-back
/tmp
julien@ubuntu:/tmp$ pwd
/tmp
```
- [x] [11-lists](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/11-lists)
	- Script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the ``/boot`` directory (in this order), in long format.<br>
- [x] [12-file_type](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/12-file_type)
	- Script that prints the type of the file named ``iamafile``. The file ``iamafile`` will be in the ``/tmp`` directory<br>
	- Note that depending on the file, the output of your script will be different.<br>
Example:
```
ubuntu@ip-172-31-63-244:~$ ./12-file_type
/tmp/iamafile: ELF 64-bit LSB  executable, x86-64, version 1 (SYSV), dynamically linked (uses shared libs), for GNU/Linux 2.6.24, BuildID[sha1]=bd39c07194a778ccc066fc963ca152bdfaa3f971, stripped
```
- [x] [13-symbolic_link](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/13-symbolic_link)
	- Scrip that creates a symbolic link to ``/bin/ls``, named ``__ls__``<br>
Example:
```
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 144
drwxrwxr-x  2 ubuntu ubuntu   4096 Sep 20 03:24 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:24 ..
ubuntu@ip-172-31-63-244:/tmp/sym$./13-symbolic_link
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 144
drwxrwxr-x  2 ubuntu ubuntu   4096 Sep 20 03:24 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:24 ..
lrwxrwxrwx  1 ubuntu ubuntu      7 Sep 20 03:24 __ls__ -> /bin/ls
```
- [x] [14-copy_html](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/14-copy_html)
	- Script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.<br>
	- You can consider that all HTML files have the extension ``.html``
- [x] [15-lets_move](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/15-lets_move)
	- Script that moves all files beginning with an uppercase letter to the directory ``/tmp/u`` <br>
	- You can assume that the directory ``/tmp/u`` will exist when we will run your script <br>
Example:
```
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 148
drwxrwxr-x  3 ubuntu ubuntu   4096 Sep 20 03:33 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:26 ..
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 My_file
lrwxrwxrwx  1 ubuntu ubuntu      7 Sep 20 03:24 __ls__ -> /bin/ls
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 Elif_ym
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 random_file
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la /tmp/u
total 8
drwxrwxr-x 2 ubuntu ubuntu 4096 Sep 20 03:33 .
drwxrwxr-x 3 ubuntu ubuntu 4096 Sep 20 03:33 ..
ubuntu@ip-172-31-63-244:/tmp/sym$ ./15-lets_move
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 148
drwxrwxr-x  3 ubuntu ubuntu   4096 Sep 20 03:33 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:26 ..
lrwxrwxrwx  1 ubuntu ubuntu      7 Sep 20 03:24 __ls__ -> /bin/ls
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 random_file
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la /tmp/u
total 8
drwxrwxr-x 2 ubuntu ubuntu 4096 Sep 20 03:33 .
drwxrwxr-x 3 ubuntu ubuntu 4096 Sep 20 03:33 ..
-rw-rw-r-- 1 ubuntu ubuntu    0 Sep 20 03:32 My_file
-rw-rw-r-- 1 ubuntu ubuntu    0 Sep 20 03:32 Elif_ym
```
- [x] [16-clean_emacs](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/16-clean_emacs)
	- Script that deletes all files in the current working directory that end with the character ``~`` <br>
Example:
```
ubuntu@ip-172-31-63-244:/tmp/sym$ ls
main.c  main.c~  Makefile~
ubuntu@ip-172-31-63-244:/tmp/sym$ ./16-clean_emacs
ubuntu@ip-172-31-63-244:/tmp/emacs$ ls
main.c
ubuntu@ip-172-31-63-244:/tmp/emacs$
```
- [x] [17-tree](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/basics/17-tree)
	- Script that creates the directories ``welcome/``, ``welcome/to/`` and ``welcome/to/school`` in the current directory.<br>
	- You are only allowed to use two spaces (and lines) in your script, not more.<br>
Example:
```
julien@ubuntu:/tmp/h$ ls -l
total 4
-rwxrw-r-- 1 julien julien 44 Sep 20 12:09 17-tree
julien@ubuntu:/tmp/h$ wc -l 17-tree 
2 17-tree
julien@ubuntu:/tmp/h$ head -1 17-tree 
#!/bin/bash
julien@ubuntu:/tmp/h$ tr -cd ' ' < 17-tree | wc -c # you do not have to understand this yet, but the result should be 2, 1 or 0
2
julien@ubuntu:/tmp/h$ ./17-tree 
julien@ubuntu:/tmp/h$ ls
17-tree  welcome
julien@ubuntu:/tmp/h$ ls welcome/
to
julien@ubuntu:/tmp/h$ ls -l welcome/to
total 4
drwxrwxr-x 2 julien julien 4096 Sep 20 12:11 school
julien@ubuntu:/tmp/h$
```
