# Born2beRoot

## Table of Contents
1. [How does a virtual machine work and what is its purpose?](#virtual_machine)
2. [The basic differences between CentOS, Rocky and Debian?](#centos_rocky_debian)
3. [My choice of operating system and why?](#debian)
4. [The difference between aptitude, and apt](#aptitude_apt)
5. [AppArmor](#apparmor)
6. [LVM (Logical Volume Manager](#LVM)
7. [SSH (Secure Shell or Secure Socket Shell](SSH)
8. [UFW (Uncomplicated Firewall)](UFW)
9. [SUDO (Superuser do)](sudo)
10. [Password policy](password)
11. [What is the sudoers file, & its purpose?](sudoers_file)
12. [What is the monitoring.sh script?](monitoring.sh)
13. [Wall command (write all](wall)
14. [Cron](cron)

## How does a virtual machine work and what is its purpose? <a name="virtual_machine"></a>

A virtual machine (VM) is virtual environment that functions as a virtual computer system that is created on a physical machine (like a laptop, smart phone, or server). It has its own CPU, memory, network interfaces, and storage. 

A hypervisor, also known as a virtual machine monitor or VMM, is software that creates and runs virtual machines (VMs). A hypervisor allows one host computer to support multiple guest VMs by virtually sharing its resources, such as memory and processing. 

### The two types of hypervisors used for virtualization: 

- **Type 1 hypervisor:** acts like a lightweight operating system and runs directly on the host’s hardware. 

- **Type 2 hypervisor:** runs as a software layer on an operating system, like other computer programs. 

### Several reasons to use VMs: 

- **Server consolidation:**

    Virtualizing servers allows for better utilization of physical resources by running multiple virtual servers on a single physical server, reducing the need for additional hardware. 

- **Cost and resource savings:**

    VMs reduce the need for purchasing extra physical resources, saving on expenses for hardware, power, space, and cooling in data centers. 

- **Disaster recovery:**

    VMs provide failover and redundancy options, improving resilience and reducing the reliance on additional hardware for disaster recovery. 

- **Isolation and flexibility:**

    VMs provide isolated environments, allowing different applications or operating systems to run independently without interfering with each other or the host hardware. 

- **Testing and development:**

    VMs are ideal for testing new applications or setting up production environments in a controlled and isolated manner. 

- **Single-purpose tasks:**

    VMs can be dedicated to specific processes or tasks, providing a focused and optimized environment for those requirements. 

Because the software is separate from the physical host computer, users can run multiple OS instances on a single piece of hardware, saving a company time, management costs and physical space. 

Furthermore, VMs can support legacy apps, reducing or eliminating the need and cost of migrating an older app to an updated or different operating system. 

## The basic differences between CentOS, Rocky and Debian? <a name="centos_rocky_debian"></a>

### Origins:  

-   **CentOS:** CentOS is a type of operating system that was created to be a free alternative to a commercial operating system called Red Hat Enterprise Linux (RHEL). 

- **Rocky Linux:** Rocky Linux is another free operating system that was made to replace CentOS after it changed its direction. 

- **Debian:** Debian is an independent operating system that has been around for a long time. It focuses on being stable, secure, and based on free software principles. 

### Relationship with Commercial Distributions:  

- **CentOS and Rocky Linux:** Both CentOS and Rocky Linux have a connection to a commercial operating system called Red Hat Enterprise Linux. They were made to be similar to it but free to use. 

- **Debian:** Debian doesn't have a direct connection to a commercial operating system. It works on its own and is developed by a community of people. 

### Release Cycle and Updates:  

- **CentOS:** CentOS used to have a release model similar to the commercial operating system it was based on. However, it recently changed to provide more frequent updates. 

- **Rocky Linux:** Rocky Linux follows a similar release model as CentOS, aiming for stability and long-term support for each major version. 

- **Debian:** Debian follows a stable release model with a longer release cycle to ensure reliability and compatibility. 

### Package Management:  

- **CentOS and Rocky Linux:** They use a package manager called YUM or DNF to install and manage software on the operating system. 

- **Debian:** Debian uses a package manager called APT, which makes it easy to install and update software. 

### Software Ecosystem:  

- **CentOS and Rocky Linux:** These operating systems are commonly used for servers and have many software options suitable for enterprise environments. 

- **Debian:** Debian has a wide range of software available, both for servers and personal computers. It is known for its commitment to free and open-source software. 

## My choice of operating system and why? <a name="debian"></a>

### Debian 

- **Easy Installation:** Debian has a simple and beginner-friendly installation process. 

- **Stability and Reliability:** Debian is known for being stable and dependable. 

- **Lots of Software:** Debian has a large collection of software available for easy installation. 

- **Supportive Community:** There is a helpful community of users and developers ready to assist beginners. 

- **Helpful Documentation:** Debian provides extensive documentation and tutorials for beginners. 

- **Focus on Security:** Debian prioritizes security and provides regular updates to keep your system safe. 

- **Customization Options:** Debian allows you to personalize your system's look and feel. 

In summary, Debian is easy to install, stable, has a wide range of software, has a helpful community, provides useful documentation, focuses on security, and offers customization options. These factors make it an excellent choice for beginners. 

## APT (Advanced Packaging Tool)

Apt is the default Linux command-line tool to manage the packages on a Debian-based system. It comes by default and doesn't offer a graphical interface to manage the tools that are installed and the ones that you can need in the future. 

To install a package, you need to specify the name of the package just after the `apt install` command. The package manager reads the `/etc/apt/sources.list` file and the contents of the `/etc/apt/sources.list.d` folder to retrieve the ones that you need with all the dependencies.

Apt command offers a lot of sub-commands that help you to manage your system so that the packages can be added, updated, removed, or fixed if a problem occurs. During those processes, it will automatically install, update or remove the necessary dependencies or the other packages which depend on the main package that is being operated

## Aptitude

Aptitude is also an advanced packaging tool that you can use over apt. It offers a command-line and text-based front-end for package management. It doesn't come by default, so you need to install it with the `apt` command.

If you do not have Aptitude installed, you can install it by using the command below:

```
sudo apt install aptitude
```

Aptitude offers the possibility to manage your packages through command lines and also from a visual interface directly on your terminal. You can perform the main actions like installing, updating, and deleting your packages. it also offers sub-commands to manage your packages as apt but some people prefer the visual interface as it's easy to use.

## The difference between aptitude, and apt <a name="aptitude_apt"></a>

Apt offers a command-line interface, while aptitude offers a visual interface. When facing a package conflict, `apt` will not fix the issue while `aptitude` will suggest a resolution that can do the job. Aptitude can interactively retrieve and displays the Debian changelog of all available official packages

Apt requires the user to have a solid knowledge of Linux systems and package management as you are running everything in the command line. It can be difficult for a novice to handle.

On the other hand, aptitude with its interface is more user-friendly as it offers a layer of abstraction regarding the different sub-commands to use for installation, upgrades, etc.

## AppArmor <a name="apparmor"></a>

AppArmor is a Mandatory Access Control framework. When enabled, AppArmor confines programs according to a set of rules that specify what files a given program can access. This proactive approach helps protect the system against both known and unknown vulnerabilities.

## LVM (Logical Volume Manager) <a name="LVM"></a>

LVM, which stands for Logical Volume Management, is a technology that helps manage storage devices in a flexible way. It allows users to pool and abstract the physical layout of storage devices, providing advantages such as increased abstraction, flexibility, and control. 

### LVM has three main components: 

- **Physical Volumes (PV):**

    Physical volumes are the raw materials or building blocks that are used to achieve the abstraction that is logical volumes. In simpler words, physical volumes are the logical unit of an LVM system. 

    A physical volume can be anything, a raw disk, or a disk partition. Creating and initializing a physical volume are the same thing. Both mean you're just preparing the building blocks (i.e. partitions, disks) for further operations 

- **Volume Groups (VG):**

    Volume groups are collections of physical volumes. Volume groups are the storage pool that combines the storage capacity of multiple raw storage devices. 

- **Logical Volumes (LV):**

    Logical volumes are created within volume groups and function as partitions or filesystems. They provide much more flexibility compared to traditional partitions on a physical disk. Logical volumes are the main components that users and applications interact with. 

## SSH (Secure Shell or Secure Socket Shell) <a name="SSH"></a>

SSH is a secured network protocol to access remote computers in a network. SSH encrypts the communication between the client and the server, making it difficult for anyone to intercept or read the data being transmitted. It uses strong encryption and authentication methods to ensure privacy and security. 

### How does it work? 

SSH uses a client-server architecture for secured communication over the network by connecting a SSH client with the SSH server. SSH server by default listens on TCP port 22, however you can modify this for more security. 

It uses a public-key cryptography technique to authenticate between client and server. In addition, the protocol uses strong symmetric encryption & hashing algorithms for the exchange of messages between client and server to ensure privacy and data integrity. 

## UFW (Uncomplicated Firewall) <a name="UFW"></a>

UFW (Uncomplicated Firewall) is a user-friendly front-end tool for managing firewall rules on Linux systems. It provides a simplified interface for configuring and managing firewall settings, making it easier for users to control incoming and outgoing network traffic. 

With UFW, you can define rules to allow or deny specific connections based on protocols, ports, and IP addresses. It enables you to create firewall rules to protect your system from unauthorized access, block malicious traffic, and control network communication for different applications or services running on your machine. 

UFW simplifies the process of configuring firewall rules by using a straightforward command-line interface. It abstracts the complexities of configuring iptables (the underlying firewall infrastructure) and provides a more intuitive way to manage firewall settings. 

## SUDO (Superuser do) <a name="sudo"></a>

Sudo is a Linux command that allows programs to be executed as a super user (aka root user) or another user. 

## Password policy <a name="password"></a>
A password policy defines the password strength rules that are used to determine whether a new password is valid.

### How do you implement the password policy?
The password policy was implemented by installing Password Quality Checking Library and adding additional password quality requirements such as minimum length, inclusion of uppercase letters and digits, restrictions on repeating characters, and prevention of using the username in the password to `pam_pwquality` module in the `/etc/pam.d/common-password` file where it checks for password quality.
```
password	requisite	pam_pwquality.so	retry=3 minlen=10 ucredit=-1 dcredit=-1 maxrepeat=3 reject_username difok=7 enforce_for_root
```

> `password`: This indicates that the configuration applies to password authentication.
> 
> `requisite:` Specifies that the module is required for password authentication to be successful.
> 
> `pam_pwquality.so`: Refers to the pam_pwquality module responsible for checking password quality.

The additional parameters are:
> `retry=3`: Specifies that the user will have three attempts to enter a valid password before failing.
> 
> `minlen=10`: Sets the minimum password length to 10 characters.
> 
> `ucredit=-1`: Requires at least one uppercase letter in the password.
> 
> `dcredit=-1`: Requires at least one digit (number) in the password.
> 
> `maxrepeat=3`: Limits the number of consecutive repeated characters in the password to three.
> 
> `reject_username`: Prevents the use of the username as part of the password.
> 
> `difok=7`: Specifies that at least seven characters in the new password should be different from the old password.
> 
> `enforce_for_root`: Applies the password quality checks even for the root user.

The password quality settings is also adjusted in the `/etc/login.defs` file by redefining the expiration period, the minimum waiting period before changing passwords, and the warning period for users. These settings contribute to enforcing a stronger security posture by ensuring that passwords are regularly updated and users are notified in advance of password expiration.
```
PASS_MAX_DAYS 30
PASS_MIN_DAYS 2
PASS_WARN_AGE 7
```

> `PASS_MAX_DAYS 30`: Maximum of 30 days before the password expires. After 30 days, users will be required to change their passwords.

> `PASS_MIN_DAYS 2`: Minimum number of 2 days a user must wait before changing their password again. This setting helps prevent users from frequently changing their passwords to bypass password history restrictions.

> `PASS_WARN_AGE 7`: Users will receive a warning message 7 days before their password expires, reminding them to change it.

### Advantages:
The main benefit of password complexity rules is that they enforce the use of unique passwords that are harder to crack. 

### Disadvantages:
With in increase of complexity requirements it becomes harder to remember the password potentially causing people to store their passwords using an insecure method such as writing it down or storing it on their phone or computer. Many organizations have found that as complexity requirements increase, users will have worse password hygiene. 

## What is the sudoers file, & its purpose? <a name="sudoers_file"></a>
The sudoers file is a configuration file in Unix-like operating systems that determines which users or groups are allowed to run specific commands with administrative privileges using the sudo command. It controls access to the system and provides a way to delegate limited root access to non-root users.

The purpose of the sudoers file is to define a policy that specifies who can perform privileged operations and what commands they are allowed to execute. It helps enhance security by allowing system administrators to grant certain privileges to trusted users while limiting access to critical system functions.

Open Sudoers file
```
sudo visudo
```

> `Defaults env_reset`: Resets the environment to a default state when executing commands with sudo.
> 
> `Defaults mail_badpass`: Sends an email notification to the user when they enter an incorrect password.
> 
> `Defaults secure_path="/usr/local/sbin:/usr/local/bin:/usr/bin:/sbin:/bin"`: Sets the secure path, which is the list of directories that sudo considers safe for executing commands.
> 
> `Defaults badpass_message="Password is wrong, please try again!"`: Specifies a custom error message to be displayed when a user enters an incorrect password.
> 
> `Defaults passwd_tries=3`: Sets the number of password attempts a user is allowed before the authentication fails.
> 
> `Defaults logfile="/var/log/sudo/sudo.log"`: Specifies the path to the sudo log file where sudo commands and related information are logged.
> 
> `Defaults log_input, log_output`: Enables logging of user input and output when executing sudo commands.
> 
> `Defaults requiretty`: Requires a TTY (terminal) to be present when executing sudo commands, which helps prevent remote execution of sudo commands.

> `root ALL=(ALL :ALL) ALL`: Grants the root user all privileges (on all hosts and terminals).

> `trngo ALL=(ALL) ALL`: Grants user "trngo" all privileges (on all hosts and terminals).
> 
> `%sudo ALL=(ALL :ALL) ALL`: Grants all members of the "sudo" group all privileges (on all hosts and terminals).
> 
> `trngo ALL=(ALL) NOPASSWD: /user/local/bin/monitoring.sh`: Allows user "trngo" to execute the command `/user/local/bin/monitoring.sh` without entering a password.

## What is the monitoring.sh script? <a name="monitoring.sh"></a>
Go to where the monitoring script file is in
```
cd /usr/local/bin
vim monitoring.sh
```

The monitoring.sh script is a bash script that collects various system information and broadcasts it to all logged-in users using the wall command. Here's a simplified explanation of what the script does:
- It uses various command-line utilities to gather system information such as architecture, CPU details (both physical and virtual), memory usage, disk usage, CPU load, last boot time, LVM usage, TCP connections, user login count, network information (IP address and MAC address), and the number of sudo commands executed.
- After collecting the system information, it formats it into a message using the wall command. The message includes the gathered information labeled with respective headings.
- The wall command broadcasts the message to all logged-in users, displaying the system information on their terminals.

In summary, the monitoring.sh script automates the process of collecting system information and notifying users about the current system status.

## Wall command (write all) <a name="wall"></a>
The wall command is a Unix command-line utility that stands for "write all." It allows you to send a message to all logged-in users on a Unix-like system. The message you provide as an argument to the wall command will be displayed on the terminals of all currently logged-in users.

The wall command is often used by system administrators to broadcast important messages, announcements, or notifications to all users on a system. It is particularly useful for conveying urgent information or system-wide notifications that require immediate attention from users.

In this section, the wall command in monitoring.sh script is used to send the formatted system information message as a broadcast to all logged-in users. The message includes various system details such as architecture, CPU information, memory usage, disk usage, CPU load, last boot time, LVM usage, TCP connections, user login count, network information, and the number of sudo commands executed.

When the script is executed, this line with the wall command will display the system information on the terminals of all currently logged-in users.
```
wall "	#Architecture: $arc
          #CPU physical: $pcpu
          #vCPU: $vcpu
          #Memory Usage: $uram/${fram}MB ($pram%)
          #Disk Usage: $udisk/${fdisk}Gb ($pdisk%)
          #CPU load: $cpul
          #Last boot: $lb
          #LVM use: $lvmu
          #Connections TCP: $ctcp ESTABLISHED
          #User log: $ulog
          #Network: IP $ip ($mac)
          #Sudo: $cmds cmd"
```
> The variables starting with `$` (e.g., `$arc`, `$pcpu`) will be replaced with the corresponding values obtained from executing various commands within the script when the message is broadcasted.

> `#Architecture`: Represents the system's architecture.
> 
> `#CPU physical`: Indicates the number of physical CPUs in the system.
> 
> `#vCPU`: Represents the number of virtual CPUs.
> 
> `#Memory Usage`: Shows the used and total memory in megabytes (MB) and the percentage of memory usage.
> 
> `#Disk Usage`: Displays the used and total disk space in gigabytes (GB) and the percentage of disk usage.
> 
> `#CPU load`: Indicates the CPU load percentage.
> 
> `#Last boot`: Represents the date and time of the last system boot.
> 
> `#LVM use`: Indicates whether LVM (Logical Volume Manager) is being used on the system.
> 
> `#Connections TCP`: Displays the number of established TCP connections.
> 
> `#User log`: Indicates the number of users currently logged in.
> 
> `#Network: IP`: Shows the system's IP address and MAC address.
> 
> `#Sudo: $cmds cmd`: Represents the number of sudo commands executed.

## Cron <a name="cron"></a>
Cron is a time-based job scheduler in Unix-like operating systems. It is a built-in utility that allows users to schedule and automate the execution of tasks or commands at specific intervals, dates, or times. The tasks scheduled with Cron are often referred to as "Cron jobs."

The purpose of Cron is to enable users to automate repetitive or scheduled tasks, system maintenance, data backups, and various other activities. It provides a convenient way to execute commands or scripts without manual intervention. Cron is commonly used for:

- Regular Maintenance: Cron allows you to schedule tasks like system updates, log rotation, and cleanup operations to keep the system running smoothly.
- Data Backups: Cron can be used to schedule regular backups of files or databases to ensure data integrity and disaster recovery.
- System Monitoring: You can use Cron to run monitoring scripts or commands that check system health, log errors, or collect performance metrics at specified intervals.
- Batch Processing: Cron enables the execution of batch jobs or processes that need to run at specific times or on specific dates, such as generating reports or performing data processing tasks.
- Automation: By leveraging Cron, repetitive tasks can be automated, reducing the need for manual execution and saving time and effort.

Cron relies on a configuration file called the "crontab" (short for "Cron table"), where users define the schedule and commands for their Cron jobs. Each user typically has their own crontab file, which they can modify using the crontab command.
Cron provides a flexible and reliable way to schedule and manage recurring tasks, making it a valuable tool for system administrators, developers, and users who require automated task execution.

Open the crontab and add a rule
```
sudo crontab -u root -e
```
Change from very 10 min to 1, the monitoring.sh script will be broadcasted.
```
*/1 * * * * /usr/local/bin/monitoring.sh
```

Stop script or start running without modifying the script itself. To check this, sudo reboot to restart the VM.
```
sudo /etc/init.d/cron stop
sudo /etc/init.d/cron start
```

## Reference
[Thuggonaut](https://github.com/Thuggonaut/42IC_Ring01_Born2beRoot/blob/main/README.md)


