## User Permissions

Objectif : At the end of this session, i should be able to manage users and files permissions in linux

----

in linux, users has differnts permissions on files according to thier groups roles

- x denote execution
- w denote write
- r denote read

a user has the right to execution, writing, and reading if the file has all this three permissions (r,w,x)

----

commands for user and permissions
- chmod : change file permission. e.g chmod -r file.txt
- chown : change file owner. e.g chown <fileDirectory> wilfrid

## MINDSET TO HAVE

when dealing with user and permission, i think like such:
- who need permission ?
- for what ?
- How (read, write, execute)
- where which directory (home, etc)
- why (role, service, task)

the answer to this questions will let me know the permission type of user to create.

### I. Creating user when and why

in linux, a user has a unique name. the magic word `useradd`

1. create a simple user with no work dir

cases to create a simple non directory user :
 - no login user,
 - automation user,
 - service user 
 - user not storing files
 - restricted mood user

cmd : sudo useradd <userUniqueName>. (this will create a no shell, directory, less permission user. very goog for background tasks)

2. create a normal user with file directory

cases to create a normal user with directory when we want a user to login and have particular permissions. e.g : developper, student, teacher etc

cmd : `sudo useradd -m -s /bin/bash` <userUniqueeName>

this is perfect for real login session

3. Restricted user

we create restricted user when we need a user with no login session. this is particulary for system services such as database, server etc

cmd: `sudo useradd -r -s /usr/sbin/nologin <userServiceUniqueName>`.

this will create a no shell, no login user with a minimum priviledge.

### II. Group creation

we usaully create groups to ease user permissions, clean secure access control and roles (dev, finance, etc ) management.

cmd : 
- create group : `sudo groupadd <groupNAme>`
- add user to a group : `sudo usermod -aG <groupName> <existingUserName>`
- see all users : `cat /etc/passwd` || `cut -d: f1 /etc:passwd`
- see all group : `cat /etc/group` || `cut -d: -f1 /etc/group`
- see user of particular group : `getent group <groupName>`
- create sudo user : `sudo usermod -aG sudo <userName>`



### III. Permisson (chmod). When and Why

cases to use chmod

- restrict user access in a file,
- secure a file
- avoid execution from users etc

the differents roles are R = 4, W = 2, X = 1

a file has three repartitions : owner, group, and others

e.g test.sh = rwx-rw-r-- (764) is interpreted as the owner has all access, group has read and write permissions, while others has read permission only

1. making fiel executable : chmod +x <filename>
2. secure private file : chmod 600 <fileName>
3. complet folder with full permissions : chmod chmod -R <role(e.g: 770)> <folderNAme>

### IV. Ownership (chown, chgrp) when and why

in linux we can grant ownership of folders, files

- in case i need a file to belong to a particular group  user, i can grant them ownership of  file or folder. 
- we also use it to resolve permission denied messages 
- create a shared folder, file

1. give ownership to user : `sudo chown <userName> <fileName>`
2. ownership to group : `sudo chgrp <groupName> <fileDirectory>`
3. changing bob user and group : `sudo chown user:group filedirectory`

note : tha above command ownership of the identified fileDirectory and not the content. add `-R` to include the content. e.g : `sudo chown -R user fileDirectory` || `sudo chgrp -R group fileDirectory`


### V. Attributes (usermod)

usermod command is user to modify user data

cases :
- add user to a group : `sudo usermod -aG groupName userName`
- give user admin priviledge : `sudo usermod -aG sudo userName`
- lock/unlock user : `sudo usermod -L userName`
- to rename the user 
etc








