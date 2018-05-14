# Fogbow-Deploy

## Description 
This repository was made to simplify Fogbow Installation. To install using those Ansible playbooks, we need to install the following dependency:
  - [Ansible: [link](http://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)]
   
## Configuration
Now, we have to edit hosts file, filling the IP where yout want to install each component of fogbow. Example: 
 
>\[fogbow-manager\]\
>\<manager_vm_ip\>\
>\[fogbow-manager:vars\]\
>ansible_ssh_private_key_file=<absolute_path_to_private_key>\

**Repeat the steps above to the others components**
 
## Components Configuration

To deploy those components and make it work properly, you need to update the **confs** directory, which has another 3 directories, be sure that you have updated all the configuration files in each directory.

* root\
&nbsp;  |\
&nbsp;  \\-- confs\
&nbsp;  &nbsp;  &nbsp;  &nbsp;  |\
&nbsp;  &nbsp;  &nbsp;  &nbsp;  |\\-- manager\
&nbsp;  &nbsp;  &nbsp;  &nbsp;  |\\-- rendezvous\
&nbsp;  &nbsp;  &nbsp;  &nbsp;  \\-- reverse-tunnel\

With the configuration done, we are ready to run the Ansible-playbook:

## Running 
To install all the components, run:
**ansible-playbook fogbow-setup-all.yml**
