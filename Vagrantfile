# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  
  config.vm.define "agent" do |agent|
  agent.vm.box = "sbeliakou/centos-6.7-x86_64"
  agent.vm.network "private_network", ip: "192.168.25.201"
  agent.vm.hostname = "zabbix-agent"
  
  agent.vm.provider "virtualbox" do |vb|
    vb = agent.vm.hostname
  end
  
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = 'ansible/provision.yml'
    ansible.verbose = 'vv'
  end
  end
end
