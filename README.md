### Ansible Playbook Example for deploing PowerDNS Actoritative and Recursor servers with MySQL backend (Master/Slave replication) and PowerDNS-Admin web GUI (Flask, Gunicorn, Nginx, SSL)
Using:
* Install complementary roles:
```bash
ansible-galaxy install -r install_roles.yml
```
* Configure password in _group_vars/all.yml_ (you can encrypt this file with ansible-vault)
* Replace _mysql_replication_master_ in _dns_admin.yml_ for real ip of your master server
* Deploy
```bash
ansible-playbook dns_admin.yml
```
* Open PowerDNS-Admin - _https://servers_ip/_. Default login and password: admin / admin
