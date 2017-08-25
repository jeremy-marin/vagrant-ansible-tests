# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
	config.vm.box = "bento/debian-8.9"
	config.vm.box_version = "201708.22.0"

	config.vm.network :forwarded_port, guest: 80, host: 45678
	config.vm.network :private_network, ip: "192.168.60.71"

	config.vm.provision "ansible" do |ansible|
		ansible.playbook = "playbook.yml"
	end
end
