# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "my-bahmni-box"
  config.vm.box_url = "file:///C:/Projects/bahmni/bahmni-vagrant/package.box"

  config.vm.box_check_update = true
  config.ssh.insert_key = false
  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.synced_folder "C:/Projects/bahmni/", "/bahmni", :owner => "vagrant"
  config.vm.provider "virtualbox" do |v|
     v.customize ["modifyvm", :id, "--memory", 3092, "--cpus", 2, "--name", "Bahmni-RPM"]
  end
end
