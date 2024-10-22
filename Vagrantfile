# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "debian/bookworm64"


  config.vm.define "venus" do |venus|
    venus.vm.network "private_network", ip: "192.168.57.102"
    venus.vm.hostname ="venus.sistema.test"
    venus.vm.provider "virtualbox" do |vb|
    end
  end

  config.vm.define "tierra" do |venus|
    venus.vm.network "private_network", ip: "192.168.57.103"
    venus.vm.hostname ="tierra.sistema.test"
    venus.vm.provider "virtualbox" do |vb|
    end
  end
end
