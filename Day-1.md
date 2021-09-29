						                    Day – 1
							       Overview of Linux
							              Q&A
								        
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

**UEFI was designed to overcome many limitations of the old BIOS, including:**

* UEFI supports drive sizes upto 9 zettabytes, whereas BIOS only supports 2.2 terabytes.
* UEFI has discrete driver support, while BIOS has drive support stored in its ROM, so updating BIOS firmware is a bit difficult.
* UEFI runs in 32bit or 64bit mode, whereas BIOS runs in 16bit mode. So UEFI  is able to provide a GUI (navigation with mouse) as opposed to BIOS which allows navigation only using the keyboard.


**Q5. How to decide when should we go for Ubuntu & when for other systems?**

Before choosing for the operating system one should keep the following points in mind :-

* Stability and Robustness
* Cost and Support
* Discontinued Products
* OS Releases 
* The packages provided by the distributors.

**Q6. What are the various linux distributors & their uses?**

`Ubuntu -` Ubuntu is a Linux distribution based on Debian. It is developed by Canonical and a community of developers. It has 3 official editions: Desktop, Server and Core, which can either run on a computer or on a VM. More than 33% of the websites using Linux use Ubuntu, according to W3Techs data. Its growth since 2010 has been amazing. It is also a popular distribution among cloud computing projects.

`CentOS - ` CentOS is a distribution based on the source code of the commercial distribution Red Hat Enterprise Linux (RHEL). It was launched in 2004 and is backed up by a growing community. It is a safe bet for those looking for a high-quality code. But CentOS 8 will be its last version. In 2019, Red Hat announced that CentOS Linux would be replaced by CentOS Stream — an upstream development platform for RHEL. 

`Red Hat Enterprise Linux (RHEL) -` Red Hat Enterprise Linux (RHEL) is a commercial Linux distribution developed by Red Hat. It has a server version and a desktop version. As it uses open source software, published under a General Public License, they make their code available to the public via CentOS. Red Hat has sponsored the CentOS project since 2014.

`Fedora -`  Fedora is a Linux distribution developed by the Fedora Project — sponsored mainly by Red Hat, with support from other companies. It is developed and maintained by the community and it is an upstream source of the commercial RHEL distribution. Fedora usually has more modern software versions, considered as “non stable”, that are later included in RHEL. There are different Fedora editions available: Workstation, Server, CoreOS, Silverblue and IoT. Fedora Linux was launched in 2003.


**Q7. What is getty?**

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


**Q8.What is Uname commands?**

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


 **Q9. What is systemd.unit(5)?**
 
 Man Pages are divided into 8 sections.

* User Commands : Commands that can be run from the shell by a normal user
* System Calls: Programming functions used to make calls to the Linux kernel
* C Library Functions: Programming functions that provide interfaces to specific programming libraries.
* Devices and Special Files: File system nodes that represent hardware devices or software devices.
* File Formats and Conventions: The structure and format of file types or specific configuration files.
* Games: Games available on the system
* Miscellaneous: Overviews of miscellaneous topics such as protocols, filesystems and so on.
* System administration tools and Daemons:Commands that require root or other administrative privileges to use. 

**Q10. Difference between Systemd and initd?**

The init process forces services to be launched in a particular sequence. It makes each process dependent on another process which can lead to delay.
Whereas systemd is used to run the system services in parallel. It is helpful in removing unnecessary delays and boosting up the initialization process.


