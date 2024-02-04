# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    # VM settings
    # See: https://www.vagrantup.com/docs/vagrantfile/
    config.vm.define "www5.wunderbyte.at" do |node|
        node.vm.box = "debian/bookworm64"

        node.vm.hostname = "www5.wunderbyte.at"

        node.vm.network "forwarded_port", guest: 80, host: 8080
        node.vm.network "forwarded_port", guest: 443, host: 4443
        # node.vm.network "private_network", type: "dhcp", ip: "10.0.2.2", libvirt_network_name: "foo-network"

        node.vm.synced_folder ".", "/srv/moodle/src", type: "nfs", nfs_version: "4"

        node.vm.provider "virtualbox" do |vb|
            vb.name = "wunderbyte moodle test"
            vb.memory = 8192
            vb.cpus = 4
        end
    end

    config.vm.define "www6.wunderbyte.at" do |node|
        node.vm.box = "debian/bookworm64"

        node.vm.hostname = "www6.wunderbyte.at"

        node.vm.network "forwarded_port", guest: 80, host: 8080
        node.vm.network "forwarded_port", guest: 443, host: 4443
        # node.vm.network "private_network", type: "dhcp", ip: "10.0.2.2", libvirt_network_name: "foo-network"

        node.vm.synced_folder ".", "/srv/moodle/src", type: "nfs", nfs_version: "4"

        node.vm.provider "virtualbox" do |vb|
            vb.name = "wunderbyte moodle test 2"
            vb.memory = 8192
            vb.cpus = 4
        end
    end
end
