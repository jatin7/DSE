Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  # Add 4GB RAM
  config.vm.provider :virtualbox do |vb|
    vb.customize [
      "modifyvm", :id,
      "--name", "dse",
      "--memory", "4096"
    ]
    vb.cpus = 2
  end

  config.vm.hostname = "dse"
  config.vm.network "private_network", ip: "192.168.4.111"
  config.vm.network "forwarded_port", guest: 9042, host: 9042
  config.vm.network "forwarded_port", guest: 8888, host: 8888

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "dse.yml"
  end

end
