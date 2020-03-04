# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.network "forwarded_port", guest: 1433, host: 21433

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048" # minimum memory size to run mssql-server in linux
    vb.name = "mssql-provision"
    vb.cpus = "2"
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.compatibility_mode = "2.0"
    ansible.playbook = "ansible/playbook.yml"
    ansible.host_vars = {
        "default" => {
            "ansible_python_interpreter" => "/usr/bin/python3"
        }
    }
  end
end
