# Ansible

![Ansible](/images/Ansiblelogo.png)

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

U can refer the video for installing the Ansible on docker : https://www.youtube.com/watch?v=Sf8urGA-Yhs&ab_channel=RedAakash

For more refer the Official document of Ansible : https://docs.ansible.com/ansible/latest/installation_guide/index.html


## Setup Environment in AWS

* First Login to AWS account.

* Go to instances running and Launch an instance as shown in the fig

![aws](/images/aws1.png)

* Give the name to the server and select the Operating system , here i have choosed the Ubuntu

![aws](/images/aws2.png)

* Create the Key pair .The key pair will be downloaded and stored in the local machine.

![aws](/images/aws3.png)

* Once the instance has been created go to **Actions** in the menu bar and selcet **Image and Templates** and **Lauch more like this** 

![aws](/images/aws4.png)

* Select the specified amount of instances required and click on the launch , here i have launched 3 instances

* Once the insatnces have been created edit the name as you like.

the final output should look like this.

![aws](/images/aws5.png)

### Installing Ansible in instance

* Connecting with other servers canbe done by installing the ansible in one of the instances 

* Connect the server through EC2 instance on which u want to install the ansible server and click the connect button as shown in fig:

![connect](/images/c1.png)

![connect](/images/c2.png)

* The EC2 instance shell will be opened. updtae the instance using the following command

**sudo apt update**

![connect](/images/c3.png)

install the ansible using the following command:

**sudo apt install ansible**

Ansible will be installed in the Current instance.

![connect](/images/c4.png)

### Connecting with servers

* In order to connect with other server you need to have an ssh in the instance.can create by following the below steps

**cd .ssh**

**vim ansible_key**


![connect](/images/c5.png)

* Create file and paste the key pair you have generated before.

![connect](/images/c6.png)

* To make an SSH key file readable in an AWS instance use the command 

**chmod 400 /path/to/your/key.pem**

* Replace /path/to/your/key.pem with the actual path to your SSH key file.

* Once u have  key pair u can connect to other server by connecting it's IP adress as shown in image:

**ssh -i ~/.ssh/ansible_key ubuntu@IP**

![connect](/images/c7.png)

* Create a inventory file in order to place the hosts

![connect](/images/c10.png)

* inside a hosts place the servers like this

![connect](/images/c12.png)

Refer the video for Environment setup in aws : https://www.youtube.com/watch?v=SGB7EdiP39E&t=993s&ab_channel=TrainWithShubham


## Ansible ad-hoc Commands

* Ad-hoc commands in Ansible refer to one-line commands that are used for performing quick tasks or operations on remote hosts without the need for writing a full-fledged playbook.

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

### commands

Will Create first Ansible ad hoc command and at the same time validate that our inventory is configured as expected. Let’s go ahead and execute a ping command against all our hosts:

**ansible all -m ping -i /home/ubuntu/ansible/hosts --private-key=~/.ssh/ansible_key**

![adhoc](/images/adhoc1.png)

seems like we can successfully ping the 3 hosts that we have defined in our hosts file.

Next, run a live command only to the server1 node by using the **–limit** flag

**ansible all -i /home/ubuntu/ansible/hosts --limit server1 -a "/bin/echo hello" --private-key=~/.ssh/ansible_key**

![adhoc](/images/adhoc2.png)

Next will run a command to check the Memory Usage

**ansible all -a "free-h"  -i /home/ubuntu/ansible/hosts --private-key=~/.ssh/ansible_key**

![adhoc](/images/adhoc3.png)

Run a command to check the servers **uptime**

ansible servers -a "uptime"  -i /home/ubuntu/ansible/hosts --private-key=~/.ssh/ansible_key

![adhoc](/images/adhoc4.png)


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

Lets Create a directory inside a master server where ansible is installed 

**mkdir playbooks**

![pb1](/images/PB1.png)

Change to the Playbook directory

**cd playbooks**

![pb2](/images/PB2.png)

Create a file with .yml or .yaml extension

**Vim create_file.yml**

![pb3](/images/PB3.png)



Let's start by writing an example YAML file. First, we must define a task. These are the interface to ansible modules for roles and playbooks.

**Example:**

```
---  
   
- name: This Playbook will create a file
  hosts: all
  become: true
  tasks:
  - name: create a file
   file:
    path: /home/ubuntu/newfile.txt
    state: touch

```

Above is a basic syntax of a playbook. Save it in a file as create_file.yml. A YAML syntax needs to follow the correct indentation.

Run the Playbook by following command

```

ansible—playbook create_file.yml -i /home/ubuntu/ansible/hosts --private—key=~/.ssh/ansible_key

```

![pb4](/images/PB4.png)

You  will find the file in the targeted hosts:

![pb5](/images/PB5.png)




### YAML Tags

Here are some YAML tags are given below, such as:

|  Tags     | Explanation  |
|-----------|--------------|
| Name	    |It specifies the name of the Ansible Playbooks.|
| Hosts	    |It specifies the lists of the hosts against which you want to run the task. And the host's Tag is mandatory. It tells Ansible that on which hosts to run the listed tasks. These tasks can be run on the same machine or the remote machine. One can run the tasks on the multiple machines, and the host's tag can have a group of host's entry as well.|
| Vars	    |Vars tag defines the variables which you can use in your playbook. Its usage is similar to the variables in any programming language.|
| Tasks	    |Tasks are the lists of the actions which need to perform in the playbooks. All the playbooks should contain the tasks to be executed. A task field includes the name of the task. It is not mandatory but useful for debugging the playbook. Internally each task links to a piece of code called a module. A module should be executed, and arguments that are required for the module you want to run.|

