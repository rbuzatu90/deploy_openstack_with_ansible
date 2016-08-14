# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  ### Default configs ###

  #config.vm.network "public_network"
  config.vm.provider "virtualbox" do |v, override|
    override.vm.box = "ubuntu/trusty64"
    v.linked_clone = true
  end

  ###  VMs configs ###

  config.vm.define "ansible" do |my_vm|
    my_vm.vm.hostname = 'ansible'
    my_vm.vm.network "private_network", ip: "10.0.0.5" # Management
    config.vm.provider :virtualbox do |vb|
      vb.memory = 1024
      vb.cpus = 2
      vb.name = "ansible"
    end
  end

  config.vm.define "infra1" do |my_vm|
    my_vm.vm.hostname = 'infra1'
    my_vm.vm.network "private_network", ip: "10.0.0.10" # Management
    my_vm.vm.network "private_network", ip: "10.0.1.10" # VXLan
    config.vm.provider :virtualbox do |vb|
      vb.memory = 2048
      vb.cpus = 2
      vb.name = "infra1"
    end
  end

  config.vm.define "net1" do |my_vm|
    my_vm.vm.hostname = 'net1'
    my_vm.vm.network "private_network", ip: "10.0.0.11" # Management
    my_vm.vm.network "private_network", ip: "10.0.1.11" # VXLan
    config.vm.provider :virtualbox do |vb|
      vb.memory = 2048
      vb.cpus = 2
      vb.name = "net1"
    end
  end

  config.vm.define "compute1" do |my_vm|
    my_vm.vm.hostname = 'compute1'
    my_vm.vm.network "private_network", ip: "10.0.0.12" # Management
    my_vm.vm.network "private_network", ip: "10.0.1.12" # VXLan
    config.vm.provider :virtualbox do |vb|
      vb.memory = 2048
      vb.cpus = 2
      vb.name = "compute1"
    end
  end

  config.vm.define "log1" do |my_vm|
    my_vm.vm.hostname = 'log1'
    my_vm.vm.network "private_network", ip: "10.0.0.13" # Management
    my_vm.vm.network "private_network", ip: "10.0.1.13" # VXLan
    config.vm.provider :virtualbox do |vb|
      vb.memory = 2048
      vb.cpus = 2
      vb.name = "log1"
    end
  end




  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
  # end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Define a Vagrant Push strategy for pushing to Atlas. Other push strategies
  # such as FTP and Heroku are also available. See the documentation at
  # https://docs.vagrantup.com/v2/push/atlas.html for more information.
  # config.push.define "atlas" do |push|
  #   push.app = "YOUR_ATLAS_USERNAME/YOUR_APPLICATION_NAME"
  # end

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end
