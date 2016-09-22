# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure('2') do |config|
  config.vm.box      = 'ubuntu/trusty64'
  config.vm.hostname = 'deep-learning-test'

  config.vm.network :forwarded_port, guest: 3001, host: 3001
  config.vm.network :forwarded_port, guest: 8889, host: 8889

  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 4
  end
  
  config.vm.provision :shell, path: 'bootstrap.sh', keep_color: true
  config.vm.synced_folder "notebooks/", "/home/vagrant/notebooks"
end
