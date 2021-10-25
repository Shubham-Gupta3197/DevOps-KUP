**Q1. What is the GNU project?**

GNU project is a mass collaborative initiative for the development of free software. The original purpose of the GNU project was the creation of a free operating system. The OS known as Linux is based on the Linux kernel but all other components are GNU. As such, many believe that the OS should be known as GNU/Linux or GNU Linux.

**Q2. Difference between Unix and Linux?**

|**S.No** | **Key** | **Linux** | **Unix** |
|-----|-----|-------|------|
|1. | Development | Linux is open source and is developed by Linux community of developers. | Unix was developed by AT&T Bell labs and is not open source. |
|2. | GUI | Linux uses KDE and Gnome. Other GUI supported are LXDE, Xfce, Unity, Mate. | Unix was initially a command based OS. Most of the unix distributions now have Gnome. |
|3. | Usage | Linux is used in wide varieties from desktop, servers, smartphones to mainframes. | Unix is mostly used on servers, workstations or PCs. |
|4. | Supportd File systems | Ext2, Ext3, Ext4, Jfs, ReiserFS, Xfs, Btrfs. | fs, gpfs, hfs, hfs+, ufs, xfs, zfs. |
|5. | Example | Ubuntu, Debian GNU, Arch Linux, etc. | SunOS, Solaris, SCO UNIX, AIX, HP/UX, ULTRIX etc. |

**Q3. Integrity Check of BIOS?**

The first step in the Linux boot process is the BIOS which performs system integrity checks. The BIOS's main goal is to find the system bootloader. So once the BIOS boots up the hard drive, it searches for the boot block to figure out how to boot up the system.

**Q4. What is UEFI? Difference between UEFI and BIOS?**

UEFI stands for **Unified Extensible Firmware Interface**. It does the same job as a BIOS, but with one basic difference: it stores all data about initialization and startup in an .efi file, instead of storing it on the firmware.

The BIOS (basic input/output system) is a firmware component stored in nonvolatile memory, usually a flash chip.The BIOS loads the boot loader, which is the first software component loaded during the boot process. 

**Q5. What is the difference between BIOS & UEFI?**

The main difference between UEFI and boot is that the UEFI is the latest method of booting a computer that is designed to replace BIOS whcih comes with new features while the boot is the process of booting the computer using BIOS firmware.Boot is the regular method of booting the system using BIOS. In terms of feature -

1. It Supports for more than four partitions on a drive.
2. Fast booting. 
3. UEFI supports for hard drive partitions larger than 2 TB.
4. Efficient power and system management.

**Q6. When should you go for Ubuntu & when for other systems?**

Before choosing for the operating system one should keep the following points in mind :-

* Stability and Robustness
* Cost and Support
* Discontinued Products
* OS Releases 
* The packages provided by the distributors.

We can modify our own operating system according to your use-case.

**Q7. What are the various linux distributors & their uses?**

`Ubuntu -` Ubuntu is a Linux distribution based on Debian. It is developed by Canonical and a community of developers. It has 3 official editions: Desktop, Server and Core, which can either run on a computer or on a VM. More than 33% of the websites using Linux use Ubuntu, according to W3Techs data. Its growth since 2010 has been amazing. It is also a popular distribution among cloud computing projects.

`CentOS - ` CentOS is a distribution based on the source code of the commercial distribution Red Hat Enterprise Linux (RHEL). It was launched in 2004 and is backed up by a growing community. It is a safe bet for those looking for a high-quality code. But CentOS 8 will be its last version. In 2019, Red Hat announced that CentOS Linux would be replaced by CentOS Stream — an upstream development platform for RHEL. 

`Red Hat Enterprise Linux (RHEL) -` Red Hat Enterprise Linux (RHEL) is a commercial Linux distribution developed by Red Hat. It has a server version and a desktop version. As it uses open source software, published under a General Public License, they make their code available to the public via CentOS. Red Hat has sponsored the CentOS project since 2014.

`Fedora -`  Fedora is a Linux distribution developed by the Fedora Project — sponsored mainly by Red Hat, with support from other companies. It is developed and maintained by the community and it is an upstream source of the commercial RHEL distribution. Fedora usually has more modern software versions, considered as “non stable”, that are later included in RHEL. There are different Fedora editions available: Workstation, Server, CoreOS, Silverblue and IoT. Fedora Linux was launched in 2003.

