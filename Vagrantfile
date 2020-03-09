# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "devop-box" do |devbox|
    devbox.vm.box = "debian/stretch64"

    config.vm.network "forwarded_port", guest: 8081, host: 8081

    config.vm.network "private_network", ip: "192.168.33.55"

    ## Provision
    config.vm.provision :ansible do |ansible|
      ansible.playbook = "provisioning/playbook.yml"
    end

    ## Sync folder
    config.vm.synced_folder "../../workspace/pfone_terraform/", "/workspace", type: "nfs"

    config.vm.provider "virtualbox" do |vb|
        vb.customize ["modifyvm", :id, "--memory", "2048"]
        vb.name = "devop-box"
    end

    config.vm.provision "file", source: "~/.vagrant.d/insecure_private_key", destination: "/home/vagrant/.ssh/id_rsa"

  end
end
