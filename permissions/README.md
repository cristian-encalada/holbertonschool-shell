# Shell Permissions Project  
> Repository created to work on shell permissions tasks  
> Holberton Dev Bootcamp - Montevideo  <br /> \
##Learned Topics  
* Permissions (chmod, sudo, su, chown, chgrp)
* How to create users and groups <br /> \
##Tasks completed
- [x] [0-iam_betty](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/0-iam_betty)
	- Script that switches the current user to the user betty.
- [x] [1-who_am_i](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/1-who_am_i)
	- Script that prints the effective username of the current user.
- [x] [2-groups](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/2-groups)
	- Script that prints all the groups the current user is part of.
- [x] [3-new_owner](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/3-new_owner)    
	- Script that changes the owner of the file hello to the user betty.
- [x] [4-empty](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/4-empty)    
	- Script that creates an empty file called hello. 
- [x] [5-execute](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/5-execute)
	- Script that adds execute permission to the owner of the file hello.
- [x] [6-multiple_permissions](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/6-multiple_permissions)
	- Script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello.
- [x] [7-everybody](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/7-everybody)
	- Script that adds execution permission to the owner, the group owner and the other users, to the file hello
- [x] [8-James_Bond](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/8-James_Bond)
	- Script that sets the permission to the file hello as follows:
		- Owner: no permission at all
		- Group: no permission at all
		- Other users: all the permissions
- [x] [9-John_Doe](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/9-John_Doe)
	- Script that sets the mode of the file hello to this:
		- ```-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello```
- [x] [10-mirror_permissions](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/10-mirror_permissions)
	- Script that sets the mode of the file hello the same as olleh’s mode. Both files will be in the working directory.
- [x] [11-directories_permissions](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/11-directories_permissions)
	- Script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed..
- [x] [12-directory_permissions](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/12-directory_permissions)
	- Script that creates a directory called my_dir with permissions 751 in the working directory.
- [x] [13-change_group](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/13-change_group)
	- Script that changes the group owner to school for the file hello.
- [x] [14-change_owner_and_group](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/14-change_owner_and_group)
	- Script that changes the owner to vincent and the group owner to staff for all the files and directories in the working directory.
- [x] [15-symbolic_link_permissions](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/15-symbolic_link_permissions)
	- Script that changes the owner and the group owner of _hello to vincent and staff respectively.
		- The file _hello is in the working directory
		- The file _hello is a symbolic link
- [x] [16-if_only](https://github.com/cristian-encalada/holbertonschool-shell/blob/master/permissions/16-if_only)
	- Script that changes the owner of the file hello to vincent only if it is owned by the user guillaume. The file hello will be in the working directory.