For more details on playbook refer official documentation: https://docs.ansible.com/ansible/latest/playbook_guide/index.html


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
---
- name: Install packages
  hosts: all
  become: yes
  vars:
    ec2_instance_id: "i-0786c3d298aaa22e0"
  tasks:
    - name: Display instance ID
      debug:
        msg: "Instance ID: {{ ec2_instance_id }}"


```

Run the Ansible Playbook by following command

```

ansible—playbook variable.yml -i /home/ubuntu/ansible/hosts --private—key=~/.ssh/ansible_key

```



![vars](/images/vars.png)

**Explanation**

1.The --- at the beginning indicates the start of a YAML document.

2.The name field provides a descriptive name for the playbook. In this case, it's "Install packages."

3.The hosts field specifies the group of hosts that the playbook will run against. In this case, it's the ansible_host group defined in the inventory file (inventory.ini). This means the playbook will run against the EC2 instance with the specified public IP address.

4.The become field is set to yes, which means the playbook will run with elevated privileges (usually using the sudo command) to perform tasks that require administrative access.

5.The vars field is used to define variables specific to this playbook. In this example, we define a variable named ec2_instance_id and set it to <your_ec2_instance_id>. You should replace <your_ec2_instance_id> with the actual ID of your EC2 instance.

6.The tasks field contains a list of tasks that Ansible will execute on the target host(s).

7.In this playbook, we have a single task with the name "Display instance ID." The debug module is used to print a message to the console. In this case, we display the value of the ec2_instance_id variable using the msg field.

8.The {{ ec2_instance_id }} syntax is used to access the value of the ec2_instance_id variable within the message.


## Ansible Tags

* In Ansible, tags are labels or identifiers that you can assign to tasks or plays in a playbook. 

* They provide a way to selectively run specific tasks or plays based on the tags assigned to them. 

* Tags are useful when you want to execute only a subset of tasks or plays in a playbook, rather than running the entire playbook.

* In Ansible, tags can be applied to many structures, but its simplest use is with individual tasks. Let's see an example that tags three tasks with different tags, such as:

**Example**

```

---
- name: Install packages on EC2 instance
  hosts: server1
  become: yes
  tasks:
    - name: Install nginx
      apt:
        name: nginx
        state: present
      tags:
        - package1

    - name: Install MySQL server
      apt:
        name: mysql-server
        state: present
      tags:
        - package2

    - name: Install Python packages
      apt:
        name:
        - python3
        - python3-pip
        - python3-dev
        state: present
      tags:
        - package3


```

In this example, we have three tasks that install different packages on the EC2 instance on server1.

* The first task installs the nginx package.

* The second task installs the mysql-server package.

* The third task installs multiple packages related to Python development, including python3, python3-pip, and python3-dev.

To run specific tasks or plays based on tags, you can use the --tags or --skip-tags options with the ansible-playbook command.

Run the Ansible Playbook by following command

```

ansible—playbook variable.yml --tags all  -i /home/ubuntu/ansible/hosts --private—key=~/.ssh/ansible_key

```

![tags](/images/tags.png)

### Tags


**Special Tags**

"always" is a unique tag that will always run a task, unless specifically skipped (--skip-tags always)

**For example**:

```

tasks:  
- debug:  
    msg: "Always runs"  
  tags:  
  - always  
  
- debug:  
    msg: "runs when you use tag1"  
  tags:  
  - tag1  

```

**New in version 2.5**

Here is another unique tag that is "never" which prevents a task from running unless a tag is specifically requested.

**For example**:

```

tasks:  
  - debug: msg="{{ showmevar }}"  
    tags: [ never, debug ]  

```

In the above example, the task will only run when the "never" or "debug" tag is explicitly requested.

Here are another three special keywords for tags:

"**tagged**" which run only tagged,

"**untagged**" which run only untagged, and

"**all**" which run all tasks respectively.

By default, Ansible runs as if "**--tags**" all had been specified.

## Ansible Modules

* Ansible modules are discrete units of code which can be used from the command line or in a playbook task.

* The modules also referred to as task plugins or library plugins in the Ansible.

* Ansible ships with several modules that are called module library, which can be executed directly or remote hosts through the playbook.

Users can also write their modules. These modules can control like services, system resources, files, or packages, etc. and handle executing system commands.

Let's see how to execute three different modules from the command line.

```

ansible webservers -m service -a "name=httpd state=started"  
ansible webservers -m ping  
ansible webservers -m command -a "/sbin/reboot -t now"  

```
Each module supports taking arguments. Mainly all modules take key=value arguments, space delimited.

Some module takes no arguments, and the shell/command modules take the string of the command which you want to execute.

From playbook, Ansible modules execute in a very similar way, such as:

```

- name: reboot the servers  
  command: /sbin/reboot -t now

```

Here is another way to pass arguments to a module that is using YAML syntax, and it is also called complex args.

```

