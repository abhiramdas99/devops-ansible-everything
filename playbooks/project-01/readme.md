## To achieve the tasks, you can follow the following steps 
- First organize your ansible project structure
- execute the playbook 
```git 
# To setup  apache and nginx server groups 
ansible -i inventories/production/apache_servers -i inventories/production/nginx_servers playbooks/setup_servers.yml

```

