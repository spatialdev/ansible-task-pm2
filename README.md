# ansible-task-pm2
Ansible task for setting up PM2

Include this task in your ansible playbook to install PM2 and configure start-up script.

Synopsis of sub-tasks

1) Install PM2 globally

2) Copy PM2 JSON application configuration file from Ansible Management Node to target host(s). An example of a PM2 config file is [here](http://pm2.keymetrics.io/docs/usage/application-declaration/). Optional, if **pm2_config_apps: True**. 

### Optional Variables
**pm2_config_apps** (Boolean) - whether to configure PM2 to manage specific apps. default  
**pm2_json_src_path** (string) - the path to PM2 json application config file on the Ansible Managment Node  
**pm2_json_dest_path** (string) - the path to which the PM2 json application config file should be copied to on target host  
**pm2_username** (string) - username for that will execute PM2
