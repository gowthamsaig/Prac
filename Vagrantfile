# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

#box settings
  config.vm.box = "ubuntu/jammy64"

 #nt settings
config.vm.network "private_network", type: "dhcp"
  # config.vm.box_check_update = false
  # config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"

#folder settings
  # config.vm.synced_folder "../data", "/vagrant_data"

#pprovider settings
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
  # end


#provision settings
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
config.vm.provision "shell", inline: <<-END
apt update
apt install -y apache2
cp -r /vagrant/webcontent/* /var/www/html/
echo "Machine provisioned at $(date)! Welcome!"
end
