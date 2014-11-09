# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "centos6_x64-20141109"


  config.vm.define "vm1" do |vm1|
    vm1.vm.network :private_network, ip: "172.17.8.11"
  end  

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "demo-site.yml"
    ansible.verbose = "v"
    ansible.sudo = "true"
    ansible.sudo_user = "root"
    ansible.host_key_checking = "false"
  end

end
