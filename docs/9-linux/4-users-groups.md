# **Users & Groups**


### 1\. Users and Group Management

#### Creating Users and Groups
-   Add User: `sudo adduser username`
-   Add Group: `sudo addgroup groupname`

#### Modifying Users and Groups
-   Add User to Group: `sudo adduser username groupname`
-   Change User's Primary Group: `sudo usermod -g groupname username`

### 2\. Permissions and Ownership

Every file and directory in Linux has associated access rights, which are defined by the file's owner, the group, and others.

#### Viewing Permissions
-   List with Permissions: `ls -l`

#### Modifying Permissions
-   Change Permissions:  `chmod 755 filename`

#### Changing Ownership
-   Change Owner: `chown username:groupname filename`
  
#### File Permissions and Ownership
- Change file permissions.
    `chmod 755 script.sh`
- Change file owner and group.
    `chown user:usergroup file.txt`
- Change the group of a file.
    `chgrp newgroup file.txt`

#### Special Permissions
- setuid on an executable file:
    `chmod u+s /path/to/executable`
- setgid on a directory:
    `chmod g+s /path/to/directory`
- Sticky bit on a directory:
    `chmod +t /path/to/directory`

#### Permissions Numeric System Example
- Give read, write, and execute permissions to the owner, read and execute to the group, and only read to others:
    `chmod 754 file.txt`