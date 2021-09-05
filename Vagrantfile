# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define "attacker" do |attacker|
  	attacker.vm.box = "kalilinux/rolling"
  	attacker.vm.hostname = "attacker"
  	attacker.vm.network "private_network", ip: "192.168.33.10"
  end

  config.vm.define "victim" do |victim|
  	victim.vm.box = "ubuntu/impish64"
  	victim.vm.box_version = "20210904.0.0"
  	victim.vm.hostname = "victim"
  	victim.vm.network "private_network", ip: "192.168.33.11"
  end

end
