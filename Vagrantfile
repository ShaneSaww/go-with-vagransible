Vagrant.configure("2") do |config|
	config.vm.box = "ubuntu/trusty64"
	config.vm.synced_folder "go/", "/home/vagrant/go/", owner: "vagrant"
	config.vm.synced_folder ".", "/vagrant", disabled: true
	config.vm.provision :ansible do |ansible|
		ansible.playbook = "provisioning/installgo.yml"
		ansible.sudo = true
	end
end
