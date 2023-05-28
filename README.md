 # Born2beRoot

## How does a virtual machine work and what is its purpose? 

A virtual machine (VM) is virtual environment that functions as a virtual computer system that is created on a physical machine (like a laptop, smart phone, or server). It has its own CPU, memory, network interfaces, and storage. 

A hypervisor, also known as a virtual machine monitor or VMM, is software that creates and runs virtual machines (VMs). A hypervisor allows one host computer to support multiple guest VMs by virtually sharing its resources, such as memory and processing. 

### The two types of hypervisors used for virtualization: 

- **Type 1 hypervisor:** acts like a lightweight operating system and runs directly on the host’s hardware. 

- **Type 2 hypervisor:** runs as a software layer on an operating system, like other computer programs. 

### Several reasons to use VMs: 

Because the software is separate from the physical host computer, users can run multiple OS instances on a single piece of hardware, saving a company time, management costs and physical space. 

Furthermore, VMs can support legacy apps, reducing or eliminating the need and cost of migrating an older app to an updated or different operating system. 

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

## The basic differences between CentOS, Rocky and Debian? 

### Origins:  

- **CentOS:** CentOS is a type of operating system that was created to be a free alternative to a commercial operating system called Red Hat Enterprise Linux (RHEL). 

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

## My choice of operating system and why? 

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

## The difference between aptitude, and apt

Apt offers a command-line interface, while aptitude offers a visual interface. When facing a package conflict, `apt` will not fix the issue while `aptitude` will suggest a resolution that can do the job. Aptitude can interactively retrieve and displays the Debian changelog of all available official packages

Apt requires the user to have a solid knowledge of Linux systems and package management as you are running everything in the command line. It can be difficult for a novice to handle.

On the other hand, aptitude with its interface is more user-friendly as it offers a layer of abstraction regarding the different sub-commands to use for installation, upgrades, etc.

## AppArmor

AppArmor is a Mandatory Access Control framework. When enabled, AppArmor confines programs according to a set of rules that specify what files a given program can access. This proactive approach helps protect the system against both known and unknown vulnerabilities.

## LVM (Logical Volume Manager): 

LVM, which stands for Logical Volume Management, is a technology that helps manage storage devices in a flexible way. It allows users to pool and abstract the physical layout of storage devices, providing advantages such as increased abstraction, flexibility, and control. 

### LVM has three main components: 

- **Physical Volumes (PV):**

    Physical volumes are the raw materials or building blocks that are used to achieve the abstraction that is logical volumes. In simpler words, physical volumes are the logical unit of an LVM system. 

    A physical volume can be anything, a raw disk, or a disk partition. Creating and initializing a physical volume are the same thing. Both mean you're just preparing the building blocks (i.e. partitions, disks) for further operations 

- **Volume Groups (VG):**

    Volume groups are collections of physical volumes. Volume groups are the storage pool that combines the storage capacity of multiple raw storage devices. 

- **Logical Volumes (LV):**

    Logical volumes are created within volume groups and function as partitions or filesystems. They provide much more flexibility compared to traditional partitions on a physical disk. Logical volumes are the main components that users and applications interact with. 

## SSH (Secure Shell or Secure Socket Shell): 

SSH is a secured network protocol to access remote computers in a network. SSH encrypts the communication between the client and the server, making it difficult for anyone to intercept or read the data being transmitted. It uses strong encryption and authentication methods to ensure privacy and security. 

### How does it work? 

SSH uses a client-server architecture for secured communication over the network by connecting a SSH client with the SSH server. SSH server by default listens on TCP port 22, however you can modify this for more security. 

It uses a public-key cryptography technique to authenticate between client and server. In addition, the protocol uses strong symmetric encryption & hashing algorithms for the exchange of messages between client and server to ensure privacy and data integrity. 

## UFW (Uncomplicated Firewall): 

UFW (Uncomplicated Firewall) is a user-friendly front-end tool for managing firewall rules on Linux systems. It provides a simplified interface for configuring and managing firewall settings, making it easier for users to control incoming and outgoing network traffic. 

With UFW, you can define rules to allow or deny specific connections based on protocols, ports, and IP addresses. It enables you to create firewall rules to protect your system from unauthorized access, block malicious traffic, and control network communication for different applications or services running on your machine. 

UFW simplifies the process of configuring firewall rules by using a straightforward command-line interface. It abstracts the complexities of configuring iptables (the underlying firewall infrastructure) and provides a more intuitive way to manage firewall settings. 

## SUDO (Superuser do)

sudo is a Linux command that allows programs to be executed as a super user (aka root user) or another user. 

