# -*- mode: ruby -*-
# vi: set ft=ruby :

# Command
#  vagrant box add my-dev11 debian-11.6.0-amd64-virtualbox.box
#  vagrant box list
#  vagrant up
#  vagrant ssh

Vagrant.configure("2") do |config|

  config.vm.box = "my-dev11"
  config.ssh.username = "packer"
  config.ssh.password = "packer"
  config.vm.box_check_update = false

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y nginx
  SHELL
end
