Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/bionic64"
    config.vm.network "private_network", ip: "192.168.56.10"
    config.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end
    config.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y apache2
      ufw allow 'Apache Full'
    SHELL
  end
  