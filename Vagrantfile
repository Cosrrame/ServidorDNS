# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "debian/bookworm64"


  config.vm.define "venus" do |venus|
  config.vm.box = "debian/bookworm64"
    venus.vm.network "private_network", ip: "192.168.57.102"
    venus.vm.hostname ="venus.sistema.test"
    config.vm.provision "shell", inline:<<-SHELL
      apt-get update
      apt-get install -y bind9
      systemctl restart bind9
    SHELL
  end

  config.vm.define "tierra" do |tierra|
  config.vm.box = "debian/bookworm64"
    tierra.vm.network "private_network", ip: "192.168.57.103"
    tierra.vm.hostname ="tierra.sistema.test"
    config.vm.provision "shell", name: "update", inline:<<-SHELL
    apt-get update
    apt-get install -y bind9
    systemctl restart bind9
  SHELL
  end
end
