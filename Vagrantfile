# -*- mode: ruby -*-
# vim: set ft=ruby :

MACHINES = {
    :systemd => {
        :box_name => "centos/7",
        :box_version => "2004.01",
    },
}

Vagrant.configure("2") do |config|
    MACHINES.each do |boxname, boxconfig|
        config.vm.define boxname do |box|
            box.vm.box = boxconfig[:box_name]
            box.vm.box_version = boxconfig[:box_version]
            box.vm.host_name = "systemd"
            box.vm.provider :virtualbox do |vb|
                vb.customize ["modifyvm", :id, "--memory", "1024"]
                needsController = false
            end
        end
        config.vm.provision "ansible" do |ansible|
            #ansible.verbose = "vvv"
            ansible.playbook = "Ansible/playbook.yml"
            ansible.become = "true"
        end
    end
end
