

## Ansible - Host provisioning

1. Install Vagrant 
[https://www.vagrantup.com/downloads.html](https://www.vagrantup.com/downloads.html)

2. Use the Vagrant file to configure your VM & running `vagrant up` to start the Vagrant instance.

ssh into each node that will be building a docker container & run
ie: edge & backend

    sudo apt install docker-ce=18.06.1~ce~3-0~ubuntu jq

3. Use the playbook file structure & roles to manage your playbooks.

### Check if successful
SSH into edge node & curl local ip with extension /countries/netherlands





