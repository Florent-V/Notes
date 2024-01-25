<img align="middle" src="https://github.com/marwin1991/profile-technology-icons/assets/76662862/2481dc48-be6b-4ebb-9e8c-3b957efe69fa" width="300" height="300"/>

# Linux Command Line Cheat Sheet

Welcome to the Command Line Cheat Sheet! This comprehensive guide is designed to assist both beginners and experienced users in navigating the command line interface efficiently. Whether you're managing files and directories, working with permissions, or diving into network and remote connections, this cheat sheet provides a quick reference for essential commands of [Linux](https://www.linux.org).

## How to Use:

- Commands are presented in the format used in a bash terminal.
- Explanatory notes are provided in paragraph format to give you a clear understanding of each command's functionality.

## Table of Contents

- [Linux Command Line Cheat Sheet](#linux-command-line-cheat-sheet)
  - [How to Use:](#how-to-use)
  - [Table of Contents](#table-of-contents)
  - [Users](#users)
  - [Directory Navigation](#directory-navigation)
    - [Working with Files](#working-with-files)
  - [File/Directory Permissions](#filedirectory-permissions)
  - [Search](#search)
  - [Archive](#archive)
  - [Installing Programs from Packages](#installing-programs-from-packages)
  - [Processes](#processes)
  - [System](#system)
  - [Hardware Commands](#hardware-commands)
  - [Disc Management Commands](#disc-management-commands)
  - [Network](#network)
  - [Remote Connection](#remote-connection)

## Users

Detailed information about a user (uid, gid, and group).

```bash
id
```

Lists information about recent logins, including time, username, IP address, and session duration.

```bash
last
```

Displays authorized users.

```bash
who
```

Creates a group named "testgroup".

```bash
groupadd "testgroup"
```

Adds a user with the name "NewUser".

```bash
adduser NewUser
```

Deletes the user with the name "NewUser".

```bash
userdel NewUser
```

Modifies information about the user "NewUser".

```bash
usermod NewUser
```

[&#8593; Back to Top](#table-of-contents)

## Directory Navigation

Navigate to the root directory.

```bash
cd /
```

Navigate to the home directory (using the $HOME variable).

```bash
cd ~
```

Navigate to the /root directory.

```bash
cd /root
```

Move one level up.

```bash
cd ..
```

Navigate to the hidden folder .ssh.

```bash
cd /root/.ssh
```

[&#8593; Back to Top](#table-of-contents)

### Working with Files

Displays files and directories in the current folder.

```bash
ls -al
```

Shows the current working directory.

```bash
pwd
```

Creates a new directory named 'NewFolder'.

```bash
mkdir NewFolder
```

Deletes the file named 'NewFile'.

```bash
rm NewFile
```

Forcefully deletes the file named 'NewFile'.

```bash
rm -f NewFile
```

Recursively deletes the directory named 'NewFolder'.

```bash
rm -r NewFolder
```

Forcefully and recursively deletes the directory named 'NewFolder'.

```bash
rm -rf NewFolder
```

Copies the content of 'oldfile1' to 'newfile2'.

```bash
cp oldfile1 newfile2
```

Recursively copies the directory 'olddir1' to 'newdir2'. Dir2 will be created if it doesn't exist.

```bash
cp -r olddir1 newdir2
```

Renames 'oldfile1' to 'newfile2'.

```bash
mv oldfile1 newfile2
```

Creates a symbolic link to the file.

```bash
ln -s /etc/log/file logfile
```

Creates an empty file named 'newfile'.

```bash
touch newfile
```

Takes STDIN and puts it into 'newfile'.

```bash
cat > newfile
```

Outputs the content of 'newfile' one screen at a time.

```bash
more newfile
```

Outputs the first 10 lines of the file 'newfile'.

```bash
head newfile
```

Outputs the last 10 lines of 'newfile'.

```bash
tail newfile
```

Encrypts 'newfile' in gpg format using a password and saves it in the same directory.

```bash
gpg -c newfile
```

Decrypts the gpg file.

```bash
gpg newfile.gpg
```

Displays the count of bytes, words, and lines in the new file.

```bash
wc newfile
```

[&#8593; Back to Top](#table-of-contents)

## File/Directory Permissions

Sets read, write, and execute permissions for everyone who has access to the server (owner, group, others).

```bash
chmod 777 /root/ssh
```

Configures permissions as rwx for the owner and r_x for the group and others.

```bash
chmod 755 /root/ssh
```

Sets rwx for the owner and rw for the group and others.

```bash
chmod 766 /root/ssh
```

Changes the owner of newfile to newuser.

```bash
chown newuser newfile
```

Changes both the owner and group owner of newfile to newuser and newgroup.

```bash
chown newuser:newgroup newfile
```

Changes both the owner and group owner of the directory newfolder to newuser and newgroup.

```bash
chown newuser:newgroup newfolder
```

Displays the user and group owners of newfile.

```bash
stat -c "%U %G" newfile
```

[&#8593; Back to Top](#table-of-contents)

## Search

Searches for the searchargument in newfile.

```bash
grep searchargument newfile
```

Recursively searches for the searchargument in all files within the newfolder.

```bash
grep -r searchargument newfolder
```

Shows all locations of the newfile.

```bash
locate newfile
```

Finds files with names starting with searchargument in the /etc directory.

```bash
find /etc/ -name "searchargument"
```

Finds files larger than 50000k in size in the /etc directory.

```bash
find /etc/ -size +50000k
```

[&#8593; Back to Top](#table-of-contents)

## Archive

Create an archive 'archive.tar' from the file 'newfile.'

```bash
tar -cf archive.tar newfile
```

Extract the contents of the file 'archive.tar.'

```bash
tar -xf archive.tar
```

Create an archive from the /var/log/ directory and compress it using gzip.

```bash
tar -zcvf archive.tar.gz /var/log/
```

Compress the new file (it will have the extension .gz).

```bash
gzip newfile
```

[&#8593; Back to Top](#table-of-contents)

## Installing Programs from Packages

Installs an RPM package on CentOS, RHEL, etc.

```bash
rpm -i pkg_program.rpm
```

Removes an RPM package on CentOS, RHEL, etc.

```bash
rpm -e pkg_name
```

Installs a package using DNF from the repository on CentOS, RHEL, etc. YUM was previously used, but it has recently been replaced by DNF.

```bash
dnf install pkg_name
```

Installs from a DEB package on Debian, Ubuntu, Mint, etc.

```bash
dpkg -i pkg_name
```

Removes a DEB package on Debian, Ubuntu, Mint, etc.

```bash
dpkg -r pkg_name
```

Installs a package from the repository on Debian, Ubuntu, Mint, etc.

```bash
apt install pkg_name
```

Removes a package on Debian, Ubuntu, Mint, etc.

```bash
apt remove pkg_name
```

Updates the packages in the system (Debian, Ubuntu, Mint, etc.) and updates the repositories.

```bash
apt upgrade && apt update
```

[&#8593; Back to Top](#table-of-contents)

## Processes

Displays currently running processes.

```bash
ps
```

Finds the process ID (PID) of 'bash'.

```bash
ps aux | grep 'bash'
```

Maps the process with PID 11 in process memory.

```bash
pmap -x 11
```

Shows all running processes.

```bash
top
```

Terminates a process by PID.

```bash
kill pid
```

Terminates all processes with the name "process".

```bash
killall process
```

Sends a signal to a process by name.

```bash
pkill process-name
```

Sends a suspended process to the background.

```bash
bg
```

Brings a running process to the foreground.

```bash
fg
```

Brings a process named "process" to the foreground.

```bash
fg process
```

Lists files opened by processes.

```bash
lsof
```

Sets the lowest priority for a process.

```bash
renice 19 PID
```

Finds the process ID for 'bash'.

```bash
pgrep bash
```

Shows a tree-like representation of processes.

```bash
pstree
```

[&#8593; Back to Top](#table-of-contents)

## System

Displays system information.

```bash
uname
```

Shows information about the Linux kernel.

```bash
uname -r
```

Shows system uptime and average load.

```bash
uptime
```

Displays the host name.

```bash
hostname
```

Displays the host's IP address.

```bash
hostname -i
```

Shows the reboot history.

```bash
last reboot
```

Displays date and time.

```bash
date
```

Outputs and modifies date and time settings.

```bash
timedatectl
```

Displays the calendar.

```bash
cal
```

Shows users currently logged in.

```bash
w
```

Displays your username.

```bash
whoami
```

Shows information about the root user (requires installation with "apt-get install finger").

```bash
finger root
```

[&#8593; Back to Top](#table-of-contents)

## Hardware Commands

Displays system messages during boot.

```bash
dmesg
```

Shows information about the processor.

```bash
cat /proc/cpuinfo
```

Displays information about the memory.

```bash
cat /proc/meminfo
```

Shows detailed information about devices.

```bash
lshw
```

Displays information about block devices.

```bash
lsblk
```

Frees up memory: RAM and swap (switch -m for MB).

```bash
free -m
```

Shows PCI device information in a tree view.

```bash
lspci -tv
```

Displays USB devices in a tree view.

```bash
lsusb -tv
```

Shows information about BIOS devices.

```bash
dmidecode
```

Displays information about the disk.

```bash
hdparm -i /dev/xda
```

Shows read and write speed of xda.

```bash
hdparm -tT /dev/xda
```

Performs a test for bad sectors.

```bash
badblocks -s /dev/xda
```

[&#8593; Back to Top](#table-of-contents)

## Disc Management Commands

Shows free space on mounted partitions (in bytes).

```bash
df -h
```

Displays free inodes in the file system.

```bash
df -i
```

Provides information about the disk, partitions, and file system.

```bash
fdisk -l
```

Shows undistributed space on mounted partitions in MB, GB, TB.

```bash
du -sh
```

Displays all mount points.

```bash
findmnt
```

Mounts partition 1 of sdb disk to the /mnt directory.

```bash
mount /dev/sdb1 /mnt
```

[&#8593; Back to Top](#table-of-contents)

## Network

Displays the IP addresses of all available network interfaces.

```bash
ip addr show
```

Assigns the address 192.168.0.1 to the eth0 interface.

```bash
ip address add 192.168.0.1/24 dev eth0
```

Shows the IP addresses of all available network interfaces.

```bash
ifconfig
```

Sends an ICMP protocol request to connect to the node at 192.168.0.1.

```bash
ping 192.168.0.1
```

Displays information about the

```bash
whois domain
```

Retrieves DNS information about the domain.

```bash
dig domain
```

Performs reverse DNS resolution.

```bash
dig -x 192.168.0.1
```

Resolves the host address.

```bash
host serverspace.us
```

Shows local addresses.

```bash
hostname -I
```

Downloads a file.

```bash
wget file_name(link to file)
```

Displays all ports being listened to on the host (requires "apt-get install net-tools").

```bash
netstat -pnltu
```

[&#8593; Back to Top](#table-of-contents)

## Remote Connection

Connects to a remote host via ssh as the root user.

```bash
ssh root@host
```

Connects to a remote host using a non-default ssh port, specifying the user.

```bash
ssh -p port_number user@host
```

Utilizes the default connection using the current user.

```bash
ssh host
```

Uses a telnet connection (port 23).

```bash
telnet host
```

[&#8593; Back to Top](#table-of-contents)