Ansible - Host provisioning

Review the Ansible playbook intro: https://docs.ansible.com/ansible/latest/playbooks_intro.html
Additional interesting topics:
Terminal commands: https://docs.ansible.com/ansible/latest/ansible-playbook.html and https://docs.ansible.com/ansible/latest/ansible.html
The concept of idempotence, as discussed here: https://docs.ansible.com/ansible/latest/playbooks_intro.html#tasks-list
The following assingments work based on a Vagrant setup that is provisioned using ansible. This setup can be found in a github repository: https://github.com/jdijt/VagrantAnsible .
In this assignment your ansible playbook (defined in playbook.yml) is executed on the "Bastion" node using ansible-playbook when you run "vagrant up".

The files in your repository are mounted under the /vagrant directory. And are thus directly accessible in your Bastion node.

To rerun the provisioning you can log into the bastion node:

<yourmacbook> $ vagrant ssh bastion
<vagrant-bastion>$ cd /vagrant
<vagrant-bastion>$ ansible-playbook -i inventory playbook.yml
The assignment:

Set up your app using ansible. Put the database and webapp on the "backend" node and your web proxy on the "edge" node
Its your own choice if you deploy using docker, apt, or a combination of both.
Define ansible roles for your app and use those to deploy it.
