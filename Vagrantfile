# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  # Ansible Node - Centos 7
  config.vm.define "node" do |node|

    node.vm.hostname = "node.devopsstore.local"
    node.vm.box = "centos/7"
    node.vm.synced_folder ".", "/vagrant", disabled: true
    node.vm.network "public_network", bridge: "wlp2s0", ip: "192.168.1.11"

    node.vm.provider "virtualbox" do |y|
        y.customize [ "modifyvm", :id, "--cpus", "2" ]
        y.customize [ "modifyvm", :id, "--memory", "2048" ]
    end

  end
  # End Puppet Node - Centos 7

end