- name: restart webserver  
  service:  
    name: httpd  
    state: restarted 

```
Technically, all modules return JSON format data, though command line or playbooks, you don't need to know much about that. If you're writing your module, it means you do not have to write modules in any particular language which you get to choose.

Modules should be idempotent and avoid making any changes if they detect that the current state matches the desired final state. When using Ansible playbooks, these modules can trigger "change events" in the form of notifying "handlers" to run additional tasks.

Documentation for each module can be accessed from the command line with the Ansible-doc tool:

```

ansible-doc yum 

```

For more details on module refer official documentation:https://docs.ansible.com/ansible/latest/module_plugin_guide/index.html

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

**For example**, let us stick to the default structure of the roles. 

```

playbooks/
├── install_packages/
│   └── tasks/
│   |    └── main.yml
|   └── vars/
|          └──main.yml
└── install.yml

```

1.Update the tasks/main.yml file in the install_packages role with the following content:

```

---
- name: Install packages
  become: yes
  apt:
    name: "{{ packages }}"
    state: present

```

2.Create the install.yml playbook file with the following content:

```

---
- name: Install packages on EC2 instance
  hosts: server2
  become: yes
  roles:
    - install_packages

```

3.Create the vars/main.yml file in the install_packages role with the following content:

```

---
packages:
  - nginx
  - mysql-server
  - python3
  - python3-pip
  - python3-dev

```

Run the playbook using the ansible-playbook command:

```

ansible-playbook install.yml -i /home/ubuntu/ansible/hosts   --private-key=~/.ssh/ansible_key

```

![roles](/images/roles.png)


### Explanation

The directory structure is organized as follows:

```

playbooks/
├── install_packages/
│   └── tasks/
│   |    └── main.yml
|   └── vars/
|          └──main.yml
└── install.yml

```
The  install_packages directory represents the role, containing the tasks directory, which contains the main.yml file. The install.yml file is the playbook file.


* The tasks/main.yml file within the install_packages role contains the task that installs packages. It uses the apt module to install packages specified in the packages variable. The **become**: yes line allows the task to run with elevated privileges.

* The roles.yml playbook file is responsible for orchestrating the installation of packages on the EC2 instance. It specifies the playbook name, the target hosts (server1), and that privileged access is required (become: yes). The roles section includes the install_packages role, which will be executed as part of the playbook.

* The vars/main.yml file within the install_packages role contains the packages variable, which is a list of packages to be installed. In this case, it includes the package names nginx, mysql-server, python3, python3-pip, and python3-dev.

* When you run the ansible-playbook command, make sure you execute it from the playbooks directory. The playbook will execute the install_packages role and install the specified packages on the EC2 instance specified in the inventory file.

By organizing the tasks, variables, and files into roles, you can modularize your Ansible code, making it reusable and easier to maintain.

## Ansible Galaxy

Ansible Galaxy is a galaxy website where users can share roles and to a command-line tool for installing, creating, and managing roles.

Ansible Galaxy gives greater visibility to one of Ansible's most exciting features, such as application installation or reusable roles for server configuration. Lots of people share roles in the Ansible Galaxy.

Ansible roles consist of many playbooks, which is a way to group multiple tasks into one container to do the automation in a very effective manner with clean, directory structures.

**Ansible Galaxy Commands**

Here are some helpful Ansible Galaxy commands, such as:

**To display the list of installed roles, with version numbers.**

```

ansible-galaxy list  

```

**To remove an installed role.**

```

ansible-galaxy remove [role] 

```

**To create a role template suitable for submission to Ansible Galaxy.**

```

ansible-galaxy init

```

### Example

In this example we are going to apply Apache role to EC2 instance

Make sure you have installed the geerlingguy.apache role using the ansible-galaxy command before running the playbook:

```

ansible-galaxy install geerlingguy.apache

```

![galaxy](/images/galaxy1.png)

Ensure that the role is successfully installed and located in the proper location.

Create a yml file in the playbook and run the following command:

```

---
- name: Apply Apache role to EC2 instance
  hosts: server3
  become: yes
  roles:
    - geerlingguy.apache

```

This should apply the geerlingguy.apache role to the EC2 instance.

![galaxy](/images/galaxy2.png)


## Ansible Shell

* Ansible shell module is designed to execute the shell commands against the target UNIX based hosts. Ansible can run except any high complexes commands with pipes, redirection. And you can also perform the shell scripts using the Ansible shell module.

* The main advantage of the Ansible shell is except any high complexes commands with pipes and semicolons can be a disadvantage from the security perspective as a single mistake could cost a lot and break the system integrity.

* The Ansible shell module is designed to work only with LINUX based machines and not for the windows. For windows, you should use the win_shell

* Ansible shell module can be used to execute shell scripts. Ansible has a dedicated module named script, which is used to copy the shell script from the control machine to the remote server.

Let see the syntax of how to use the Ansible shell module in the playbook and Adhoc:

**Syntax of Ansible shell module in a playbook**

The beauty of the playbook is the way it looks and written. A playbook is written in YAML so it can be easily understood.

The below image demonstrates how an Adhoc command would be transformed as a play of an Ansible playbook.

![shell](/images/ansible-shell.png)

**Syntax of Ansible shell module in Adhoc**

The below image shows a quick syntax of the Ansible shell module in Adhoc manner.

![shell2](/images/ansible-shell2.png)

### Example

This example will execute the shell command on the specified remote host and display the output.

 Below is an example that executes a single command using the Shell module in a remote host.

```

