# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
 
  config.vm.define "attacker" do |attacker|
  	attacker.vm.box = "kalilinux/rolling"
  	config.vm.network "private_network", ip: "192.168.33.10"
  	config.vm.synced_folder "C:\\Users\\USER\\Desktop\\TIC4301", "/vagrant_data"
  	config.vm.provision "shell", inline: <<-SHELL
  		apt-get update
  		apt-get install -y apache2
  	SHELL
  end

  config.vm.define "victim" do |victim|
  	victim.vm.box = "ubuntu/trusty64"
  	config.vm.network "private_network", ip: "192.168.33.11"
  	config.vm.synced_folder "C:\\Users\\USER\\Desktop\\TIC4301", "/vagrant_data"
  	config.vm.provision "shell", inline: <<-SHELL
  		apt-get update
  		apt-get install -y apache2
  	SHELL
  end

end
