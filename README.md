"# ansible-setup" 

1. Create and store Your public-private keypair and authorized_keys file in "ssh_keys"  directory. If one managed node - auto generated keys from that node.
2. Check fabfile.py in the "prod" subdirectory and change env.hosts IP, user data and ssh_keys directory if needed.
3. OC starts of the Ansible playbook ./prod/deploy.yml using script ./deploy_prod.sh using role common and all configuraton files from ./prod/roles/common/ directory
Configured both web servers: http and https
4. Add domain FQDN in .prod/group_vars/all
5. Add your SECRET_KEY in application dependencies in file ./prod/group_vars/all and app_admin_user and password