---
- name: Execute Shell command on remote host
  hosts: server2
  become: yes
  tasks:
    - name: Run Shell command
      shell: echo "Hello, world!"
      register: result

    - name: Display command output
      debug:
        var: result.stdout


```

In this example:

* The shell module is used to execute the echo command on the remote host, which simply prints "Hello, world!".

* The register keyword is used to capture the output of the shell command into the result variable.

* The debug module is used to display the value of result.stdout, which contains the standard output of the shell command.

Run the Playbook by following command

```

ansible—playbook shell.yml -i /home/ubuntu/ansible/hosts --private—key=~/.ssh/ansible_key

```

![shell](/images/shell.png)

**Note:**

However, it's worth noting that whenever possible, it is recommended to use Ansible's idempotent modules (such as apt, copy, service, etc.) that are specifically designed to manage various aspects of system configuration. The shell module should be used sparingly when there is no suitable existing module available.



## Ansible Templates

* Ansible is used to manage configurations of multiple servers and environments. But these configuration files can vary for each cluster or remote server. But apart from a few parameters, all other settings will be the same.

* Creating static files for each of these configurations is not an efficient solution. It will take a lot of time, and every time a new cluster is added, then you have to add more files. If there is an efficient way to manage these dynamic values, it would be beneficial. This is where Ansible template modules come into play.

* A template is a file that contains all your configuration parameters, but the dynamic values are given as variables in the Ansible. During the playbook execution, it depends on the conditions such as which cluster you are using, and the variables will be replaced with the relevant values.

* You can do more than replacing the variables with the help of the Jinj2 templating engine. You can have loops, conditional statements, write macros, filters for transforming the data, do arithmetic calculations, etc.

Usually, the template files will have the .j2 extension, which denotes the Jinja2 templating engine used.

The double curly braces will denote the variables in a template file, **'{{variables}}'**.

We need to have two parameters when using the Ansible Template module, such as:

* **src**: The source of the template file. It can be a relative and absolute path.

* **dest**: Dest is the destination path on the remote server.

### Template Module Attributes

Here are some other parameters which can be used to change some default behavior of the template module:

* **Force**: If the destination file already exists, then the Force parameter will decide whether it should be replaced or not. By default, the value is yes.

* **Mode**: This parameter is used to set the permissions for the destination file explicitly.

* **Backup**: If you want a backup file to be created in the destination directory, you should set the value of the backup parameter to yes. By default, the value is no. and the backup file will be created every time there is a change in the destination directory.

* **Group**: Name of the group that should own the directory. It is similar to executing chown command for a file in Linux systems.

**Example**

In the below example, we are using the template module on the example1.j2 file that replaces the default variables with values given in the playbook.

**File: Playbook.yml**

```

---  
- hosts: all  
  vars:  
    variable1: 'Hello'  
    variable2: 'My first playbook using template'  
  tasks:  
    - name: Basic Template Example  
      template:  
        src: example1.j2  
        dest: /home/knoldus/Documents/Ansible/output.txt  

```
**File: example1.j2**   

```

{{variable1}}  
No change in this line  
{{variable2}}  

```

**File: output.txt**

```

Hello
No change in this line
My first playbook using the template

```

You can see, their values replace both variables in the example1.j2 in the above example.

## Ansible YAML

* YAML is used to describe configuration that has been increasing in the past few years with the help of Ansible and SaltStack.

* YAML is more easy to understand compared to other standard data formats such as XML or JSON.  

* All YAML files (regardless of their association with Ansible or not) can optionally begin with --- and end with ---. This is part of the YAML format and indicates the start and end of a document.

All members of a list are lines beginning at the same indentation level starting with a "-" (a dash and space):

```

---  
# A list of colors  
- White  
- Green  
- Red  
- Black  
---  

```

We have different ways in which the YAML data is represented, such as:

**Key-value Pair**

YAML uses the Key-Value pair to represent the data. And the dictionary is described in the key: value pair.

**For example**, a student record

```

---  
# A student record  
Martin:  
name: Kiran   
roll no: 10  
class: 12th  
div: A  
---  

```

**Abbreviation**

We can also use the abbreviation to represent the directories:

```

Martin: [name: Kiran, roll no: 10, class: 12th, div: A] 

```

### Representing List

We can also represent List in YAML. Every element (member) of the list should be written in a new line with the same indentation starting with "-" (- and space).

**For example**: Name of the countries

```

---  
#Name of country   
Countries:    
   - India   
   - China   
   - USA  
   - Russia   
--- 

```

**Abbreviation**

To represent the list, we can also use the abbreviation method:

```

Countries: ['India', 'China', 'USA', 'Iceland']  

```

**List inside Dictionaries**

We can use the list inside dictionaries, i.e., the value of a key is a list.

**For example**, a student record

```

---  
# A student record  
Martin:  
name: Martin   
roll no: 10  
class: 12th  
div: A  
likes:  
- Physics   
- Chemistry  
- Math   
--- 

```

**List of Directories**

We can also make a list of directories:

**For example**:

```

