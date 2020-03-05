Vagrant.configure("2") do |config|
  config.vm.define "master" do |master|
    master.vm.box = "ubuntu/bionic64"
    master.vm.hostname = 'c1-master1'
    master.vm.box_url = "ubuntu/bionic64"

    master.vm.network :private_network, ip: "172.16.94.10"

    master.vm.provider :virtualbox do |v|
      # v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "c1-master1"]
    end
  end

  config.vm.define "node1" do |node1|
    node1.vm.box = "ubuntu/bionic64"
    node1.vm.hostname = 'c1-node1'
    node1.vm.box_url = "ubuntu/bionic64"

    node1.vm.network :private_network, ip: "172.16.94.11"

    node1.vm.provider :virtualbox do |v|
      # v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "c1-node1"]
    end
  end

  config.vm.define "node2" do |node2|
    node2.vm.box = "ubuntu/bionic64"
    node2.vm.hostname = 'c1-node2'
    node2.vm.box_url = "ubuntu/bionic64"

    node2.vm.network :private_network, ip: "172.16.94.12"

    node2.vm.provider :virtualbox do |v|
      # v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--name", "c1-node2"]
    end
  end

end
