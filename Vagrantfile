# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "generic/ubuntu2004"
  config.vm.define "prometheus-demo"

  # config.vm.provision "shell", inline: "apt update && apt install -y python3-passlib"
  config.vm.provision "ansible_local" do |ansible|
    ansible.galaxy_role_file = "collections/ansible_collections/acme/demo_prometheus/requirements.yml"
    ansible.inventory_path = "hosts.yml"
    ansible.playbook = "playbooks/demo_prometheus.yml"
    ansible.provisioning_path = "/vagrant/acme-ansible/"
    # ansible.verbose = true
    ansible.version = "latest"
  config.vm.provision "shell", inline: "echo VM ip: $(ip -o address show | tr -s ' ' | grep 'eth0 inet ' | cut -d ' ' -f 4 | cut -d '/' -f 1). VM configuration complete!"
  end
  
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  config.vm.synced_folder ".", "/vagrant"
end