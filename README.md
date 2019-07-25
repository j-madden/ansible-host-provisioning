
## Ansible - Host provisioning

1.  Review the Ansible playbook intro: [https://docs.ansible.com/ansible/latest/playbooks_intro.html](https://docs.ansible.com/ansible/latest/playbooks_intro.html)
2.  Additional interesting topics:
    1.  Terminal commands: [https://docs.ansible.com/ansible/latest/ansible-playbook.html](https://docs.ansible.com/ansible/latest/ansible-playbook.html) and [https://docs.ansible.com/ansible/latest/ansible.html](https://docs.ansible.com/ansible/latest/ansible.html)
    2.  The concept of idempotence, as discussed here: [https://docs.ansible.com/ansible/latest/playbooks_intro.html#tasks-list](https://docs.ansible.com/ansible/latest/playbooks_intro.html#tasks-list)

The following assingments work based on a Vagrant setup that is provisioned using ansible. This setup can be found in a github repository: [https://github.com/jdijt/VagrantAnsible](https://github.com/jdijt/VagrantAnsible) .  
In this assignment your ansible playbook (defined in playbook.yml) is executed on the "Bastion" node using ansible-playbook when you run "vagrant up".

The files in your repository are mounted under the /vagrant directory. And are thus directly accessible in your Bastion node.

To rerun the provisioning you can log into the bastion node:
```
`<yourmacbook> $ vagrant` `ssh`  `bastion`

`<vagrant-bastion>$` `cd`  `/vagrant`

`<vagrant-bastion>$ ansible-playbook -i inventory playbook.yml`
```
The assignment:

1.  Set up your app using ansible. Put the database and webapp on the "backend" node and your web proxy on the "edge" node
    1.  Its your own choice if you deploy using docker, apt, or a combination of both.
2.  Define ansible roles for your app and use those to deploy it.
