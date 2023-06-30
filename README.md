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

## Ansible Tags

If you have a large playbook, it becomes useful to be able to run only a specific part of it rather than running everything in the playbook. Ansible supports a tag attribute for this reason.

When you apply tags on things, then you can control whether they are executed by adding command-line options.

When you execute a playbook, you can filter tasks based on the tags in two ways, such as:

* On the command line, with the -tags or -skip-tags options.

* In Ansible configuration settings, with the TAGS_RUN and TAGS_SKIP options.

In Ansible, tags can be applied to many structures, but its simplest use is with individual tasks. Let's see an example that tags two tasks with different tags, such as:

```

tasks:  
- yum:  
    name: "{{ item }}"  
    state: present  
  loop:  
  - httpd  
  - memcached  
  tags:  
  - packages  
  
- template:  
    src: templates/src.j2  
    dest: /etc/foo.conf  
  tags:  
  - configuration

```

if you want to run the configuration and packages part of a very long playbook, then you can use the -tags option on the command line.

```

ansible-playbook example.yml --tags "configuration,packages"  

```

And if you want to run a playbook without certain tagged tasks, then you can use the -skip-tags command-line option.

```

ansible-playbook example.yml --skip-tags "packages"  

```

### Tag Reuse

We can apply the same tag to more than one task. By using the "--tags" command line options, all tasks with that tag name will be run.

**For example**: In below example, we use one tag "ntp" for several tasks, such as:

```

---  
# file: roles/common/tasks/main.yml  
  
- name: be sure ntp is installed  
  yum:  
    name: ntp  
    state: present  
  tags: ntp  
  
- name: be sure ntp is configured  
  template:  
    src: ntp.conf.j2  
    dest: /etc/ntp.conf  
  notify:  
  - restart ntpd  
  tags: ntp  
  
- name: be sure ntpd is running and enabled  
  service:  
    name: ntpd  
    state: started  
    enabled: yes  
  tags: ntp 

```

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

### Create Roles with Ansible Galaxy

* The Ansible Galaxy is essentially a large public repository of Ansible roles. Roles ship with READMEs detailing the roles use and variables. 

* Ansible Galaxy contains a large number of roles that are continually evolving and increasing.

* The Galaxy can use Git to add other role sources like GitHub. 

* You can initialize a new galaxy role using the ansible-galaxy init or install a role directly from the Ansible galaxy role store by executing the ansible-galaxy install <name of role> command.

* To create an Ansible role using the Ansible Galaxy, you need to use the ansible-galaxy command and its templates. 

* Roles must be downloaded before they used in the playbooks. They are placed into the default directory that is /etc/ansible/roles.

**Create Collections**

Ansible Galaxy has been a tool for constructing and managing roles with new iterations of the Ansible, and you are bound to see changes or additions. On Ansible version 2.8, you get the unique feature of the collections.

Collections are the distribution format for the Ansible content. They can be used to package and distribute roles, modules, playbooks, and plugins.

Collections follow the following simple structure:

```

collection/   
├── docs/   
├── galaxy.yml   
├── plugins/   
│ ├── modules/   
│ │ └── module1.py   
│ ├── inventory/   
│ └── .../   
├── README.md   
├── roles/   
│ ├── role1/   
│ ├── role2/   
│ └── .../   
├── playbooks/   
│ ├── files/   
│ ├── vars/   
│ ├── templates/   
│ └── tasks/   
└── tests/ 

```

The ansible-galaxy-collection command implements the following commands. Some commands are the same as used with ansible-galaxy, such as:

* **init**: It creates a basic collection Skeleton based on the default template included with Ansible or your own template.

* **build**: It creates a collection artifact that can be uploaded to the galaxy or your own repository.

* **publish**: It publishes a built connection artifact to the galaxy.

* **install**: It installs one or more connections.

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

To execute a single command in a single task using a Shell or command module. Suppose you want to get the date of the remote server. And the remote server is under the hostgroup which name is testservers.

**Step 1**: Login to the Ansible server.

**Step 2**: Below is an example that executes a single command using the Shell module in a remote host.

```

---  
-name: Shell command example   
Hosts: testservers  
tasks:  
-name: check date with the shell command  
shell:  
"date"  
register: datecmd  
tags: datecmd  
-debug: msg= "{{datecmd.stdout}}"

```

