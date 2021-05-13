## 
Vagrant.configure("2") do |masterConfig|
  #VM1: master
  masterConfig.vm.define "master" do |master|
    master.vm.box = "centos/8"
    master.vm.hostname = "master"
    master.vm.network "private_network", ip: "192.168.20.10"
    master.ssh.insert_key = false
    master.vm.provider "virtualbox" do |vMaster|
      vMaster.name = "ansible_master"
      vMaster.customize ["modifyvm", :id, "--memory", 2048]
      vMaster.customize ["modifyvm", :id, "--cpus", 1]
    end
    master.vm.provision "shell", inline: <<-SHELL
      dnf update
      dnf groupinstall -y 'Minimal Install'
      dnf install -y epel-release
      dnf install -y podman skopeo buildah vim
      echo "192.168.20.10 master master" >> /etc/hosts
      echo "192.168.20.12 node1 node1" >> /etc/hosts
      echo "192.168.20.14 node2 node2" >> /etc/hosts
      echo "192.168.20.16 node3 node3" >> /etc/hosts
    SHELL
  end
end

Vagrant.configure("2") do |node1Config|
  #VM2: Node1
  node1Config.vm.define "node1" do |node1|
    node1.vm.box = "centos/8"
    node1.vm.hostname = "node1"
    node1.vm.network :private_network, ip: "192.168.20.12"
    node1.ssh.insert_key = false
    node1.vm.provider "virtualbox" do |vNode1|
      vNode1.name = "ansible_node1"
      vNode1.customize ["modifyvm", :id, "--memory", 1024]
      vNode1.customize ["modifyvm", :id, "--cpus", 1]
    end
    node1.vm.provision "shell", inline: <<-SHELL
      dnf install -y epel-release
      echo "192.168.20.10 master master" >> /etc/hosts
      echo "192.168.20.12 node1 node1" >> /etc/hosts
      echo "192.168.20.14 node2 node2" >> /etc/hosts
      echo "192.168.20.16 node3 node3" >> /etc/hosts
    SHELL
  end
end

Vagrant.configure("2") do |node2Config|
  #VM3: Node2
  node2Config.vm.define "node2" do |node2|
    node2.vm.box = "centos/8"
    node2.vm.hostname = "node2"
    node2.vm.network :private_network, ip: "192.168.20.14"
    node2.ssh.insert_key = false
    node2.vm.provider "virtualbox" do |vNode2|
      vNode2.name = "ansible_node2"
      vNode2.customize ["modifyvm", :id, "--memory", 1024]
      vNode2.customize ["modifyvm", :id, "--cpus", 1]
    end
    node2.vm.provision "shell", inline: <<-SHELL
      dnf install -y epel-release
      dnf install -y podman skopeo buildah
      echo "192.168.20.10 master master" >> /etc/hosts
      echo "192.168.20.12 node1 node1" >> /etc/hosts
      echo "192.168.20.14 node2 node2" >> /etc/hosts
      echo "192.168.20.16 node3 node3" >> /etc/hosts
    SHELL
  end
end

Vagrant.configure("2") do |node3Config|
  #VM4: Node3
  node3Config.vm.define "node3" do |node3|
    node3.vm.box = "centos/8"
    node3.vm.hostname = "node3"
    node3.vm.network :private_network, ip: "192.168.20.16"
    node3.ssh.insert_key = false
    node3.vm.provider "virtualbox" do |vNode3|
      vNode3.name = "ansible_node3"
      vNode3.customize ["modifyvm", :id, "--memory", 1024]
      vNode3.customize ["modifyvm", :id, "--cpus", 1]
    end
    node3.vm.provision "shell", inline: <<-SHELL
      dnf install -y epel-release
      dnf install -y podman skopeo buildah
      echo "192.168.20.10 master master" >> /etc/hosts
      echo "192.168.20.12 node1 node1" >> /etc/hosts
      echo "192.168.20.14 node2 node2" >> /etc/hosts
      echo "192.168.20.16 node3 node3" >> /etc/hosts
    SHELL
  end
end
