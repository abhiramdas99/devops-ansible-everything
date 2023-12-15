# devops-ansible-everything

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
````git
ansible_project_xyz/
|-- inventories/               =>  just store remote server ip and 
|   |-- production/            => denote the environment type
|       |-- apache_servers     => point to all apache sever ip 
|       |-- nginx_servers      => point to all nginx server ip 
|
|   |-- staging/
|       |-- apache_servers
|       |-- nginx_server
|
|-- roles/                    => just store the task information that want to perform in remote server 
|  |-- apache/
|      |-- tasks/              => jstore the task like installation, start service , configuration of a partical applicaton 
|          |-- main.yml
|      |-- templates/
|          |-- index.html.j2
|
|   |-- nginx/
|       |-- tasks/
|          |-- main.yml
|       |-- templates/
|          |-- index.html.j2
|
|   |-- java/
|       |-- tasks/
|          |-- main.yml
|
|-- playbooks/
|   |-- setup_servers.yml
|   |-- install_java.yml 
````
## Lets do some  project on ansible 
- Project-01
  - CASE:
```git
You are a Devops Engineer and the organization you are working on needs to set up two configuration
management server groups. One for Apache another for Nginx. Being a Devops Engineer it is your task
to deal with this configuration management issue.
Let us see the tasks that you need to perform using Ansible.
1. Create two Server Groups. One for Apache and another for Nginx.
2. Push two html files with their server information.
Make sure that you don’t forget to start the services once the installation is done. Also send post
installation messages for both the server groups.
Using Ansible Roles accomplish the above the tasks.
Also, once the Apache server configuration is done you need to install Java on that server group using
ansible role in a playbook.
````
  - Solution:
    

