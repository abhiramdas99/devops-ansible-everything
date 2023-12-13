![image](https://github.com/abhiramdas99/devops-ansible-everything/assets/62290469/496d88ee-f0b1-4ad7-a153-be310f8d41c9)# devops-ansible-everything

## What is ansible in short ? 
Ansible is a open source IT automation tool that use to automates provisioning, application deployment and orchestration many IT process.

## Scenario 
Suppose we have 100 server and want to install nginx or apache in all system at same time . We  use to ansible to perform this task

## How ansible work ?
- The server that has Ansible installed is called the control node, while the remote machine where we want to install the application is called the managed node.
- There are two approach to execute the command by ansible tool
  1) Ad-hoc commands (command-line) : just think ansible as linux machine and  the ad-hoc commands are as shell command that  run in linux system
  2) Playbooks : just think as the shell scripts the run in linux system.   

## Standard Project Structure ?
```git
ansible_project_xyz/
|-- inventories/
|  |-- production/
|    |-- apache_servers
|    |-- nginx_servers
|
|-- roles/
|
|-- playbooks/
|  |-- setup_servers.yml
|  |-- install_java.yml 
```