**Q8. What is systemd.unit(5)?**

Man Pages are divided into 8 sections.

* User Commands : Commands that can be run from the shell by a normal user
* System Calls: Programming functions used to make calls to the Linux kernel
* C Library Functions: Programming functions that provide interfaces to specific programming libraries.
* Devices and Special Files: File system nodes that represent hardware devices or software devices.
* File Formats and Conventions: The structure and format of file types or specific configuration files.
* Games: Games available on the system
* Miscellaneous: Overviews of miscellaneous topics such as protocols, filesystems and so on.
* System administration tools and Daemons:Commands that require root or other administrative privileges to use.

**Q9. What are getty commands and uname commands?**

The getty command sets and manages terminal lines and ports. The getty command is run by the init command. The getty command is linked to the Terminal State Manager program. The Terminal State Manager program provides combined terminal control and login functions.

## Syntax
**getty** [ [ -r | -u | -U ] [ -d ] [ -H HeraldString ] [ -M motdFile ] [ -N ] ] PortName

###Flags

| Item | Description |
|------|-------------|

| -d | Provides debugging information. |
| -M | Specifies the path to an alternate message of the day file. If not specified, this value is /etc/motd by default. |
| -N | Causes getty to bypass any checking for the process ID in the /etc/utmp file. This allows a process other than the lowest login shell to exec getty. |
| -r | Makes the port available for shared (bi-directional) use. If the lock is unsuccessful, the getty command waits until the lock is available and then exits. If the lock is successful, the getty command waits for a byte of data on the port after locking the port. |
| -u | Makes the port available for shared (bi-directional) use. If the lock is unsuccessful, the getty command waits until the lock is available and then exits. |
| -U | Same as the -u flag, except getty does not wait for the lock to be available. It makes the port available regardless of the lock. |

**Uname** command is used to displays the information about the system.

**Syntax:** uname [OPTION]

1. **-a option:** It prints all the system information in the following order: Kernel name, network node hostname, kernel release date, kernel version, machine hardware name, hardware platform, operating system.
2. **-s option:** It prints the kernel name.
3. **-n option:** It prints the hostname of the network node(current computer).
4. **-r option:** It prints the kernel release date.
5. **-v option:** It prints the version of the current kernel.
6. **-m option:** It prints the machine hardware name.
7. **-p option:** It prints the type of the processor.
8. **-i option:** It prints the platform of the hardware.
9. **-o option:** It prints the name of the operating system. 

**10. What is squashfs file system?**

Squashfs is a compressed read-only file system for Linux. SquashFS brings all this to a new level. It is a read-only file system that lets you compress whole file systems or single directories, write them to other devices/partitions or to ordinary files, and then mount them directly (if a device) or using a loopback device (if it is a file).

**Q11. What are /dev/loop and /dev/tty?**

dev/loop* are loop devices making plain files accessible as block devices. They are basically used for mounting disk images.
/dev/tty stands for the controlling terminal (if any) for the current process. To find out which tty's are attached to which processes use the "ps -a" command. For the shell process we are in, /dev/tty is the terminal we are now using.

**Q12. What are Linux Signals?**

A signal is an event generated by the UNIX and Linux systems in response to some condition. Upon receipt of a signal, a process may take action.

A signal is just like an interrupt; when it is generated at the user level, a call is made to the kernel of the OS, which then acts accordingly. Two types- Maskable and Non-Maskable.

**Q13. What is the purpose of creating hidden files?**

Hidden files are used for storage of user preferences or for preservation of the state of utilities. They are created frequently by various system or application utilities. Hidden files are helpful in preventing accidental deletion of important data.

**Q14. How ext4fs is faster/better?**

ext4 file system is faster among all the ext. file system. The ext4 filesystem is also capable of performing faster file system checks than other equivalent journaling filesystems.

**Q15. What is swap & swap memory?**

`swap -` The primary function of swap space is to substitute disk space for RAM memory when real RAM fills up and more space is needed.

`swap memory -` whenever RAM runs out of memory in Linux, it borrows some memory from the secondary storage to store its inactive content. RAM finds sufficient space to hold a new process within it. Here, the borrowed space from the hard disk is called Swap Memory. In this article, we will try to learn the concept of swap memory in detail.

**Q16. How to mount a file system?**

