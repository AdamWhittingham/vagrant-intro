# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::configure("2") do |config|
  config.vm.box = 'trusty'
  config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"
  config.vm.hostname = 'example1'

  config.vm.network :forwarded_port, guest: 80, host: 6080
  config.vm.network :private_network, ip: '10.0.0.3'

  host_data_dir = File.join(File.dirname(__FILE__), 'data')
  config.vm.synced_folder host_data_dir, "/var/host", create: true
end
