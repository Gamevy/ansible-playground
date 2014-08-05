# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "debian7"
  config.vm.box_url = "http://52c6818de4d94384984f-9c74e18f2484dedf74ee8809937722fe.r66.cf5.rackcdn.com/debian7.box"

  config.vm.network :forwarded_port, :host => 8080, :guest => 8080

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
