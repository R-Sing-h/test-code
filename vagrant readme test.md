<p align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/Vagrant.png/150px-Vagrant.png"></p>

# Vagrant.readme
This file will be a brief overview of the operations of Vagrant. This readme will be specific for our uses within this project, thus will focus on containing information relevant to our use case. This guide will use ***Ubuntu 22.04.1 LTS*** as a base, so syntax will follow those used with that OS. 

**[Vagrant Website](https://www.vagrantup.com/)**

**[Source](https://github.com/hashicorp/vagrant)** -Github Page

**[HashiCorp Fourm](https://discuss.hashicorp.com/c/vagrant/24)** 

### Why Vagrant? 
Vagrant is a tool for building, testing, operating, and distributing development environments. We will be using this in conjunction with **[VirtualBox 6.1.38](https://www.virtualbox.org/wiki/Download_Old_Builds_6_1)**  to create, operate, and destroy virtual machines as needed. Although we are going to be using VirtualBox, we can use other forms of VMs such as ***VMware, AWS, OpenStack,*** or in containers such as with ***Docker*** or ***raw LXC*** to create VMS. 
### Installation 

##### VirtualBox
Download Page: https://www.virtualbox.org/wiki/Download_Old_Builds_6_1
Specifically we shall be using **VirtualBox 6.1.38** . This is not the current version of VB. 

Installing VB via the terminal is pretty straight forwards. We will start by running the command:

Installation Information Gathered From [linuxconfig.org](https://linuxconfig.org/install-virtualbox-on-ubuntu-20-04-focal-fossa-linux)
##### VIA Terminal 
**Intial Installation**
```
$ sudo apt install virtualbox copy 
```
**Running VirtualBox**
```
$ virtualbox
```

**Extention Pack**
Additionally there is an extention pack to download, but this is not required for our use case.
```
$ sudo apt install virtualbox-ext-pack
```
Then just restart the application.

##### VIA GNOME Desktop 
In **Software Store** search for the **"Software"** application.
<p><img src="https://linuxconfig.org/wp-content/uploads/2020/03/01-install-virtualbox-on-ubuntu-20-04-focal-fossa-linux.png"></p> 

Search for ***VirtualBox*** making sure the version is not newer than **6.1.xx**, as of 11/13/22 ***Vargant*** is not compatiable will newer versions.
<p><img src="https://linuxconfig.org/wp-content/uploads/2020/03/02-install-virtualbox-on-ubuntu-20-04-focal-fossa-linux.png"></p>  

User who is installing must belong to the **SUDO group** to proceed with the software installation the software.
<p><img src="https://linuxconfig.org/wp-content/uploads/2020/03/04-install-virtualbox-on-ubuntu-20-04-focal-fossa-linux.png"></p> 

Once installation of ***VirtualBox*** has been completed, we are ready to launch! Have Fun!
<p><img src="https://linuxconfig.org/wp-content/uploads/2020/03/05-install-virtualbox-on-ubuntu-20-04-focal-fossa-linux.png"></p> 

##### Vagrant
Installation information gathered from, [https://developer.hashicorp.com/vagrant](https://developer.hashicorp.com/vagrant/tutorials/getting-started/getting-started-install)

Getting started with the Vagrant install we need to first download the actual software. There is no way to do this from the GNOME GUI so we will exvlusively focus on installing through our terminal. 

First we will need to run this command listed below, it will help to prep with the actual [install](https://developer.hashicorp.com/vagrant/downloads). Embedded in that hyperlink is the download page for most supported operating systems. This guide will follow **Ubuntu/Debian** 
```
$ wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
```
Following up with the previous command next we will need to run, 
```
$ echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
```
Lastly we can run the command below to finally install and update the ***Vagrant*** software.
```
$ sudo apt update && sudo apt install vagrant
```
After the installation is complete we can run the command,
```
$ vagrant 
```
This should return something along the lines of. If so we have completed the installation of ***Vagrant*** on this machine.
```
$ vagrant
Usage: vagrant [options] <command> [<args>]
    
    -v, --version                    Print the version and exit.
    -h, --help                       Print this help.

# ...
```
Additionally we can run,
```
vagrant --version 
```
which should return (your version might be different):
```
$ vagrant --version

Vagrant 2.2.19

#...
```
If all this has been successful we have installed ***Vagrant*** on our machine. Congratulations!