To mount a particular file system for example

mount [OPTION...] DEVICE_NAME DIRECTORY

mount dev/sdb1 mnt/music

**Q17. Mention a ZFS use case?**

ZFS stands for Zettabyte File System. It is a local file system and logical volume manager created to direct and control the placement, storage and retrieval of data. ZFS is built into the Oracle OS and offers an ample feature set and data services free of cost. ZFS is a free open-source filesystem that can be expanded by adding hard drives to the storage pool.

**Q18. How to check the port number of a process?**

We can use the following command : - sudo netstat -ano -p tcp
			OR
use lsof -i :port number

**Q19. What is Unix Time Sharing (UTS)?**

`Unix time sharing-` allows a single system to appear to have a different host and domain name to different process.

**Q20. What are control groups?**

`Control group-` allow to relocate the resources such as CPU time, system memory, network bandwidth.

**Q21. What is the difference between sbin & usr/sbin?**

`sbin -` For binaries with superuser (root) privileges required. usable before the /usr partition is mounted. This is used for trivial binaries used in the very early boot stage or ones that you need to have available in booting single-user mode. Think of binaries like cat, ls, etc.

`usr/sbin-` Same as first, but for general system-wide binaries.

**Q22. Examples of awk, grep and sed.**

1. To print 2nd field of file

     awk '{print $2}' file.txt

2. To print josh as first name

     grep 'Josh .*' file.txt

3. To change the occurrence of josh to JOSH

     sed 's/Josh/JOSH/' file.txt

**Q23. How many tables are there in iptables?**

`iptables` contains five tables:

1. Raw is used only for configuring packets so that they are exempt from connection tracking.

2. Filter is the default table, and is where all the actions typically associated with a firewall take place.

3. Nat is used for network address translation (e.g. port forwarding).

4. Mangle is used for specialized packet alterations.

5. Security is used for Mandatory Access Control networking rules (e.g. SELinux)

**Q24. What is prot, opt, in, out, source & destination?**

`prot:` It denotes the Protocols. tcp, udp, icmp, etc., 

`opt:` Special options for that specific rule. 

`in:` Name of input interface via which the packet isreceived

`out:` Name of output interface via which the packetwill be send

`source:` Source ip-address or domain name of the packet 

`destination:` Destination ip-address or domain namefor the packet


**Q25. Why are rules added to the top?**

Rules are added to the top of the iptables because it will neglect the rules defined below a particular rule which is defined on the top.

**Q26. What type of rules we can add to the iptables?**

1. Delete Existing Rule
2. Set Default Chain Policies
3. Block a Specific ip-address.
4. Allow ALL Incoming SSH.
5. Allow Incoming SSH only from a Specific Network.
6. Allow Incoming HTTP and HTTPS.
7. Combine Multiple Rules Together using Multi Ports.
8. Allow Outgoing SSH.
9. Allow Outgoing SSH only to a Specific Network
10. Allow Outgoing HTTPS

**Q27. Can we block a website by its domain name only?**

Yes, With iptable, we can apply rules according to the domain name. There are a few ways we can apply iptable according to the domain name.

**Q28. How can we persist rules in iptables?**

We can persist rules in iptables by using following commands :

`sudo netfilter-persistent save`

		OR

`sudo iptables-save > /etc/iptables/rules.v4`

**Q29. How can we save rules in iptables?**

Save iptables firewall rules permanently on Linux using

`sudo iptables-save > ~/rules.v4`

**Q30. What is Difference between ufw & iptables?**

iptables provide a complete firewall solution that is both highly configurable and highly flexible.ufw aims to provide an easy to use interface for people unfamiliar with firewall concepts, while at the same time simplifies complicated iptables commands to help an administrator who knows what he or she is doing.

**Q31. What are public & private keys?**

In `public key,` two keys are used. One key is used for encryption and another key is used for decryption.

In `private key,` same key is used for encryption and decryption.

**Q32. How does ssh work?**

SSH, or Secure Shell, is a remote administration protocol that allows users to control and modify their remote servers over the Internet. It provides a mechanism for authenticating a remote user, transferring inputs from the client to the host, and relaying the output back to the client.

**Q33. Difference between HTTP & HTTPS?**

