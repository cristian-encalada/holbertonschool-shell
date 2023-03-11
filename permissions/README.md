# Shell Permissions Project  
> Repository created to work on shell permissions tasks  <br>
Holberton Dev Bootcamp - Montevideo  
## Learned Topics  
* Permissions (chmod, sudo, su, chown, chgrp)
* How to create users and groups
## Requirements
* Allowed editors: ``vi``, ``vim``, ``emacs``
* All your scripts will be tested on Ubuntu 20.04 LTS
* All your scripts should be exactly two lines long (``$ wc -l file`` should print 2)
* All your files should end with a new line [why?](https://unix.stackexchange.com/questions/18743/whats-the-point-in-adding-a-new-line-to-the-end-of-a-file/18789)
* The first line of all your files should be exactly ``#!/bin/bash``
* A ``README.md`` file, at the root of the folder of the project, describing what each script is doing
* You are not allowed to use backticks, ``&&``, ``||`` or ``;``
* All your files must be executable
## Tasks completed
- [x] [0-iam_betty](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/0-iam_betty)
	- Script that switches the current user to the user ``betty``.
		- You should use exactly 8 characters for your command (+1 character for the new line)
		- You can assume that the user ``betty`` will exist when we will run your script <br>
Example:
```
julien@ubuntu:/tmp/h$ tail -1 0-iam_betty | wc -c
9
julien@ubuntu:/tmp/h$
```
- [x] [1-who_am_i](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/1-who_am_i)
	- Script that prints the effective username of the current user. <br>
Example:
```
julien@ubuntu:/tmp/h$ ./1-who_am_i
julien
julien@ubuntu:/tmp/h$ 
```
- [x] [2-groups](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/2-groups)
	- Script that prints all the groups the current user is part of. <br>
Example:
```
julien@ubuntu:/tmp/h$ ./2-groups
julien adm cdrom sudo dip plugdev lpadmin sambashare
julien@ubuntu:/tmp/h$ 
```
- [x] [3-new_owner](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/3-new_owner)    
	- Script that changes the owner of the file ``hello`` to the user ``betty``.<br>
Example:
```
julien@ubuntu:/tmp/h$ ls -l
total 4
-rwxrw-r-- 1 julien julien 30 Sep 20 14:23 3-new_owner
-rw-rw-r-- 1 julien julien  0 Sep 20 14:18 hello
julien@ubuntu:/tmp/h$ sudo ./3-new_owner 
julien@ubuntu:/tmp/h$ ls -l
total 4
-rwxrw-r-- 1 julien julien 30 Sep 20 14:23 3-new_owner
-rw-rw-r-- 1 betty  julien  0 Sep 20 14:18 hello
julien@ubuntu:/tmp/h$
```
- [x] [4-empty](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/4-empty)    
	- Script that creates an empty file called ``hello``. 
- [x] [5-execute](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/5-execute)
	- Script that adds execute permission to the owner of the file ``hello``.
		- The file ``hello`` will be in the working directory <br>
```
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:26 5-execute
-rw-rw-r-- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./hello
bash: ./hello: Permission denied
julien@ubuntu:/tmp/h$ ./5-execute 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:26 5-execute
-rwxrw-r-- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$
```
- [x] [6-multiple_permissions](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/6-multiple_permissions)
	- Script that adds execute permission to the owner and the group owner, and read permission to other users, to the file ``hello``.
		- The file ``hello`` will be in the working directory <br>
```
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 36 Sep 20 14:31 6-multiple_permissions
-rw-r----- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./6-multiple_permissions 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 36 Sep 20 14:31 6-multiple_permissions
-rwxr-xr-- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
- [x] [7-everybody](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/7-everybody)
	- Script that adds execution permission to the owner, the group owner and the other users, to the file ``hello``
		- The file ``hello`` will be in the working directory
		- You are not allowed to use commas for this script <br>
```
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:35 7-everybody
-rw-r----- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./7-everybody 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:35 7-everybody
-rwxr-x--x 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
- [x] [8-James_Bond](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/8-James_Bond)
	- Script that sets the permission to the file ``hello`` as follows:
		- Owner: no permission at all
		- Group: no permission at all
		- Other users: all the permissions
		- The file ``hello`` will be in the working directory You are not allowed to use commas for this script <br>
```
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:40 8-James_Bond
-rwxr-x--x 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./8-James_Bond 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:40 8-James_Bond
-------rwx 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
- [x] [9-John_Doe](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/9-John_Doe)
	- Script that sets the mode of the file ``hello`` to this: <br>
		- The file ``hello`` will be in the working directory
		- You are not allowed to use commas for this script
```
-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello
```
- [x] [10-mirror_permissions](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/10-mirror_permissions)
	- Script that sets the mode of the file ``hello`` the same as ``olleh``’s mode. Both files will be in the working directory. <br>
		- Note: the mode of ``olleh`` will not always be ``664``. Make sure your script works for any mode. <br>
Example:
```
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 42 Sep 20 14:45 10-mirror_permissions
-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello
-rw-rw-r-- 1 julien julien  0 Sep 20 14:43 olleh
julien@ubuntu:/tmp/h$ ./10-mirror_permissions 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 42 Sep 20 14:45 10-mirror_permissions
-rw-rw-r-- 1 julien julien 23 Sep 20 14:25 hello
-rw-rw-r-- 1 julien julien  0 Sep 20 14:43 olleh
julien@ubuntu:/tmp/h$ 
```
- [x] [11-directories_permissions](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/11-directories_permissions)
	- Script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed. <br>
Example:
```
julien@ubuntu:/tmp/h$ ls -l
total 20
-rwxrwxr-x 1 julien julien   24 Sep 20 14:53 11-directories_permissions
drwx------ 2 julien julien 4096 Sep 20 14:49 dir0
drwx------ 2 julien julien 4096 Sep 20 14:49 dir1
drwx------ 2 julien julien 4096 Sep 20 14:49 dir2
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./11-directories_permissions 
julien@ubuntu:/tmp/h$ ls -l
total 20
-rwxrwxr-x 1 julien julien   24 Sep 20 14:53 11-directories_permissions
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
- [x] [12-directory_permissions](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/12-directory_permissions)
	- Script that creates a directory called ``my_dir`` with permissions ``751`` in the working directory. <br>
Example:
```
julien@ubuntu:/tmp/h$ ls -l
total 20
-rwxrwxr-x 1 julien julien   39 Sep 20 14:59 12-directory_permissions
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./12-directory_permission s
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien   39 Sep 20 14:59 12-directory_permissions
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
drwxr-x--x 2 julien julien 4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
- [x] [13-change_group](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/13-change_group)
	- Script that changes the group owner to ``school`` for the file ``hello``.
		- The file ``hello`` will be in the working directory <br>
Example:
```
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien   34 Sep 20 15:03 13-change_group
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
drwxr-x--x 2 julien julien 4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ sudo ./13-change_group 
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien      34 Sep 20 15:03 13-change_group
drwx--x--x 2 julien julien    4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien    4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien    4096 Sep 20 14:49 dir2
drwxr-x--x 2 julien julien    4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 julien school   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
- [x] [14-change_owner_and_group](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/14-change_owner_and_group)
	- Script that changes the owner to ``vincent`` and the group owner to ``staff`` for all the files and directories in the working directory.<br>
```
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien   36 Sep 20 15:06 14-change_owner_and_group
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
drwxr-x--x 2 julien julien 4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ sudo ./14-change_owner_and_group 
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 vincent staff   36 Sep 20 15:06 14-change_owner_and_group
drwx--x--x 2 vincent staff 4096 Sep 20 14:49 dir0
drwx--x--x 2 vincent staff 4096 Sep 20 14:49 dir1
drwx--x--x 2 vincent staff 4096 Sep 20 14:49 dir2
drwxr-x--x 2 vincent staff 4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 vincent staff   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
- [x] [15-symbolic_link_permissions](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/15-symbolic_link_permissions)
	- Script that changes the owner and the group owner of ``_hello`` to ``vincent`` and ``staff`` respectively.
		- The file ``_hello`` is in the working directory
		- The file ``_hello`` is a symbolic link <br>
Example:
```
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien   44 Sep 20 15:12 15-symbolic_link_permissions
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
lrwxrwxrwx 1 julien julien    5 Sep 20 15:10 _hello -> hello
julien@ubuntu:/tmp/h$ sudo ./15-symbolic_link_permissions 
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien      44 Sep 20 15:12 15-symbolic_link_permissions
-rw-rw-r-- 1 julien julien      23 Sep 20 14:25 hello
lrwxrwxrwx 1 vincent  staff    5 Sep 20 15:10 _hello -> hello
julien@ubuntu:/tmp/h$ 
```
- [x] [16-if_only](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/16-if_only)
	- Script that changes the owner of the file ``hello`` to ``vincent`` only if it is owned by the user ``guillaume``.
		- The file ``hello`` will be in the working directory.<br>
Example:
```
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien    julien      47 Sep 20 15:18 16-if_only 
-rw-rw-r-- 1 guillaume julien      23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ sudo ./16-if_only 
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien      47 Sep 20 15:18 16-if_only 
-rw-rw-r-- 1 vincent  julien      23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
