Vagrant.configure("2") do |config|
  config.vm.box = "generic/debian10"
  config.vm.provider "virtualbox" do |v|
      	v.name = "Box PostgreSQL"
	v.memory = 1024
	v.cpus = 2
  end
  config.vm.synced_folder "./" , "/vagrant"

  config.vm.network "public_network", bridge: "eth2", type: "dhcp"
  config.vm.provision "shell", path: "installPostgres.sh"
end