|**HTTP** |  | **Https** |
|-----|-----|-----|
| HTTP stands for Hypertext Transfer Protocol. | HTTPS stands for Hypertext Transfer Protocol Secure. |
| It is an application layer protocol for transmitting hypermedia documents. | It is an extension of HTTP. |
| It was designed for communication between web browser and web server. | It is used for server communication over a network. |
| Use port no 80 for communication. | Use port no 443 for communication. |

**Q34. What is SSL?**

`SSL` certificate is a digital certificate that authenticates a website's identity and enables an encrypted connection. SSL stands for Secure Sockets Layer, a security protocol that creates an encrypted link between a web server and a web browser.

**Q35. What is the difference between apt update & apt upgrade?**

`apt-get update-` updates the list of available packages and their versions, but it does not install or upgrade any packages. 
`apt-get upgrade-` it installs newer versions of the packages you have. After updating the lists, the package manager knows about available updates for the software you have installed.

**Q36. What do repositories contain in a Linux system?**

A Linux repository is a storage location from which your system retrieves and installs OS updates and applications.

**Q37. What are the package managers used in Linux?**

Package manager is a tool that allow users to install, remove, upgrade, configure and manage software package on an operating system.

In Linux, we have two types of package manager.

`Low level package manager-` They are only responsible for installing the application and not the dependencies. e.g. dpkg,rpm

`High level package manager-` They resolve the dependencies & meta data searching. e.g.apt

**Q38. What does the number represent after the file permissions?**

It denotes the number of files contained in that particular directory.

**Q39. What is the difference between apt and apt-get?**

`apt-get-` may be considered as lower-level and "back-end", and support other APT-based tools. 
`apt-` is designed for end-users (human) and its output may be changed between versions. The apt command is meant to be pleasant for end users and does not need to be backward compatible like apt-get(8).


**Q40. How can I give access to someone to my AWS instance?**

Create an IAM group and users

And follow the steps given by the amazon Identity and access management for Amazon EC

**Q41. What are daemon applications or processes?**

A daemon (also known as background processes) is a Linux or UNIX program that runs in the background. Almost all daemons have names that end with the letter "d".

**Q42. What does a ".d" represent after a filename?**

"d" stands for directory and such a directory is a collection of configuration files which are often fragments that are included in the main configuration file. The point is to compartmentalize configuration concerns to increase maintainability.

**Q43. What happens when a pem file gets deleted?**

We cannot the acces the aws instance if the pem is deleted.

**Q44. What information is stored in the /etc/hosts file?**

It stores ip address for hostnames and is used to translate hostnames to its corresponding ip address.

**Q45. What is SCP & what does this command do?**

SCP stands for secure copy. It is used to copy file between server in a secure way. It allows the local host and the remote host or between two remote host.

	`scp  /path/file_name ubuntu@ip destination`
**Q46. How port forwarding works?**

`Port forwarding-` is a technique that is used to allow external devices access to computers services on private networks. Local port forwarding is the most common type of port forwarding. It is used to let a user connect from the local computer to another server, i.e. forward data securely from another client application running on the same computer as a Secure Shell (SSH) client.

**Q47. How can we connect without IP to AWS instance?**

Go into the EC2 dashboard, then in the NETWORK & SECURITY menu go to Elastic IPs. Click on Allocate a new address. Right click on the new IP and select Associate address. Associate it with your EC2 instance that doesn't have an elastic IP.

**Q48. What is an SSH Agent?**

ssh-agent is a key manager for SSH. It holds your keys and certificates in memory, unencrypted, and ready for use by ssh. It saves you from typing a passphrase every time you connect to a server. It runs in the background on your system, separately from ssh, and it usually starts up the first time you run ssh after a reboot.

**Q49. Create a unit file for any application.**

[Unit]
Description=The NGINX HTTP and reverse proxy server
After=syslog.target network-online.target remote-fs.target nss-lookup.target
Wants=network-online.target

[Service]
Type=forking
PIDFile=/run/nginx.pid
ExecStartPre=/usr/sbin/nginx -t
ExecStart=/usr/sbin/nginx
ExecReload=/usr/sbin/nginx -s reload
ExecStop=/bin/kill -s QUIT $MAINPID
PrivateTmp=true

[Install]
WantedBy=multi-user.target


**Q50. What is RHEL?**

RHEL stands for Red Hat Enterprise Linux. It is commercial Linux distribution developed by Red hat. It is not free. We have to purchase the licensed.