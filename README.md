
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
  The first `..` refers to the source directory, and the second `.` refers to the current directory. This command is used to move files.


# Additional Linux Commands & Shell Scripting

## Basic Linux Commands

- **sudo usermod -aG docker $USER**  
  Used to give permission 
  
- **rm (filename)**  
  Used to delete a file.

- **rm -rf(directoryname)**  
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
