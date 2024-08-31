# -*- mode: ruby -*-
# vi: set ft=ruby :

ENV['VAGRANT_SERVER_URL'] = 'https://vagrant.elab.pro'
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/focal64"
  config.vm.box_check_update = false
  config.vm.hostname = "testing"

  config.vm.network "public_network", ip: "192.168.1.100"
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  config.vm.network "forwarded_port", guest: 9090, host: 9090
  config.vm.define "testing"
  config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.provider "virtualbox" do |vb|
    vb.name = "testvb"
    vb.gui = false

    vb.memory = "1024"
    vb.cpus = "1"

  end

  #
  # Run Ansible from the Vagrant Host
  #

  config.vm.provision "ansible" do |ansible|

    ansible.playbook = "playbook.yml"
    ansible.verbose = true
  end
end

