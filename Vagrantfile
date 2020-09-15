# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "serverpxe"
  config.vm.define :servidorPXE do |servidorPXE|
	servidorPXE.vm.box = "bento/centos-7.8"
	#servidorPXE.vm.network "public_network", use_dhcp_assigned_default-route: true
	servidorPXE.vm.network :private_network, ip: "172.168.1.11"
	#servidorPXE.vm.provision "shell",path: "script.sh"
	servidorPXE.vm.hostname = "servidorPXE"
  end
  config.vm.provider :virtualbox do |vb|
    vb.customize [ 'modifyvm', :id, '--memory', '3096' ]
	vb.customize [ 'modifyvm', :id, '--cpus',	'4'    ]
  end
end
