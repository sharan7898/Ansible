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


