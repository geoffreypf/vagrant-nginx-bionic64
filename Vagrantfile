# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
 
  # Box settings
  config.vm.box = "ubuntu/bionic64"

  # Provider settings
  config.vm.provider "virtualbox" do |vb|

  end

  # Network settings 
  # 8080 being mac
  config.vm.network "forwarded_port", guest: 80, host: 8080 
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1" 
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"

  # Folder settings
  config.vm.synced_folder ".", "/var/www/html", :mount_options => ["dmode=777", "fmode=666"]

  # Provision settings
   config.vm.provision "shell", inline: <<-SHELL
     apt-get update
     apt-get install -y apache2
     apt-get -y install nginx
  SHELL
end
