# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define "attacker" do |attacker|
  	attacker.vm.box = "kalilinux/rolling"
  	attacker.vm.network "private_network", ip: "192.168.33.10"
  	attacker.vm.synced_folder "C:\\Users\\USER\\Desktop\\TIC4301", "/vagrant_data"
  end

  config.vm.define "victim" do |victim|
  	victim.vm.box = "ubuntu/impish64"
  	victim.vm.box_version = "20210904.0.0"
  	victim.vm.network "private_network", ip: "192.168.33.11"
  	victim.vm.synced_folder "C:\\Users\\USER\\Desktop\\TIC4301", "/vagrant_data"
  end

end