In the above example, we are running our playbook against a hostgroup named testservers and executing a simple date command and saving the output of that command into a Register variable named datecmd.

At the last line, we retrieve the registered variable and printing only the date command output stored in the stdout property of datecmd.

### Example 2: Execute multiple commands in a single shell:

The Shell can accept various commands together in a single shell play. Also, you can write your shell script with the Ansible shell module.

In the below example, we grouped some shell commands to execute a controlled and clean tomcat restart.

The playbook is designed to execute the following steps in order, such as:

* Stop the tomcatServer

* Clear the cache

* Truncate the log file

* Start the instance

```

---  
  - name: Shell Examples  
    hosts: testservers  
    tasks:  
    - name: Clear Cache and Restart tomcat  
      become: yes  
      delay: 10  
      async: 10  
      poll: 50  
      shell: |  
        echo -e "\n Change directory to the Tomcat"  
        cd tomcat8/  
        echo -e "\n Present working directory is" `pwd`  
          
        echo -e "\n Stopping the tomcat instance"  
        bin/shutdown.sh  
        echo -e "\n Clearning the tmp and work directory of tomcat"  
        rm -rfv tmp/*  
        rm -rfv work/*  
        echo -e "\nTruncate the log file"  
        > logs/catalina.out  
        echo -e "\nDirectory listing"  
        ls -lrtd logs/catalina.out  
        echo -e "\nStarting the instance"  
        bin/startup.sh      
      args:  
        chdir: "/apps/tomcat/"  
      register: fileout  
      tags: fileout   
    - debug: msg="{{ fileout.stdout_lines }}" 

```

## Ansible Templates

Ansible is used to manage configurations of multiple servers and environments. But these configuration files can vary for each cluster or remote server. But apart from a few parameters, all other settings will be the same.

Creating static files for each of these configurations is not an efficient solution. It will take a lot of time, and every time a new cluster is added, then you have to add more files. If there is an efficient way to manage these dynamic values, it would be beneficial. This is where Ansible template modules come into play.

A template is a file that contains all your configuration parameters, but the dynamic values are given as variables in the Ansible. During the playbook execution, it depends on the conditions such as which cluster you are using, and the variables will be replaced with the relevant values.

You can do more than replacing the variables with the help of the Jinj2 templating engine. You can have loops, conditional statements, write macros, filters for transforming the data, do arithmetic calculations, etc.

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

**For example**: Let's create the playbook 1_debug_example.yml, such as:

```

---  
- name: Debug Example Uptime  
hosts: localhost  
connection: local  
   
tasks:  
- name: Find Uptime  
shell: /usr/bin/uptime  
register: result  
   
- name: Print debug message  
debug:  
var: result  
verbosity: 2  

```

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

**There are many ways to invoke the debugger, such as:**

**Using the debugger Keyword**

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

-hosts: loc  
tasks:  
-name: Ansible apt install packages   
apt:  
name: zip  
state: present  
update_cache: true

```

### Installing new Apt Packages

1.Installing the latest version of a package

If you set the state of the packages to "present", then Ansible will only check if the package is present. So if the new package is available, it will not be able to install.

If you want to install the latest apt packages, then you have to set the state parameter to the latest.

This will ensure the package with the latest version is installed. The below example will update the cache first, then install the latest package of zip, such as:

```

-hosts: loc  
tasks:  
-name: ansible apt install latest version  
apt:  
name: zip  
state: latest  
update_cache: true 

```

2.Ansible install multiple packages

Instead of writing multiple tasks to install packages, you can use with_items and combine those tasks.

In the below example, we are going to install 3 packages: docker-ce, Nginx, and git.

```

-hosts: loc  
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
3.Ansible Apt ad-hoc

You can also use the ad-hoc method to install new packages using the apt module, such as:

```

ansible all -m apt -a "name=nginx state=absent" -i inventory.ini  

```

**Removing Apt Packages**

You can also remove the packages using apt module by setting the state parameter to absent.

The below example will remove the zip package. Since the module is idempotent, it will not go through an error if the package is not present.

```

-hosts: loc  
tasks:  
-name: ansible apt remove package   
apt:  
name: zip  
state: absent 

```

