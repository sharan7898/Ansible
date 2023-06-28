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

### Terms used in Ansible

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

**Step 1**: Install WSL

**wsl --install**

![step1](/images/step1.png)

Restart the System

**Step 2**: Enter the username and password once the installation is complete.

Type sudo su and enter the password

![step2](/images/step2.png)

![step3](/images/step3.png)

**Step 3** : Perform an update to the packages

**apt-get update**

![step4](/images/step4.png)

**Step 4** :Then install the software properties common package.

**apt install software-properties-common** 

![step5](/images/step5.png)

**Step 5** : And install the Ansible personal package archive.

**$ sudo apt-add-repository ppa:ansible/ansible**

![step6](/images/step6.png)

**Step 6** :  Install the Ansible.

**apt-get update**

**apt-get install ansible**

![step7](/images/step7.png)

U can refer the video for installing the Ansible on Windows 11 : https://www.youtube.com/watch?v=OhCbpGBOACs&t=309s


## Ansible ad-hoc Commands

* Ad-hoc commands are one of the simplest ways of using Ansible. 

* These are used when you want to issue some commands on a server or bunch of servers. 

* The ad-hoc commands are not stored for future use, but it represents a fast way to interact with the desired servers.

* The Ansible ad-hoc command uses the **/usr/bin/ansible** command-line tool to automate a single task on one or more managed nodes. 

* The Ad-hoc commands are quick and easy, but they are not re-usable. The Ad-hoc commands demonstrate the simplicity and power of Ansible.

**Syntax**

```
ansible <hosts> [-m <module_name>] -a <"arguments"> -u <username> [--become]  

```

**Explanation**

**Hosts**: It can be an entry in the inventory file. For specifying all hosts in the inventory, use all or "*".

**module_name**: It is an optional parameter. There are hundreds of modules available in the Ansible, such as shell, yum, apt, file, and copy. By default, it is the command.

**Arguments**: We should pass values that are required by the module. It can change according to the module used.

**Username**: It specifies the user account in which Ansible can execute commands.

**Become**: It's an optional parameter specified when we want to run operations that need sudo privilege. By default, it becomes false.

### Parallelism and shell commands

You can reboot your company server in 12 parallel forks at the same time. For this, you need to set up the SSH agent for connection.

```
$ ssh-agent bash  
$ ssh-add ~/.ssh/id_rsa 

```

To run reboot for all your company servers in the group, 'abc', in 12 parallel forks:

```
$ ansible abc -a "/sbin/reboot" -f 12

```

By default, Ansible will run the above ad-hoc commands from the current user account. If you want to change then pass the username in ad-hoc command as follows:

```

$ ansible abc -a "/sbin/reboot" -f 12 -u username

```

### File Transfer

You can use ad-hoc commands for doing SCP (secure copy protocol) which means lots of files in parallel on multiple machines or servers.

**Transferring file on many machines or servers**

```

$ ansible abc -m copy -a "src = /etc/yum.conf dest = /tmp/yum.conf"

```
**Creating new directory**

```

$ ansible abc -m file -a "dest = /path/user1/new mode = 888 owner = user1 group = user1 state = directory"   

```

Deleting all directory and files

```

$ ansible abc -m file -a "dest = /path/user1/new state = absent" 

```

### Managing Packages

Ad-hoc commands are available for apt and yum module. Here are the following ad-hoc commands using yum.

Below command checks, if the yum package is installed or not, but not update it.

```

$ ansible abc -m yum -a "name = demo-tomcat-1 state = present" 

```

Below command checks the package is not installed.

```

$ ansible abc -m yum -a "name = demo-tomcat-1 state = absent"

```

And below command checks the latest version of package is installed.

```

$ ansible abc -m yum -a "name = demo-tomcat-1 state = latest"

```

### Managing Users , Groups and Services

You can manage, create, and remove a user account on your managed nodes with ad-hoc commands.

