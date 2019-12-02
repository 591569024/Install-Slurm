## Prequisites
1. [VirtualBox](virtualbox.org/wiki/Downloads)
2. [CentOS 7.7](http://repo1.dal.innoscale.net/centos/7.7.1908/isos/x86_64/) (minimal version)

### Create virtual machines in VirtualBox
Set Network Adapter 1 to `NAT`, Adapter 2 to `Internal Network`

### Setting up Internet Connecttion and DHCP
1. Create an Inernal Network with VirtualBox's built-in command. It will mimic DHCP server.

In terminal, type:
```
VBoxManage dhcpserver add --netname intnet --ip 10.0.1.1 --netmask 255.255.255.0 --lowerip 10.0.1.2 --upperip 10.0.1.200 --enable
```

2. Setup the internet connection on each virtual machine

```nmcli d```

Show `enp0s3`, `enp0s8`, `enp0s8` will be connected, `enp0s3` will be disconnected.


