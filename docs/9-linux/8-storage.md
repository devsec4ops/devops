# **Storage**

## **Logical Volume Manager (LVM)**

LVM is a device mapper offering logical volume management for the Linux kernel. It abstracts disk storage to allow more flexible volume management beyond traditional physical storage limitations.

## Key Concepts and Operations
1.  Physical Volume (PV): Represents a physical disk or disk partition.
2.  Volume Group (VG): A pool of storage formed by one or more physical volumes.
3.  Logical Volume (LV): A resizable, virtual disk created from space in a volume group.

### Step-by-Step Guide

1.  Creating Physical Volumes:
    -   Use `pvcreate` to initialize physical storage devices as physical volumes.
    `pvcreate /dev/sda1 /dev/sdb1`

2.  Creating a Volume Group:
    -   Combine multiple PVs into a VG using `vgcreate`.
    `vgcreate vgname /dev/sda1 /dev/sdb1`

3.  Creating Logical Volumes:
    -   Allocate space from the VG to create an LV with `lvcreate`.
    `lvcreate -L 20G -n lvname vgname`
4.  Formatting and Mounting the LV:
    -   Format the LV with a filesystem (e.g., ext4) and mount it.
    `mkfs.ext4 /dev/vgname/lvname
    mount /dev/vgname/lvname /mnt`

## **Disk Quotas**

Disk quotas restrict the amount of disk space and number of files a user or group can use, essential for managing multi-user environments.

### Configuration Steps

1.  **Enabling Quotas**:
    -   Edit `/etc/fstab` to include `usrquota` and/or `grpquota` on the desired filesystem.
    -   Remount the filesystem.
    `mount -o remount /home`
2.  **Creating Quota Databases**:
    -   Initialize quota tracking with `quotacheck`.
    `quotacheck -vugm /home`
3.  **Setting Quotas**:
    -   Use `edquota` to edit quotas for users or groups.
    `edquota -u username`

## **File System Security**

Maintaining file system security involves setting proper permissions, using Access Control Lists (ACLs), and optionally, configuring SELinux or AppArmor profiles.

1.  **Permissions and Ownership**:
    -   Regularly review and adjust file and directory permissions and ownership using `chmod` and `chown`.
  
2.  **Access Control Lists (ACLs)**:
    -   Use ACLs for finer-grained access control.
    `setfacl -m u:username:rwx /path/to/file`

3.  **Encryption**:
    -   Consider encrypting sensitive data at rest, using tools like `cryptsetup` for disk encryption.
  
4.  **SELinux**:
    -   Leverage SELinux for mandatory access control policies to limit application and user access to files.


## **Assignments**

1.  **Expand an Existing Logical Volume**:
    -   Add a new disk to your VM or physical server.
    -   Extend an existing volume group and logical volume to include this new disk space.
2.  **Implement User Quotas**:
    -   Configure user disk quotas on a system with multiple users. Test by attempting to exceed these quotas.
3.  **Secure a Directory Using ACLs**:
    -   Choose a directory used by multiple users and set up ACLs to restrict and allow specific access.

## **Interview Questions**

1.  Describe the process of extending a logical volume without causing downtime. What tools and commands would you use?
2.  How can disk quotas prevent a single user from consuming all disk resources on a shared server?
3.  Explain the difference between traditional Unix/Linux permissions and ACLs. When would you use one over the other?