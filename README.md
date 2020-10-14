# Prerequesites 

# Vagrant

- Website: [https://www.vagrantup.com/](https://www.vagrantup.com/) -  Version 2.2.10
- Box: https://app.vagrantup.com/ubuntu/boxes/bionic64
- Virtual Machine: https://www.virtualbox.org/


## Quick Start

Build virtual environment:

    vagrant init ubuntu/bionic64
    vagrant up


Note: - do loop is being set here as there are multiple tasks being set.
      - gist is where the code is stored.
      
- Vagrantfile code:

  config.vm.box = "ubuntu/bionic64"
  config.vm.provision :shell do |shell|
    shell.name = "Provision Script 1"
    shell.privileged = "false"
    shell.args = ["arg1", "arg2", "arg3"]
    shell.path = "https://gist.githubusercontent.com/geoffreypf/6dd705d85dc8adae4eccee571e09542a/raw/88d1666cd22ca0c921205c6c9e819bbfa058a276/provision.sh"
  end
