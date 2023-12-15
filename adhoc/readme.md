# Ansible Adhoc 
```git
Like linux command we can directly run the command in command prompt or terminal. Followng are some example of these command - 
```
## create directly some file in  remote servers 
```git
ansible -i inventory all -m "shell" -a "touch devops-class"
```
- -i inventory: Specifies the inventory file, which contains a list of hosts that Ansible will manage.
all: Targets all hosts defined in the inventory file.

- -m "shell": Specifies the Ansible module to use, in this case, the shell module, which allows running shell commands on remote hosts.

- -a "touch devops-class": Specifies the argument for the shell module, which is the command to run on the remote hosts. In this case, it's the touch devops-class command.
