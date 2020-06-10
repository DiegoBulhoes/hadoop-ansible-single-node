Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
      v.memory = 2024
      v.cpus = 2
  end
    
  config.vm.define "hadoop-master" do |master|
      master.vm.box = "ubuntu/bionic64"
      master.vm.network "private_network", ip: "192.168.50.10"
      master.vm.hostname = "hadoop-master"
      master.vm.provision "ansible" do |ansible|
        ansible.playbook = "ansible/hadoop/defaults/main.yml"
      end
  end
end