```

$ ansible all -m user -a "name=foo password=<crypted password here>"  
  
$ ansible all -m user -a "name=foo state=absent"  

```


**Managing Services**

Ensure a service is started on all the webservers.

```

$ ansible webservers -m service -a "name=httpd state=started"  

```

Alternatively, restart a service on all webservers:

```

$ ansible webservers -m service -a "name=httpd state=restarted" 

```

Ensure a service is stopped:

```

$ ansible webservers -m service -a "name=httpd state=stopped"

```

**Gathering Facts**

Fact represents the discovered variables about a system. You can use the facts to implement conditional execution of tasks, and also used to get ad-hoc information about your systems. To see all the facts:

```

$ ansible all -m setup  

```

## Ansible PlayBook

* Playbooks are the files where the Ansible code is written. Playbooks are written in YAML format. YAML means "Yet Another Markup Language," so there is not much syntax needed. 

* Playbooks are one of the core features of Ansible and tell Ansible what to execute, and it is used in complex scenarios. They offer increased flexibility.

* Playbooks contain the steps which the user wants to execute on a particular machine. And playbooks are run sequentially. Playbooks are the building blocks for all the use cases of Ansible.

* Ansible playbooks tend to be more configuration language than a programming language.

* Through a playbook, you can designate specific roles to some of the hosts and other roles to other hosts. By doing this, you can orchestrate multiple servers in very different scenarios, all in one playbook.

### Playbook Structure

Each playbook is a collection of one or more plays. Playbooks are structured by using Plays. There can be more than one play inside a playbook.

![playbook](/images/ansible-playbooks.png)

The function of the play is to map a set of instructions which is defined against a particular host.

There are different YAML editors, but prefer to use a simple editor such as notepad++. First, open the notepad++ and copy-paste the below YAML and change the language to YAML (Language → YAML).

A YAML starts with --- (3 hyphens) always.

### Create a Playbook

Let's start by writing an example YAML file. First, we must define a task. These are the interface to ansible modules for roles and playbooks.

One playbook with one play, containing multiple tasks looks like the below example.

```
---  
   name: install and configure DB  
   hosts: testServer  
   become: yes  
  
   vars:   
      oracle_db_port_value : 1521  
     
   tasks:  
   -name: Install the Oracle DB  
      yum: <code to install the DB>  
      
   -name: Ensure the installed service is enabled and running  
   service:  
      name: <your service name>

```

Above is a basic syntax of a playbook. Save it in a file as test.yml. A YAML syntax needs to follow the correct indentation.

### YAML Tags

Here are some YAML tags are given below, such as:

|  Tags     | Explanation  |
|-----------|--------------|
| Name	    |It specifies the name of the Ansible Playbooks.|
| Hosts	    |It specifies the lists of the hosts against which you want to run the task. And the host's Tag is mandatory. It tells Ansible that on which hosts to run the listed tasks. These tasks can be run on the same machine or the remote machine. One can run the tasks on the multiple machines, and the host's tag can have a group of host's entry as well.|
| Vars	    |Vars tag defines the variables which you can use in your playbook. Its usage is similar to the variables in any programming language.|
| Tasks	    |Tasks are the lists of the actions which need to perform in the playbooks. All the playbooks should contain the tasks to be executed. A task field includes the name of the task. It is not mandatory but useful for debugging the playbook. Internally each task links to a piece of code called a module. A module should be executed, and arguments that are required for the module you want to run.|

## Ansible Roles

* Roles provide a framework for fully independent or interdependent collections of files, tasks, templates, variables, and modules.

* The role is the primary mechanism for breaking a playbook into multiple files. This simplifies writing complex playbooks and makes them easier to reuse. The breaking of the playbook allows you to break the playbook into reusable components.

* Each role is limited to a particular functionality or desired output, with all the necessary steps to provide that result either within the same role itself or in other roles listed as dependencies.