---  
# A student record  
- Martin:  
name: Martin   
roll no: 10  
class: 12th  
div: A  
likes:  
- Physics   
- Chemistry  
- Math   
- Edward:  
 name: Edward  
 roll no: 11  
class: 12th  
div: A  
likes:   
- Biology   
- English   
--- 

```

YAML uses "|" to include newlines while showing multiple lines and ">" to suppress newlines while showing various lines. Due to this, we can read and edit long lines. In both cases, the indentation will be ignored.

We can also represent Boolean (True/false) values in YAML, where Boolean values can be case insensitive.

**For example**, a student result

```

---    
#a student result   
- Martin:  
name: Martin   
roll no: 10  
class: 12th  
div: A  
likes:  
- Physics   
- Chemistry  
- Math   
     
   result:   
      Physics: 70   
     Chemistry: 45   
Math: 85  
Biology: 65  
      English: 80   
     
   passed: TRUE   
     
   messageIncludeNewLines: |   
      Congratulation!!   
      You passed with 79%   
     
   messageExcludeNewLines: >   
      Congratulation!!   
      You passed with 79%   
---

```

## Ansible Inventory

* Ansible works against multiple managed hosts in your infrastructure at the same time, using a list or group of lists is known as the inventory.

* Once an inventory is defined, you use patterns to select the hosts or groups you want to run against to Ansible.

* The default location for inventory is a file called /etc/ansible/hosts. You can also specify a different inventory file at the command line using the -i <path> option. 

* You can pull the inventory file from dynamic or cloud sources or different formats (YAML, ini). Ansible has inventory plugins to make it flexible and customize.

**Hosts and group**

The format is /etc/ansible/ hosts are in INI like format, such as:

```

mail.example.com  
  
[webservers]  
foo.example.com  
bar.example.com  
  
[dbservers]  
one.example.com  
two.example.com  
three.example.com

```

Heading in the brackets is a group name, which is used in classifying the systems. And deciding what policy you are controlling at what time and for what purpose. You can put the systems in more than one group.

For example, a server could be both a dbserver and a webserver.

If you have hosts that run on a non-standard SSH port, then you can put the port number after the hostname with the colon. The Ports listed in the SSH configuration file that can be used with the OpenSSH connection but not use with the paramiko connection.

To makes things explicit, it is suggested that you set them if items are not running on the default ports:

```

badwolf.example.com:5309

```

Suppose you have static IPs and want to set up some aliases that live in your host file, or you can connect through tunnels. Also, you can describe the hosts like the below example:

```

Jumper ansible_port=5555 ansible_host=192.0.2.50  

```

In the above example, trying to Ansible against the host alias "jumper" will connect 192.0.2.50 on port 5555. It is using features of the inventory file to define the special variables.

### Hosts Variables

You can assign the variables to the hosts that will be used in playbooks, such as:

```

[atlanta]  
host1 http_port=80 maxRequestsPerChild=808  
host2 http_port=303 maxRequestsPerChild=909 

```

**Group Variables**

The variables can be applied to an entire group at once, such as:

```

[atlanta]  
host1  
host2  
  
[atlanta:vars]  
ntp_server=ntp.atlanta.example.com  
proxy=proxy.atlanta.example.com

```

**Groups of Groups and Group Variables**


It is possible to make groups of the group using the :children's suffix. And you can apply variables using :vars.

```

[atlanta]  
host1  
host2  
  
[raleigh]  
host2  
host3  
  
[southeast: children]  
Atlanta  
Raleigh  
  
[southeast:vars]  
some_server=foo.southeast.example.com  
halon_system_timeout=30  
self_destruct_countdown=60  
escape_pods=2  
  
[usa: children]  
southeast  
northeast  
southwest  
northwest 

```

## Ansible Debug

Ansible provides a debug module option that makes the tasks more manageable. It is a handy tool to figure out any problem areas.

Ansible version 2.1 extended the debug module with a verbosity parameter that transforms it from a print line.

**For example**: Let's create the playbook debug.yml, such as:

```

---
- name: Debug Example
  hosts: server2
  become: yes
  tasks:
    - name: Print debug message
      debug:
        msg: "This is a debug message."

    - name: Set a variable
      set_fact:
        my_var: "Hello, world!"

    - name: Print variable value
      debug:
        var: my_var
  

```

In this example:

* The debug module is used to print a debug message "This is a debug message." during playbook execution.

* The set_fact module is used to set a variable my_var with the value "Hello, world!".

* The debug module is used again to print the value of the my_var variable.

Run the Playbook by following command

```

ansible—playbook debug.yml -i /home/ubuntu/ansible/hosts --private—key=~/.ssh/ansible_key

```

![debug](/images/debug.png)


During the Ansible playbook debugging, it is useful to know how to display the registered variables or host facts.

To print a message from the Ansible playbook, as well as a value of a variable, we can use the Ansible debug module. Ansible debug module is easy to use.

For example: Let's execute a simple hello world playbook 2_debug_example.yml, such as:

```

---  
- name: Debug Example - Hello World  
hosts: localhost  
tasks:  
- name: Print debug message  
debug: 

