# -*- mode: ruby -*-
# vi: set ft=ruby :
load "settings.sh"

Vagrant.configure("2") do |config|
  
  config.vm.box = "ubuntu/bionic64"
	
  config.vm.network "public_network", ip: LAN_IP, netmask: "255.255.255.0", bridge: INTERFACE
  
  config.vm.provider "virtualbox" do |virtualbox|
	  # Enable promiscuous mode
  	  virtualbox.customize ["modifyvm", :id, "--nicpromisc2", "allow-all"]

  end

  config.vm.provision "shell", path: "install.sh"

end

