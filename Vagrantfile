# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-20.04"
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 2
  end

  (1..3).each do |n|
    config.vm.define "node-#{n}" do |node|
      node.vm.hostname = "node-#{n}"
      node.vm.network "private_network", ip: "10.10.10.#{10 + n}"
    end
  end
end
