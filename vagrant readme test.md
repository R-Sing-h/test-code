<p align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/Vagrant.png/150px-Vagrant.png"></p>

# Vagrant.readme
This file will be a brief overview of the operations of Vagrant. This readme will be specific for our uses within this project, thus will focus on containing information relevant to our use case. This guid will use Ubuntu 22.04.1 LTS as a base, so syntax will follow those used with that OS. 

**[Vagrant Website](https://www.vagrantup.com/)**

**[Source](https://github.com/hashicorp/vagrant)** -Github Page

**[HashiCorp Fourm](https://discuss.hashicorp.com/c/vagrant/24)** 

## Why Vagrant? 
Vagrant is a tool for building, testing, operating, and distributing development environments. We will be using this in conjunction with **[VirtualBox 6.1.38](https://www.virtualbox.org/wiki/Download_Old_Builds_6_1)**  to create, operate, and destroy virtual machines as needed. Although we are going to be using VirtualBox, we can use other forms of VMs such as VMware, AWS, OpenStack, or in containers such as with Docker or raw LXC to create VMS. 
## Installation 
[Getting Started](https://developer.hashicorp.com/vagrant/tutorials/getting-started) - This is a full quick start guide to the operation. It will contain 9 tutorials on how to operate Vagrant. 

**VirtualBox**
Download Page: https://www.virtualbox.org/wiki/Download_Old_Builds_6_1
Specifically we shall be using Virtual Box 6.1.38 . This is not the current version of VB. 

Installing VB via the terminal is pretty straight forwards. We will start by running the command:

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
Then just restart the application

**Vagrant**
