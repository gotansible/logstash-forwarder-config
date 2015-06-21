# -*- mode: ruby -*-
# vi: set ft=ruby :
VAGRANT_VERSION = 2
Vagrant.configure(VAGRANT_VERSION) do |config|
	config.vm.define "logstash-forwarder-config" do |server|
		server.vm.box = "hashicorp/precise64"
		server.vm.hostname = "logstash-forwarder-config"
		server.vm.provision :ansible do |ansible|
			ansible.playbook = "test.yml"
			ansible.skip_tags = "notify"
		end
	end
end
