<img src="https://i.imgur.com/HG66CCx.png?raw=true" alt="CODAM" style="max-width: 50%;">

# Born2beroot

Born2BeRoot is an exercise in hands-on experience in system administration and security, specifically focusing on Linux environments.
In this project we install and configure a virtual machine to be a server. Configuration includes among other things:
Setting up a firewall, configuring user accounts and permissions, setting up monitoring and more.

### Virtual machine and operatig system
To be able to configure anything we need to have an up and running system.  
To this end we first download and install: [Virtual Box](https://www.virtualbox.org/)  

VirtualBox is a free and open-source virtualization software that allows you to run multiple operating systems on a single physical machine. It essentially acts as a "virtual computer" within our existing computer, so we can mess about without endangering our actual computer.

The next thing we need is an operation system. The [subject file](https://cdn.intra.42.fr/pdf/pdf/82536/en.subject.pdf) gives us the option to choose between either the latest stable version of Debian (no testing/unstable), or the latest stable version of Rocky. I chose Debian: [Debian](https://www.debian.org/distrib/)

---

### Setting up the server

Below we have a short summary of the tasks that were required by our assignment:

- **Create at least 2 encrypted partitions using LVM**  
  This task involves setting up encrypted partitions using Logical Volume Management (LVM). LVM allows for dynamic allocation of storage and encryption ensures that the data on these partitions is secure. Encrypted partitions provide an added layer of security as the data is unreadable without the appropriate decryption key.
- **Configure an SSH service to run on port 4242 only**
  Secure the SSH (Secure Shell) service, which is used for remote access to the system. By configuring SSH to run on a non-standard port (in this case, port 4242), it adds an extra layer of security. Additionally, disabling SSH login as root is important to prevent direct root access, which is a common security practice.
- **The hostname of our virtual machine must be ourlogin ending with 42**
  Setting the hostname is important for identifying and managing a system on a network. 
- **Configure a strong password policy**
  This one is kind of self-explanatory.
- **Install and configure sudo following strict rules**  
  `sudo` allows authorized users to execute commands with administrative privileges. Installing and configuring sudo with strict rules involves setting up who has `sudo` access, what commands they can run, and under what circumstances. This helps ensure that only authorized users can perform administrative tasks.
- **In addition to the root user, a user with your login as username has to be present**
  This task involves creating a user account with your login name. Having a dedicated user account is important for personalization and security. It's also best practice to avoid using the root account for everyday tasks.
- **Create a simple script called monitoring.sh**  
  At server startup the script will display some information on all terminals every 10 minutes.
  It will output information about the system currently running on our virtual machine. This could include details like CPU usage, memory usage, disk space, etc. It provides a way to monitor the system's performance automatically.
  The output will look something like:
  
  ![script](https://i.imgur.com/4LbzfYf.png)

  
