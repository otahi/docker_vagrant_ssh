# -*- mode: ruby -*-

VAGRANTFILE_API_VERSION = "2"


$script = <<SCRIPT
apt-get update
apt-get install -y docker.io
apt-get clean
docker.io build /vagrant/
docker.io run -P -d --name src_node
docker.io run -P -d --name dst_node
SCRIPT

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'ubuntu14.04'

  config.vm.provider "virtualbox" do |_v|
    config.vm.box_url =
      'http://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box'
  end

  config.vm.provision "shell", inline: $script
end
