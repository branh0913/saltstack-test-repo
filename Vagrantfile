# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.synced_folder "salt", "/srv/salt"

  config.vm.provision :salt do |salt|

    salt.masterless = true
    salt.minion_config = "salt/minion_config/minion1"
    salt.run_highstate = true
  end
end
