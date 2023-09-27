
Vagrant.configure("2") do |config|

  config.vm.box = "hashicorp/bionic64"


  config.vm.provider "virtualbox" do |vm|
    vm.name = "maquina-virtual-02"
 end

  config.vm.network "forwarded_port", guest: 80, host: 8090

  config.vm.network "public_network", ip: "192.168.1.212"

  config.vm.provision "shell", path: "script.sh"

  config.vm.synced_folder "site/", "/var/www/html"

end
