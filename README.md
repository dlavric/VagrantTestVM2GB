# This repository will guide you on how to create a Virtual box with a dual core and 2GB of RAM


## Pre-Requirements

1. Install the latest version of [Vagrant](https://www.vagrantup.com/docs/installation)

2. Install [VirtualBox](https://www.virtualbox.org/)

## Clone this Repository

```
# git clone https://github.com/dlavric/VagrantTestVM2GB
# cd VagrantTestVM2GB
```

## Whats included?

A `Vagrantfile` that includes a virtual box with a dual core of 2 GB

'Vagrantfile' from this repository:
```ruby
vagrant.configure("2") do |config|
 config.vm.box = "hashicorp/bionic64"
 
config.vm.provider "virtualbox" do |v|
v.memory = 2048
v.cpus = 2

end
end
```

## Start the VMs

```
# vagrant up
```

## Access the VM

```
# vagrant ssh
```

