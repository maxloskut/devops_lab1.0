# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.define "vm1" do |centos|
    centos.vm.box = "centos/7"
    centos.vm.hostname = "vm1"
    centos.vm.network :private_network, ip: "192.168.56.152" 
    centos.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
    end
  end

  config.vm.define "vm2" do |ubuntu|
    ubuntu.vm.box = "ubuntu/focal64"
    ubuntu.vm.hostname = "vm2"
    ubuntu.vm.network :private_network, ip: "192.168.56.153"
    ubuntu.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
    end
  end

end
