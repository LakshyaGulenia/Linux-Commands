
# Linux Commands Overview

Linux is an operating system, and Linus works on its kernel. The kernel is the heart of Linux, and it is open source.

## Basic Linux Commands

- **whoami**  
  Used to check which user you are currently using.

- **pwd**  
  Used to check which directory you are currently in.

- **touch**  
  This command is used to create a new file.

- **mkdir**  
  Used to create a new folder.

- **cd**  
  Used to change directory or get inside a folder.

- **cd ..**  
  Moves one directory back (to the parent directory).

- **mv ../filename .**  
  The first `..` refers to the source directory, and the second `.` refers to the current directory. This command is used to move files and rename file.


# Additional Linux Commands & Shell Scripting

## Basic Linux Commands

- **sudo usermod -aG docker $USER**  
  Used to give permission 
  
- **rm (filename)**  
  Used to delete a file.

- **rm -rf(directoryname) '-r stands for (Recursive)It allows the removal of directories and all their subdirectories (i.e., deletes everything inside).'**  
  Used to delete a directory.

- **man (command name)**  
  Used to get the help manual for a command.

- **cp (source) (destination)**  
  Used to copy files.

- **sudo scp -i (key name) (folder name) (EC2 SSH link):(path name)**  
  Used to securely copy files to an EC2 instance using a private key.

- **script vs programming**  
  Refers to the difference between writing scripts (which automate tasks) and full-fledged programs (which solve complex problems).

- **which bash**  
  Used to check the path of the bash shell.

- **.sh**  
  Shell script file extension.

- **bash (file name)**  
  Used to run a shell script.

- **chmod 777 (script file name)**  
  Used to change permissions in Linux, making the file readable, writable, and executable by everyone.

- **./(script file name)**  
  Used to execute `.sh` files.

## Sample Shell Script 1

```bash
#!/bin/bash

echo "my name is Lakhu"
#echo  $BASH

name="Lakshya"
echo "Hello ${name}, please enter your age"
read age

echo "My age is ${age}"

echo "sub: hello, I am $1"

sleep 2

echo "me: yooooo"

sleep 2

echo "sub:xyz"
```

## Sample Shell Script 2

```bash
#!/bin/bash

if [ "$1" = "Like" ]
then
 echo "hey"
else
 echo "okay"
fi
```

### To execute:
```bash
./(file_name)
```
If you pass "Like" as an argument, it will print "hey". Otherwise, it will print "okay".

# Linux Commands for DevOps Intern Interview at CloudAstra Technologies

Essential Linux commands for a DevOps Intern interview at CloudAstra Technologies, Noida. Tailored for freshers with no real-world experience, focusing on cloud and web app tasks.

## File and Directory Management
1. **ls** - `ls -l` (list files, detailed).
17. **ls -a** - `ls -a` (list hidden files,detail).
2. **cd** - `cd /var/log` (change directory).
3. **pwd** - `pwd` (show current directory).
4. **cp** - `cp app.conf app.conf.bak` (copy file).
5. **mv** - `mv app.conf /etc/app/` (move/rename).
6. **rm** - `rm -r temp/` (delete file/directory).

## System Monitoring
7. **top** - `top` (real-time process monitoring).
8. **ps** - `ps aux` (list processes).
9. **free** - `free -m` (memory usage).
10. **kill** - `kill 1234` (terminate process).
16. **df** - `df -h` (used to check disc space -h is for for readability).

## Networking
11. **ping** - `ping google.com` (check connectivity).
12. **ip addr** - `ip addr` (show network config).

## File Content
13. **cat** - `cat app.log` (view file).
14. **grep** - `grep "error" app.log` (search text).

## Permissions
15. **chmod** - `chmod 644 app.conf` (change file permissions.777 = read/write/execute for all).
18. **su - username** - `su - username` (switch between users in linux).

# Linux Directory Structure: Where Files Are Stored

## Core System Directories
| Directory      | Purpose                                                                 | Key Contents Example                     |
|----------------|-------------------------------------------------------------------------|------------------------------------------|
| `/`            | Root directory (base of filesystem)                                     | All other directories branch from here   |
| `/bin`         | Essential user command binaries                                         | `ls`, `cp`, `bash`                       |
| `/etc`         | System-wide configuration files                                         | `passwd`, `nginx.conf`, `hosts`          |
| `/home`        | User personal directories (one subdir per user)                         | `/home/username/Downloads`, `.bashrc`    |
| `/var`         | Variable data (logs, caches, etc.)                                      | `/var/log`, `/var/cache`                 |
| `/tmp`         | Temporary files (cleared on reboot)                                     | Runtime temp files                       |

## Special-Purpose Directories
| Directory      | Purpose                                                                 |
|----------------|-------------------------------------------------------------------------|
| `/root`        | Home directory for root user (not to be confused with `/`)              |
| `/opt`         | Optional/third-party software                                           |
| `/usr`         | Read-only user utilities and apps (`/usr/bin`, `/usr/lib`, etc.)        |
| `/dev`         | Device files (disks, terminals, etc.)                                   |
| `/proc`        | Virtual filesystem for process/kernel info                              |
| `/mnt`         | Temporary mount points for external filesystems                         |

## User Data Locations
- **Personal Files**: `/home/username/` (e.g., `/home/alice/Documents`)
- **System Configs**: `/etc/`
- **Logs**: `/var/log/` (e.g., `/var/log/nginx/error.log`)
- **Installed Programs**:  
  - System-wide: `/usr/bin/`  
  - User-space: `~/.local/bin/` (hidden directory in home)

> 💡 **Note**: Use `ls -l /` to see top-level directories. Hidden files (starting with `.`) are in home directories (e.g., `~/.ssh/`).

