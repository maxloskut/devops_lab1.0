Vagrant.configure("2") do |config|
  config.vm.define "vm5" do |vm5|
    vm5.vm.hostname = "vm5"
    vm5.vm.box = "centos/7"
    vm5.vm.network "private_network", ip: "192.168.33.10"
    vm5.vm.network "forwarded_port", guest: 80, host: 8888


    vm5.vm.provider "virtualbox" do |vb|
      vb.name = "vm5"
      vb.gui = false
      vb.memory = "1024"
    end
    
    vm5.vm.provision "shell", run: "always",  inline: <<-SHELL
        echo "Hello from the Centos VM"
	mkdir /var/folder1
        mkdir /var/folder2
        cat /vagrant/mv.service > /etc/systemd/system/mv.service
        systemctl daemon-reload
        systemctl start mv.service
        systemctl enable mv.service
        
    SHELL
  end
  
  
end
