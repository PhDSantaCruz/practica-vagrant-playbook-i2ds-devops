# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "hashicorp/bionic64"
  config.vm.hostname = "Ansible"
  config.vm.network "private_network", ip: "192.168.50.4"
  #config.vm.provision "shell", path: "adduser.sh"
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.provision "shell", path: "adduser.sh"

  config.ssh.insert_key = false

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "playbook.yml"
  end




end
