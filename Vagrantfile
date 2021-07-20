# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
# Box settings
  config.vm.box = "ubuntu/trusty64"

  #Provider settings
config.vm.provider "virtualbox" do |vb|
vb.memory = "512"
    vb.cpus = "1"

  end

  #Network settings
config.vm.network "forwarded_port", guest: 80, host: 1234
#config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
config.vm.network "private_network", ip: "192.168.33.10"
#config.vm.network "public_network"
config.vm.define "trusty" do |node|
  node.vm.hostname = "trusty.local"
    node.vm.provision "ansible" do |ansible|
      ansible.playbook = "main.yml"
  end
end

  #Folder settings
config.vm.synced_folder ".", "/var/www/html"

  #Provision settings
config.vm.provision "shell", inline: <<-SHELL
apt-get update
  #   apt-get install -y apache2
SHELL
end
