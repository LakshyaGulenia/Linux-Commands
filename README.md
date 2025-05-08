
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

## Networking
11. **ping** - `ping google.com` (check connectivity).
12. **ip addr** - `ip addr` (show network config).

## File Content
13. **cat** - `cat app.log` (view file).
14. **grep** - `grep "error" app.log` (search text).

## Permissions
15. **chmod** - `chmod 644 app.conf` (change permissions).