```
the Ansible includes a debugger as a part of the strategy plugins. This debugger enables you to debug as a task. You have access to all the features of the debugger in the context of the task. You can check or set the value of variables, update module arguments, and re-run the task with the new variables and arguments to resolve the cause of the failure.



###  Debugger Keyword 

**There are many ways to invoke the debugger, such as:**

The debugger keyword can be used on any block where you provide a name attribute such as a role, block, task, or play.

The debugger keyword accepts several values, such as:

**Always**: Always invokes the debugger, regardless of the outcome.

**Never**: Never invokes the debugger, regardless of the outcome.

**On_failed**: It only invokes the debugger if a task fails.

**On_unreachable**: It only invokes the debugger if the host was unreachable.

**On_skipped**: It only invokes the debugger if the task is skipped.

**On a Task**

```

- name: Execute a command  
  command: false  
  debugger: on_failed  

```

**On a play**

```

- name: Play  
  hosts: all  
  debugger: on_skipped  
  tasks:  
    - name: Execute a command  
      command: true  
      when: False  

```

When a provided at the general level, and a more specific level, the more particular wins:

```

- name: Play  
  hosts: all  
  debugger: never  
  tasks:  
    - name: Execute a command  
      command: false  
      debugger: on_failed

```

## Ansible Apt

APT stands for "Advanced Packaging Tool" is the preferred package management toolset in Ubuntu. It allows us to install new packages, update them, and remove the packages from Ubuntu or Debian systems. Here are 3 APT related command-line tools, such as:

**Apt-get**: All the basic package management operations can be done by using this tool. Ansible apt-get module provides this functionality.

**Apt-add-repository**: It is used for adding a new repository to the repository list. The default repository may not have the latest version of all the packages. So you need to add additional repositories for some software maintainers. Ansible apt_repository module provides the functionality for adding a new repository.

**Apt-key**: It is used to manage the list of keys for authenticating apt packages. Ansible apt_key module is used to manage the keys.

**Installing new Apt Packages**


To install the new packages, you have to give the name of the package in the name parameter and the desired state of the package.

The default state of the package is "present". Also, it is better to set the update_cache to true. Thus you can ensure the indexes are synchronized with the sources list. It is the same as running the apt-get update command before installing a package.

The below example will do a cache update to synchronize the index. Check if the 'zip' package is installed on the target server. And if it is not installed, the package will be installed. If the package is already installed, then it won't be upgraded.

```

---
- name: Manage Packages
  hosts: server2
  become: yes
  tasks:
    - name: Update package cache
      apt:
        update_cache: yes

    - name: Install zip package
      apt:
        name: zip
        state: present


```

Run the Playbook by following command

```

ansible—playbook apt.yml -i /home/ubuntu/ansible/hosts --private—key=~/.ssh/ansible_key

```

![apt](/images/apt.png)

In this example:

* The apt module is used to update the package cache on the remote host by setting update_cache to yes. This ensures that the package indexes are synchronized with the sources list.

* The apt module is used again to install the package zip by setting name to zip and state to present. This will install the package if it's not already installed. If the package is already present, it won't be upgraded.

### Installing new Apt Packages

1.**Installing the latest version of a package**

If you set the state of the packages to "present", then Ansible will only check if the package is present. So if the new package is available, it will not be able to install.

If you want to install the latest apt packages, then you have to set the state parameter to the latest.

This will ensure the package with the latest version is installed. The below example will update the cache first, then install the latest package of zip, such as:

```

-hosts: server 
tasks:  
-name: ansible apt install latest version  
apt:  
name: zip  
state: latest  
update_cache: true 

```

2.**Ansible install multiple packages**

Instead of writing multiple tasks to install packages, you can use with_items and combine those tasks.

In the below example, we are going to install 3 packages: docker-ce, Nginx, and git.

```

-hosts: server 
tasks:  
-name: ansible apt with_items   
apt:  
name: "{{item}}"  
update_cache: true  
state: present  
with_items:  
-'docker-ce'  
-'nginx'  
-'git'

```
3.**Ansible Apt ad-hoc**

You can also use the ad-hoc method to install new packages using the apt module, such as:

```

ansible all -m apt -a "name=nginx state=absent" -i inventory.ini  

```

**Removing Apt Packages**

You can also remove the packages using apt module by setting the state parameter to absent.

The below example will remove the zip package. Since the module is idempotent, it will not go through an error if the package is not present.

```

-hosts: server 
tasks:  
-name: ansible apt remove package   
apt:  
name: zip  
state: absent 

```

## Ansible Lineinfile

* The lineinfile is one of the most powerful modules in the Ansible toolbox. Ansible lineinfile module is used to insert a line, modify, remove, and replace an existing line.

* Ansible lineinfile module saves your time when you work with the file and modify their content on the run, such as adding a new line in the file or updating, replace a line in the file when specific text is found, and much more.

* Ansible lineinfile provides many parameters to do the job quickly. You can also use the condition to match the line before modifying, removing using the regular expressions. You can reuse and modify the matched line using the backreference parameter.

**NOTE**: Ansible lineinfile can be used only for working a single line in a file. If you want to replace multiple lines, replace the module, and if you're going to insert, update, remove a block of lines in a file use blockinfile module.

**Insert a Line**

lets see how to insert a Line in a file in the targeted hosts

```

---
- name: Insert Line in File
  hosts: server1
  become: yes
  tasks:
    - name: Insert line in file
      lineinfile:
        path: /home/ubuntu/file.txt
        line: "This line will be inserted"
        insertafter: '^Specific line'
 

