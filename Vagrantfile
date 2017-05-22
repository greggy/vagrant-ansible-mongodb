# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.define "mongo" do |mongo|
        mongo.vm.box = "ubuntu/trusty64"
        mongo.vm.hostname  = "mongo.loc"
        mongo.vm.network :public_network, ip: "192.168.1.123"

        mongo.vm.provision :ansible do |ansible|
            ansible.playbook = "provisioning/playbook.yml"
        end
  end
end
