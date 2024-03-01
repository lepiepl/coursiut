Vagrant.configure("2") do |config|
  config.vm.box = "generic/centos8"
  config.vm.provider "libvirt" do |hv|
    hv.cpus = "1"
    hv.memory = "512"
  end
  config.vm.synced_folder '.', '/vagrant', disabled: true

  config.vm.define "host1" do |host1|
    host1.vm.network :private_network, ip: "192.168.3.10"
    host1.vm.hostname = "host1"
  end
  config.vm.define "host2" do |host2|
    host2.vm.network :private_network, ip: "192.168.3.11"
    host2.vm.hostname = "host2"
  end
end
