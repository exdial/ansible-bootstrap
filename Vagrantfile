# -*- mode: ruby -*-
# vi: set ft=ruby

Vagrant.configure(2) do |config|
  config.vm.box_check_update = false
  config.ssh.insert_key = true

  config.vm.define "xenial", autostart: true do |xenial|
    xenial.vm.box = "ubuntu/xenial64"
    xenial.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = 2
    end
  end

end
