# -*- mode: ruby -*-
# vi: set ft=ruby

Vagrant.configure(2) do |config|
  config.vm.box_check_update = false
  config.ssh.insert_key = true

  # https://github.com/fgrehm/vagrant-cachier
  if Vagrant.has_plugin?('vagrant-cachier')
    config.cache.scope = :box
    config.cache.auto_detect = false
    config.cache.enable :apt
    config.cache.enable :apt_lists
    config.cache.enable :apt_cacher
    config.cache.enable :gem
  else
    puts "-> Run `vagrant plugin install vagrant-cachier` to make provisioning faster"
  end

  config.vm.define "xenial", autostart: true do |xenial|
    xenial.vm.box = "ubuntu/xenial64"
    xenial.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = 2
    end
  end

end