```

Run the Playbook by following command

```

ansible—playbook insertline.yml -i /home/ubuntu/ansible/hosts --private—key=~/.ssh/ansible_key

```

![lif](/images/lif1.png)

to check whether it is inserted or not u can check the host by executing the following command as shown in image:

Run the Playbook by following command

```

ansible—playbook insertline.yml -i /home/ubuntu/ansible/hosts --private—key=~/.ssh/ansible_key

```

![lif](/images/lif2.png)

In this example:

* The lineinfile module is used to insert the line "This line will be inserted" into the file /home/ubuntu/file.txt.

* The insertafter parameter specifies that the line should be inserted after the line matching the regular expression ^Specific line. Modify ^Specific line with the appropriate regular expression to identify the specific line after which you want to insert the new line.


### Removig a line

Set the state parameter to absent or remove the line specified. All the occurrence of that line will be removed.

```

---
- name: Remove Line from File
  hosts: server1
  become: yes
  tasks:
    - name: Remove line from file
      lineinfile:
        path: /home/ubuntu/file.txt
        state: absent
        line: "This line will be inserted"


```

Run the Playbook by following command

```

ansible—playbook insertline.yml -i /home/ubuntu/ansible/hosts --private—key=~/.ssh/ansible_key

```

![lif](/images/lif3.png)

u can see the line inserted in the previous example has been deleted

![lif](/images/lif4.png)

In this example:

* The lineinfile module is used to remove the line "This line will be inserted" from the file /home/ubuntu/file.txt.

* The state parameter is set to absent to indicate that the line should be removed from the file.



### Replacing or Modifying a Line

To modify a line, you need to use the Ansible backrefs parameter along with the regexp parameter. This should be used with state=present.

If the regexp does not match any line, then the file is not changed. If the regexp matches a line or multiple lines, then the last matched line will be replaced. The grouped elements in regexp are populated and can be used for modification.



```

---
- name: Replace Line in File
  hosts: server1
  become: yes
  tasks:
    - name: Replace line in file
      lineinfile:
        path: /home/ubuntu/file.txt
        regexp: '^This line will be inserted'
        line: "This line has been replaced"
 

```

Run the Playbook by following command

```

ansible—playbook insertline.yml -i /home/ubuntu/ansible/hosts --private—key=~/.ssh/ansible_key

```


![lif](/images/lif5.png)

u can see the above line has been replace/modified

![lif](/images/lif6.png)

In this example:

* The lineinfile module is used to replace the line that starts with "This line will be inserted" with "This line has been replaced" in the file /home/ubuntu/file.txt

* The regexp parameter is used to specify the regular expression that matches the line to be replaced.
The line parameter is set to the new line that will replace the existing line.

## Ansible Copy

The copy module is used to copy files from the local machine (the control node where Ansible is being run) to the remote hosts. It provides various options for copying files, setting permissions, and modifying ownership.

If you want to copy files after substituting with variables, such as config files with IP changes, or you can use the template module also. You can perform a lot of complicated tasks with this module.

Copying Files from server to Remote

**Example:**

```

---
- name: Copy File to EC2 Instances
  hosts: server1
  become: yes
  tasks:
    - name: Copy file to remote hosts
      copy:
        src: /home/ubuntu/copyfile.yml/text.txt
        dest: /home/ubuntu/

```

Run the Playbook by following command

```

ansible—playbook copy.yml -i /home/ubuntu/ansible/hosts --private—key=~/.ssh/ansible_key

```

![copy](/images/copy1.png)

The text file which is present in the src path is copied to the targeted hosts

![copy](/images/copy2.png)

In this example:

* The copy module is used to copy the file from the local machine to the remote hosts .

* The src parameter specifies the path to the source file on the local machine (control node).

* The dest parameter specifies the path to the destination file on the remote hosts .

## Ansible File

Ansible file module is used to creating and deleting the file or multiple files in the remote server. You can also create and delete the directories and change the permissions of the data.

**Creating a File in Remote Server**

```

---
- name: Create File on Remote Server
  hosts: server1
  become: yes
  tasks:
    - name: Create file
      file:
        path: /home/ubuntu/newfile.txt
        state: touch

```

Run the Playbook by following command

```

ansible—playbook file.yml -i /home/ubuntu/ansible/hosts --private—key=~/.ssh/ansible_key

```

![file](/images/file.png)

This will create a newfile.txt file in targeted  Hosts/Remote server.

![file](/images/file2.png)

In this example:

* The file module is used to create a file on the remote server.

* The path parameter specifies the path and filename for the remote file.

* The state parameter is set to touch to indicate that the file should be created if it doesn't exist.

**Delete a file**

```

---
- name: Delete File on Remote Server
  hosts: server1
  become: yes
  tasks:
    - name: Delete file
      file:
        path: /home/ubuntu/file.txt
        state: absent

```

Run the Playbook by following command

```

ansible—playbook file.yml -i /home/ubuntu/ansible/hosts --private—key=~/.ssh/ansible_key

```

![file](/images/file6.png)




In this example:

* The file module is used to delete a file on the remote server.

* The path parameter specifies the path and filename of the file to be deleted.

* The state parameter is set to absent to indicate that the file should be deleted.



### Creating File with Permissions

We can also create the file with permission by using the file module.

At the mode parameter: we have 4 digits. Always mention zero at the starting, and remaining digits will be your file permissions.

```

