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
|-- inventories / hosts/       =>  just store remote server ip/hostname  and  
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


## Installation 
Make sure, your control node should be ubuntu machine 

- execute the following command 
```git
sudo apt update -y 
sudo apt install ansible
```

- once installed , check  the  ansible version of that machine. 
```git 
ansible --version
```
make sure you have minimum two node , One is for ansible host / control node or others are target host.

## setup password-less authentication 
- 1st enter into ansible host node , generate private and public key 
- open the public key file in notepad and copy the content 
- paste the key in remote machine > .ssh/authorised_key file in last  
- do the ssh to check it 


- check its connect or not 
## Lets do some handsome project  
https://github.com/abhiramdas99/devops-ansible-everything/tree/main/playbooks

    

