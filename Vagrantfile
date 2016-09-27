# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "sbeliakou/centos-6.7-x86_64"
 # config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.network "private_network", ip: "192.168.25.200"
  config.vm.hostname = "zabbix"
  
  config.vm.provider "virtualbox" do |vb|
    vb = config.vm.hostname
  end
  
  config.vm.provision "shell", path: "shell.sh"
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = 'ansible/provision.yml'
    ansible.verbose = 'vv'
  end
end
