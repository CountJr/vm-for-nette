# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = 'puphpet/ubuntu1604-x64'

  config.ssh.forward_agent = true

  config.vm.network "private_network", ip: "192.168.33.11"

  # config.vm.network "forwarded_port", guest: 3000, host: 3000
  # config.vm.network "forwarded_port", guest: 8080, host: 80


  config.ssh.forward_agent = true

  config.vm.provision 'ansible_local' do |ansible|
    # ansible.galaxy_roles_path = 'tmp/ansible-roles'
    # ansible.galaxy_role_file = 'cm/requirements.yml'
    # ansible.install = true
    # ansible.version = 'latest'
    ansible.playbook = 'cm/vagrant.yml'
    # ansible.playbook = 'cm/nodejs.yml'
    # ansible.inventory_path = 'cm/production'
    ansible.limit = 'all'
    # ansible.tags = ENV['TAGS']
    # ansible.sudo = true
    ansible.verbose = 'vv'
  end

end