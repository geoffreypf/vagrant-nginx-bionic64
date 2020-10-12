# Prerequesites 

# Vagrant

- Website: [https://www.vagrantup.com/](https://www.vagrantup.com/) -  Version 2.2.10
- Box: https://app.vagrantup.com/ubuntu/boxes/bionic64
- Virtual Machine: https://www.virtualbox.org/


## Quick Start

First, make sure your development machine has
[VirtualBox](https://www.virtualbox.org/)
installed. After this,
[download and install the appropriate Vagrant package for your OS](https://www.vagrantup.com/downloads.html).

To build your first virtual environment:

    vagrant init hashicorp/bionic64
    vagrant up

Note: The above `vagrant up` command will also trigger Vagrant to download the
`bionic64` box via the specified URL. Vagrant only does this if it detects that
the box doesn't already exist on your system.

## Getting Started Guide

To learn how to build a fully functional development environment, follow the
[getting started guide](https://www.vagrantup.com/docs/getting-started).

## Installing from Source

If you want the bleeding edge version of Vagrant, we try to keep master pretty stable
and you're welcome to give it a shot. Please review the installation page [here](https://www.vagrantup.com/docs/installation/source).

## Contributing to Vagrant

Please take time to read the [HashiCorp Community Guidelines](https://www.hashicorp.com/community-guidelines) and the [Vagrant Contributing Guide](https://github.com/hashicorp/vagrant/blob/master/.github/CONTRIBUTING.md).

Then you're good to go!

Build the following infrastructure in vagrant using configuration management (Ansible, Chef or
similar):
The brief:
- All VMs built using the following vagrant box:
https://app.vagrantup.com/ubuntu/boxes/bionic64
- All VMs allow the vagrant user, and users in the admin group, to sudo without a password
- Webservers and load balancer running nginx
- Simple ‘Hello World’ application deployed to both webservers
- Automated tests to show that app is deployed correctly and nginx is load balancing correctly
- Solution is idempotent
