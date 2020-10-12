# Prerequesites 

# Vagrant

- Website: [https://www.vagrantup.com/](https://www.vagrantup.com/) -  Version 2.2.10
- Box: https://app.vagrantup.com/ubuntu/boxes/bionic64
- Virtual Machine: https://www.virtualbox.org/


## Quick Start

Build virtual environment:

    vagrant init ubuntu/bionic64
    vagrant up

Note: The above `vagrant up` command will also trigger Vagrant to download the
`bionic64` box via the specified URL. Vagrant only does this if it detects that
the box doesn't already exist on your system.
