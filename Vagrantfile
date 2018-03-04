# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.box_check_update = false

  config.vm.define 'archlinux' do |arch|
    arch.vm.box = 'terrywang/archlinux'
    arch.ssh.insert_key = false
    arch.vm.network "private_network", ip: "192.168.33.200"
    arch.vm.hostname = 'archlinux'
    arch.vm.provider :virtualbox do |vb|
      vb.name = arch.vm.hostname
    end
  end

  config.vm.define 'debian' do |deb|
    deb.vm.box = 'debian/stretch64'
    deb.ssh.insert_key = false
    deb.vm.network "private_network", ip: "192.168.33.201"
    deb.vm.hostname = 'debian'
    deb.vm.provider :virtualbox do |vb|
      vb.name = deb.vm.hostname
    end
  end

  config.vm.define 'fedora' do |fed|
    fed.vm.box = 'generic/fedora27'
    fed.ssh.insert_key = false
    fed.vm.network "private_network", ip: "192.168.33.202"
    fed.vm.hostname = 'fedora'
    fed.vm.provider :virtualbox do |vb|
      vb.name = fed.vm.hostname
    end
  end
end
