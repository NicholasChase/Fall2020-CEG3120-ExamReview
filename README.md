# Fall2020-CEG3120-ExamReview
Exam review for CEG3120 for Fall 2020

Recommendation: since filling out every topic would get ugly, I recommend creating a separate page for each topic.

# Midterm Review Outline for Fall 2020

## Git / GitHub

- add: git add [file-name]
- commit: git commit 
- push: git push
- pull: git pull
- clone vs fork: <br>FORK:  A fork is a copy of a repository that allows you to freely experiment with changes without affecting the original project. A forked repository differs from a clone in that a connection exists between your fork and the original repository itself. In this way, your fork acts as a bridge between the original repository and your personal copy where you can contribute back to the original project using Pull Requests
<br>CLONE: When you create a new repository on GitHub, it exists as a remote 63 location where your project is stored. You can clone your repository to create a local copy on your computer so that you can sync between both the local and remote locations of the project.<br>
Unlike forking, you won’t be able to pull down changes from the original repository you cloned from, and if the project is owned by someone else you won’t be able to contribute back to it unless you are specifically invited as a collaborator 49. Cloning is ideal for instances when you need a way to quickly get your own copy of a repository where you may not be contributing to the original project.
- branch: git branch [Name of branch]
- checkout: git checkout [branch name]
- merge conflicts: Merge conflicts happen when you merge branches that have competing commits, and Git needs your help to decide which changes to incorporate in the final merge.
- stashing: git stash
- clean vs reset:<br> CLEAN: Untracked files are removed but modified files are unchanged <br> RESET: Changes to modified files are discarded but untracked files are untouched:
- GitHub issues:
- GitHub pull requests:

## Linux

- file & directory permissions: chmod 777: enables all permisions. <br>
Read: The capability to read contents. This is expressed as either the number 4 or letter r.<br>
Write: The capability to write or modify. This is expressed as either the number 2 or letter w.<br>
Execute: The capability to execute. This is expressed as either the number 1 or letter x.<br>
This is a breakdown of the combinations possible and the permissions they apply.<br>

7 = 4 + 2 + 1 (read/write/execute)<br>

6 = 4 + 2 (read/write)<br>

5 = 4 + 1 (read/execute)<br>

4 = 4 (read)<br>

3 = 2 + 1 (write/execute)<br>

2 = 2 (write)<br>

1 = 1 (execute)<br>

- ownership & groups: 
- PATH manipulation: File path manipulation vulnerabilities arise when user-controllable data is placed into a file or URL path that is used on the server to access local resources, which may be within or outside the web root.
- File System - what to expect in root folders
  - /etc/: The /etc folder comprises all system-wide configuration files and some shell scripts that are executed during the system boot. All files here are text files, so they are human readable.
  - /var/: The /var contains files that are of variable content, so their content is not static and it constantly changes. For example, this is where the log files are stored. If you don’t know, a log file is a file that records all events happening in your system while it is running. These log files often help to find out if something is not working correctly in your system.
  - /proc/: This is a virtual file-system maintained by the Linux kernel. Usually, you do not touch anything in this folder. It is needed only for the kernel to run different processes.
  - /bin/: The /bin folder contains programs that are essential for the system to boot and run. So, if you destroy this folder, your system won’t boot and run.
  - /sbin/: Similar to /bin this folder contains binaries for essential system tasks but they are meant to be run by the super user, in other words, the administrator of the system.
  - /boot/: It is easy to guess from the name. This folder is needed to boot your system. It contains the Linux kernel, initial RAM disk image for drives need at boot time, and the bootloader.
  - /home/: The home directory contains a home folder for each regular user on your Linux system. For example, I have tow folders in my /home folder. ALU is my home folder. The second folder belongs to another user, whom I named User2. So, the home folder of every user is named by its username.
  - /dev/: Here, I need to introduce another important concept of Linux – everything is a file. The /dev folder contains files for all devices your Linux is able to recognize.
- User / group management
  - Configuration files to note:
    - /etc/passwd , /etc/group, /etc/shadow
- Service management
  - systemctl
- System logs
  - Log files can cause disk bloat
  - journalctl
    - Find user associated logs
    - Find service related logs

## IT Knowledge

- Partition tables, partitions, filesystems
- Mounting partition(s)
  - Role of /etc/fstab
- RAID 0, 1, 5, 6
  - Given situation, which RAID would you recommend?
- ~~Backups & Imaging~~
- cronjobs
  - Where to add a cronjob - crontab
  - Format of a cronjob

## Networking

- dotted quad (format of IPv4 address)
- host
- subnet
  - Network prefix
  - Subnet mask
  - CIDR notation (substitute for long form subnet mask)
- gateway
- routing
  - Read a routing table for where traffic will be routed
- MAC addresses
  - arp table associates MAC with IP
- Hardware interface names (common)
  - eth0, wifi0 / wlan0, lo
- DNS
  - Local hostname resolution
    - Role of /etc/hosts
    - Role of /etc/resov.conf
- Ports (common)
  - 22 (SSH), 80 (HTTP), 443 (HTTPS)
  - Read output of netstat with flags (-n -t -l)
- What an IP address tells you about the network:
  - Private network prefixes:
    - 10.0.0.0/8
    - 192.168.0.0/16
    - 172.16.0.0/12
  - Local network prefixes:
    - 127.0.0.0/8
- Router (as separate hardware):
  - NAT
  - DHCP
- Firewall
  - INPUT, OUTPUT, FORWARD chains
  - Can be managed at router level or host level
  - Host level management in Linux: iptables
  - Packet is blocked by first rule that matches in chain
- Forward proxy vs VPN
- Reverse proxies:
  - Caching
  - Load balancing (web servers)
    - Monitor services?
    - Allocation strategies
    - Connection maintainence
    - Session persistence

## System level process control

- Background processes
  - move to background
  - bring to foreground
- User generated process independent of terminal connection
  - nohup
  - screen

## Bash

- IO redirection
- Different types of quotes
- ~/.bashrc vs ~/.profile
- source vs ./ vs running script using name
- Variables and accessing variable values
- Use arguments
  - In a script
  - In a script function
- Conditionals (using the `test` command)
- if statements
- functions
- ~~Regular expressions~~

## SSH

- keys (private vs public)




-https://www.baeldung.com/linux/cd-command-bash-script
-https://www.howtogeek.com/177621/the-beginners-guide-to-iptables-the-linux-firewall/

