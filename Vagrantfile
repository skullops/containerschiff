# -*- mode: ruby -*-
# vi: set ft=ruby :
MACHINE_HOSTNAME="ansible"

Vagrant.configure("2") do |config|
  config.vm.box = "debian/stretch64"
  config.vm.network :private_network, ip: "192.168.30.2"

  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--name", MACHINE_HOSTNAME]
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    v.customize ["modifyvm", :id, "--memory", 1024]
    v.customize ["modifyvm", :id, "--cpus", 2]
    v.customize ["modifyvm", :id, "--ioapic", "on"]
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "./site.yml"
    ansible.sudo = true
    ansible.extra_vars = { ansible_ssh_user: 'vagrant' }
  end

  config.vm.define MACHINE_HOSTNAME do |machine|
    machine.vm.hostname = MACHINE_HOSTNAME
  end
end
