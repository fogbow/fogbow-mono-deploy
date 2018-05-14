# Fogbow-Deploy

## Description 
This repository was made to simplify Fogbow Installation. To install using those Ansible playbooks, we need to install the following dependency:
  - [Ansible: [link](http://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)]
   
## Configuration
Now, we have to edit hosts file, filling the IP where yout want to install each component of fogbow. Example: 
 
\[fogbow-manager\]
   
\<Manager VM IP\>
   
\[fogbow-manager:vars\]
   
ansible_ssh_private_key_file=<absolute_path_to_private_key>

**Repeat the steps above to the others components**

## Running 
To install all the components, run:
**ansible-playbook fogbow-setup-all.yml**
