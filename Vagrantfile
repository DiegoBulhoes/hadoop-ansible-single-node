Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
      v.memory = 1024
      v.cpus = 1
  end
    
  config.vm.define "hadoop-vm" do |vm|
      vm.vm.box = "ubuntu/bionic64"
      vm.vm.network "private_network", ip: "192.168.50.10"
      vm.vm.hostname = "hadoop-vm"
      vm.vm.provision "ansible" do |ansible|
        ansible.playbook = "ansible/playbook-hadoop-sigle-node.yml"
      end
  end
end