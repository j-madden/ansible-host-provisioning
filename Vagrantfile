Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/trusty64"
    
    config.vm.provision "docker"
    
    config.vm.define "edge" do |machine|
        machine.vm.network "private_network", ip: "172.17.177.21"
    end

    config.vm.define "backend" do |machine|
        machine.vm.network "private_network", ip: "172.17.177.22"
    end
#
#    config.vm.define 'bastion' do |machine|
#        machine.vm.network "private_network", ip: "172.17.177.11"
#    end
    
    config.vm.provision :ansible_local do |ansible|
        ansible.playbook        = "playbook.yml"
        ansible.verbose         = true
        ansible.inventory_path  = "inventory"
        ansible.compatibility_mode = "2.0"
    end
end