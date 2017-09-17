# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "bdtbdt/bdtcentos"
  config.vm.hostname = "bdttestpg"
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.network "private_network", ip: "192.168.56.140"

config.vm.provider "virtualbox" do |vb|
   vb.memory = 512
   vb.cpus = 1
   vb.name = "bdttestpg"
end

# ansible settings.
config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/roles/play_pg.yml"
end

end
