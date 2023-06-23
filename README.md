# Ansible

![Ansible](/images/Ansible.png)

## Introduction to Ansible

* Michael DeHaan developed Ansible, in the year 2013.

* RedHat acquired the Ansible tool in 2015.

* Ansible is included as part of the Fedora distribution of Linux.

* Ansible is also available for RedHat Enterprise Linux, Debian, CentOS, Oracle Linux, and Scientific Linux via Extra Packages for Enterprise Linux (EPEL) and Ubuntu as well as for other operating systems.

###  What is Ansible

* Ansible is an open-source IT engine that automates application deployment, cloud provisioning, intra service orchestration, and other IT tools.

* Ansible is an automation tool that is mainly used for configuration management. We can Configure so many things using Ansible like web-server, Infrastructure, etc.

* Ansible works on a declarative approach which means we don't have to tell how to install just tell what to install.

* Ansible is easy to deploy because it does not use any agents or custom security infrastructure on the client-side, and by pushing modules to the clients. 

* These modules are executed locally on the client-side, and the output is pushed back to the Ansible server.

* It can easily connect to clients using SSH-Keys, simplifying though the whole process. 

* Client details, such as hostnames or IP addresses and SSH ports, are stored in the files, which are called inventory files. 

* If you created an inventory file and populated it, then Ansible can use it.

* Ansible uses the playbook to describe automation jobs, and playbook, which uses simple language, i.e., YAML. 

* YAML is a human-readable data serialization language & commonly used for configuration files, but it can be used in many applications where data is being stored.

* Ansible is designed for multi-tier deployment. Ansible does not manage one system at a time, and it models IT infrastructure by describing all of your systems are interrelated. 

* Ansible is entirely agentless, which means Ansible works by connecting your nodes through SSH (by default). Ansible gives the option to you if you want another method for the connection like Kerberos.

* Ansible pushes small programs after connecting to your nodes which are known as "Ansible Modules". Ansible runs that module on your nodes and removes them when finished. 

* Ansible manages the inventory in simple text files (These are the host's files). Ansible uses the host file where one can group the hosts and can control the actions on a specific group in the playbooks.

### Example Illustration

**Example:** 

In a company, there are 100s of operating systems maybe some of the windows, some of the macs, some of Linux, Ubuntu, etc i.e heterogeneous environment and we have to configure some software in all operating system then we need to remember commands of all operating systems and require a lot of time to configure one by one...Then here come roles of ansible...In ansible Simply we write one playbook in YAML language and run from the controller node then it configures the software in all managed nodes.

### Why Ansible?

* Ansible is an Agentless tool that means we don't need to install it on the managed node just installed it on the controller node and start working with ansible. 

* Ansible is a very intelligent tool and its intelligence comes from modules. As an IT Admin, we don't have to remember all os commands just tell which package you wanna install and ansible will do that thing for you.

Here are some important reasons for using Ansible, such as:

* Ansible is free to use by everyone.

* Ansible is very consistent and lightweight, and no constraints regarding the operating system or underlying hardware are present.

* It is very secure due to its agentless capabilities and open SSH security features.

* Ansible does not need any special system administrator skills to install and use it.

* Ansible has a smooth learning curve determined by the comprehensive documentation and easy to learn structure and configuration.

* Its modularity regarding plugins, inventories, modules, and playbooks make Ansible a perfect companion orchestrates large environments.

## WorkFlow of Ansible

* Ansible works by connecting to your nodes and pushing out a small program called Ansible modules to them. 

* Then Ansible executed these modules and removed them after finished. 

* The library of modules can reside on any machine, and there are no daemons, servers, or databases required.


![workflow](/images/workflow.webp)

* In the above image, the Management Node is the controlling node that controls the entire execution of the playbook. 

* The inventory file provides the list of hosts where the Ansible modules need to be run. 

* The Management Node makes an SSH connection and executes the small modules on the host's machine and install the software.

Ansible removes the modules once those are installed so expertly. It connects to the host machine executes the instructions, and if it is successfully installed, then remove that code in which one was copied on the host machine.

#### Terms used in Ansible

Here are some important terms which are used in Ansible, such as:

| Terms  |  Explanation                 |
|--------|------------------------------|
|Ansible Server|It is a machine where Ansible is installed and from which all tasks and playbooks will be executed.|
|Modules |The module is a command or set of similar commands which is executed on the client-side.|
|Task	 |A task is a section which consists of a single procedure to be completed.|
|Role	 |It is a way of organizing tasks and related files to be later called in a playbook.|
|Fact	 |The information fetched from the client system from the global variables with the gather facts operation.|
|Inventory|	A file containing the data regarding the Ansible client-server.|
|Play	  |It is the execution of the playbook.|
|Handler  |The task is called only if a notifier is present.|
|Notifier |	The section attributed to a task which calls a handler if the output is changed.|
|Tag	  |It is a name set to a task that can be used later on to issue just that specific task or group of jobs.|

## Ansible Architecture

The Ansible orchestration engine interacts with a user who is writing the Ansible playbook to execute the Ansible orchestration and interact along with the services of private or public cloud and configuration management database. You can show in the below diagram, such as:

![Architecture](/images/ansible-architecture.png)

**Inventory**

Inventory is lists of nodes or hosts having their IP addresses, databases, servers, etc. which are need to be managed.

**API's**

The Ansible API's works as the transport for the public or private cloud services.

**Modules**

Ansible connected the nodes and spread out the Ansible modules programs. Ansible executes the modules and removed after finished. These modules can reside on any machine; no database or servers are required here. You can work with the chose text editor or a terminal or version control system to keep track of the changes in the content.

**Plugins**

Plugins is a piece of code that expends the core functionality of Ansible. There are many useful plugins, and you also can write your own.

**Playbooks**

Playbooks consist of your written code, and they are written in YAML format, which describes the tasks and executes through the Ansible. Also, you can launch the tasks synchronously and asynchronously with playbooks.

**Hosts**

In the Ansible architecture, hosts are the node systems, which are automated by Ansible, and any machine such as RedHat, Linux, Windows, etc.

**Networking**

Ansible is used to automate different networks, and it uses the simple, secure, and powerful agentless automation framework for IT operations and development. It uses a type of data model which separated from the Ansible automation engine that spans the different hardware quite easily.

**Cloud**

A cloud is a network of remote servers on which you can store, manage, and process the data. These servers are hosted on the internet and storing the data remotely rather than the local server. It just launches the resources and instances on the cloud, connect them to the servers, and you have good knowledge of operating your tasks remotely.

**CMDB**

CMDB is a type of repository which acts as a data warehouse for the IT installations.

## Installation

Install Ansible on Windows 11 through Windows SubSytem for Linux

Open the windows PowerShell and run as administrator:

Step 1: Install WSL

**wsl --install**

![step1](/images/step1.png)

Restart the System

Step 2: Enter the username and password once the installation is complete.

Type sudo su and enter the password

![step2](/images/step2.png)

![step3](/images/step3.png)

Step 3 : Perform an update to the packages

**apt-get update**

![step4](/images/step4.png)

Step 4 :Then install the software properties common package.

**apt install software-properties-common** 

![step5](/images/step5.png)

Step 5 : And install the Ansible personal package archive.

**$ sudo apt-add-repository ppa:ansible/ansible**

![step6](/images/step6.png)

Step 6 :  Install the Ansible.

**apt-get update**

**apt-get install ansible**

![step7](/images/step7.png)