---
- name: Create File on Remote Server
  hosts: remote_server
  become: yes
  tasks:
    - name: Create file
      file:
        path: /home/ubuntu/permission.txt
        state: touch
        mode: "0644"

```

Run the Playbook by following command

```

ansible—playbook file.yml -i /home/ubuntu/ansible/hosts --private—key=~/.ssh/ansible_key

```


![file](/images/file.png)

![file](/images/file4.png)

In this example:

* The file module is used to create a file on the remote server.

* The path parameter specifies the path and filename for the remote file.

* The state parameter is set to touch to indicate that the file should be created if it doesn't exist.

* The mode parameter is set to "0644" to specify the desired file permissions. The 0 prefix is used to indicate an octal value.

**Creating Multiple Files**

A path parameter: we can create a loop to create multiple files by using "{{item}}".

```

---
- name: Create Multiple Files on Remote Server
  hosts: remote_server
  become: yes
  tasks:
    - name: Create files
      file:
        path: "{{ item }}"
        state: touch
        mode: "0644"
      loop:
        - /path/to/remote/file1.txt
        - /path/to/remote/file2.txt
        - /path/to/remote/file3.txt

```

In this example:

* The file module is used within a loop to create multiple files on the remote server.

* The path parameter is set dynamically using the item variable, which represents each item in the loop.

* The state parameter is set to touch to indicate that the file should be created if it doesn't exist.

* The mode parameter is set to "0644" to specify the desired file permissions.

Make sure to replace remote_server with the appropriate host or host group name in your inventory file. Also, update the paths in the loop (/path/to/remote/file1.txt, /path/to/remote/file2.txt, etc.) with the actual paths and filenames for the files you want to create on the remote server.

**Deleting Multiple Files**

To delete multiple files on a remote server using Ansible, you can utilize the file module with the state parameter set to absent. 

```

---
- name: Delete Multiple Files on Remote Server
  hosts: remote_server
  become: yes
  tasks:
    - name: Delete files
      file:
        path: "{{ item }}"
        state: absent
      loop:
        - /path/to/remote/file1.txt
        - /path/to/remote/file2.txt
        - /path/to/remote/file3.txt

```

In this example:

* The file module is used within a loop to delete multiple files on the remote server.

* The path parameter is set dynamically using the item variable, which represents each item in the loop.

* The state parameter is set to absent to indicate that the files should be deleted.

Make sure to replace remote_server with the appropriate host or host group name in your inventory file. Also, update the paths in the loop (/path/to/remote/file1.txt, /path/to/remote/file2.txt, etc.) with the actual paths and filenames of the files you want to delete on the remote server.

## Install Docker in worker nodes

To install a Docker on your worker nodes , create a playbook file name called docker.yml in ~/playbooks folder

```
---
- name: Install Docker
  hosts: server1
  become: true
  remote_user: ubuntu
  

  tasks:
    - name: Update apt cache
      apt:
        update_cache: yes
      become: true

    - name: Install Docker dependencies
      apt:
        name: ['apt-transport-https', 'ca-certificates', 'curl', 'software-properties-common']
      become: true

    - name: Add Docker GPG key
      apt_key:
        url: https://download.docker.com/linux/ubuntu/gpg
        state: present

    - name: Add Docker APT repository
      apt_repository:
        repo: "deb [arch=amd64] https://download.docker.com/linux/ubuntu {{ ansible_lsb.codename }} stable"
        state: present

    - name: Update apt cache
      apt:
        update_cache: yes
      become: true

    - name: Install Docker
      apt:
        name: docker-ce
        state: present
      become: true

    - name: Start and enable Docker service
      service:
        name: docker
        state: started
        enabled: yes
      become: true

```

Run the command to install docker on the worker nodes

```

sudo ansible-playbook docker.yml -i ~/hosts --private-key=/home/ubuntu/.ssh/ansible_key

```

## Build Images in Docker

To Build images in  a Docker on your worker nodes , create a playbook file name called docker_build.yml in ~/playbooks folder

```

---
- name: Build Docker Image
  hosts: server1
  become: true
  remote_user: ubuntu
  tasks:
    - name: Clone GitHub repository
      git:
        repo: https://github.com/vijaynvb/todoapi.git
        dest: /home/ubuntu/docker/todo

    - name: Build Docker image
      command: docker build -t todoapi .
      args:
        chdir: /home/ubuntu/docker/todo

```

Run the command to build an image in docker on the worker nodes

```

sudo ansible-playbook docker_build.yml -i ~/hosts --private-key=/home/ubuntu/.ssh/ansible_key

```
## Build Container in Docker

To Build Container in  a Docker on your worker nodes , create a playbook file name called docker_container.yml in ~/playbooks folder

```

---
- name: Run Docker Image
  hosts: server1
  become: true
  remote_user: ubuntu
  tasks:
    - name: Run Docker container
      docker_container:
        name: my_container
        image: todoapi
        state: started
        ports:
          - "80:8081"

```

Run the command to build an container in docker on the worker nodes

```

sudo ansible-playbook docker_container.yml -i ~/hosts --private-key=/home/ubuntu/.ssh/ansible_key

```





