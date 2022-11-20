<p align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/Vagrant.png/150px-Vagrant.png"></p>

## Vagrant Readme  

This readme will be about using Vagrant for *Project_Artemis* it will not include the downloading and installing of the prerequeistes needed to get the VMs up and running. In our project we are currently have 4 servers. The main server we have designated "Mothership", this server will be in charge of issuing commands to our other three servers. The other three servers are as follows: ***Saltmaster***, ***TDP***, and ***CUI***. The configurations for these machines can be found in the **Vagrantfile** and their configuations can also be editied within that file. We have them set up currently using a Centos OS.
### Virtual Machine Operation

####  Commands

##### **Booting up the environment**
Once the initial boot sequence has been completed, the following command will be used to bring the servers up:
```
$ vagrant up "Server name" (without quotes)
```
and this command will call forth whichever server we want to spin up.

For our use case we will be using the "vagrant up" command to spin up *mothership*, *saltmaster*, *TDP*, or *CUI* servers. An example of this is:
```
$ vagrant up Mothership
```
In the end this will allow us to quickly spin up extra servers as needed and turn them off when not needed.

##### **Logging in and out of the environment**
After getting the servers up we can now log in to them. This will be done with a SSH command:
```
$ vagrant ssh "server name" (without quotes)
```
For example:
```
$ vagrant ssh mothership
```
![image](https://user-images.githubusercontent.com/114712045/202923209-fb5e7fc7-4b69-47ad-b577-e05f39d21515.png)

Next we will be prompted for a password:
![image](https://user-images.githubusercontent.com/114712045/202923285-c5f76c83-7233-4810-897e-d6b826183a32.png)

If we successfully log in we will be greeted with a screen that looks like:
![image](https://user-images.githubusercontent.com/114712045/202923425-d178b9b6-ed8d-42f6-8db3-ca4cdc26dcc3.png)


Once we are in the server we can now navigate as we normally would. All commands will follow their normal syntax. Logging out of the server can be done with a simple *"Exit"* command in the terminal. This will bring us back to our local terminal. 
##### **Halting the Environment**
We can shut down, or ***"halt"*** the environment with the use of the following command:
**THIS CANNOT BE DONE INSIDE OF THE MACHINE THAT NEEDS TO BE SHUT DOWN.**

This command will be:
```
$ vagrant halt "Server Name" (without quotes)
```
Potential use case:
```
$ vagrant halt mothership
```
 This will be useful when we need to have servers set up but not running.
 
##### **Destroying the Environment**
If we ever need to completely delete a server we can use command:
```
$ vagrant destroy "Server Name" (without quotes)
```
**REMINDER THIS NEEDS TO BE DONE OUTSIDE THE TARGETED SERVER**
```
$ vagrant destroy mothership
```
Using the ***"vagrant destroy"*** command **WILL DELETE** all the files that were stored on that server. 