* Roles are not playbooks. Roles are small functionality that can be used within the playbooks independently. Roles have no specific setting for which hosts the role will apply.

* Top-level playbooks are the bridge holding the hosts from your inventory file to roles that should be applied to those hosts.

### Creating a Role

The directory structure for roles is essential to creating a new role, such as:

**Role Structure**

The roles have a structured layout on the file system. You can change the default structured of the roles as well.

**For example**, let us stick to the default structure of the roles. Each role is a directory tree in itself. So the role name is the directory name within the /roles directory.

```

$ ansible-galaxy -h 

```

**Usage**

```
ansible-galaxy [delete|import|info|init|install|list|login|remove|search|setup] [--help] [options] ...  

```

**Options**


-h: (help) it shows this help message and exit.
-v: (verbose) Verbose mode (-vvv for more, -vvvv to enable connection debugging).
--version: it shows program version number and exit.


**Roles are stored in separate directories and have a particular directory structure**

```

[root@ansible-server test2]# tree  
.  
`-- role1  
    |-- defaults  
    |   `-- main.yml  
    |-- handlers  
    |   `-- main.yml  
    |-- meta  
    |   `-- main.yml  
    |-- README.md  
    |-- tasks  
    |   `-- main.yml  
    |-- tests  
    |   |-- inventory  
    |   `-- test.yml  
    `-- vars  
        `-- main.yml  

```
### Explanation

* The YAML file in the default directory contains a list of default variables that are to be used along with the playbook.

* The handler's directory is used to store handlers.

* The meta-directory is supposed to have information about the author and role dependencies.

* The tasks directory is the main YAML file for the role.

* The tests directory contains a sample YAML playbook file and a sample inventory file and is mostly used for testing purposes before creating the actual role.

* The vars directory contains the YAML file in which all the variables used by the role will be defined. The directory templates and the directory files should contain files and templates that will be used by the tasks in the role.

## Ansible Variables

In playbooks, the variable is very similar to using the variables in a programming language. It helps you to assign a value to a variable and use it anywhere in the playbook. You can put the conditions around the value of the variables and use them in the playbook accordingly.

**Creating Valid Variable Names**

Before start using variables, it's important to know what valid variable names are.

Variable names should be letters, numbers, and underscores. The variable should always start with a letter.

foo_port and foo2 both are the correct or valid variable names.

Foo-port, foo port, foo.port, and 10foo all are invalid variable names.

YAML supports dictionaries that map keys to values. For instance:

```

foo:  
  field1: one  
  field2: two  

```


Then you can reference a specific field in the dictionary using either bracket notation or dot notation:

```

foo['field1']  
foo.field1  

```

Both will reference the same value "one". But, if you choose to use dot notation, be aware that some keys can cause problems because they collide with the attributes and methods of python dictionaries. You should use bracket notation instead of dot notation if you use keys which start and end with two underscores or any of the known public attributes:

### Examples

```

- hosts : <your hosts>   
vars:  
tomcat_port : 8080 

```

In the above example, defined a variable name tomcat_port and assigned the value 8080 to the variable and can use it in your playbook wherever required.

The below code is from one of the roles (install-tomcat), such as:

```

block:   
   - name: Install Tomcat artifacts   
      action: >   
      yum name = "demo-tomcat-1" state = present   
      register: Output   
            
   always:   
      - debug:   
         msg:   
            - "Install Tomcat artifacts task ended with message: {{Output}}"   
            - "Installed Tomcat artifacts - {{Output.changed}}"   

```

**Explanation**

* **block**: The Ansible syntax to execute a given block.

* **name**: It is used in logging and helps in debugging which all blocks were successfully executed.

* **action**: The action is an Ansible keyword used in YAML.


* **register**: The output of the action tag is registered by using the register keyword.

* **always**: It is also an Ansible keyword; it says that below will still be executed.


* **msg**: It displays the message.



