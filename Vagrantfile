# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"
vagrant_root = File.dirname(__FILE__)

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 2
  end

  config.vm.box = "ubuntu/vivid64"

  config.vm.network "public_network"
  config.vm.provision "shell", path: "scripts/mc-jre-install"

end
