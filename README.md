# Multi machine web01 web02 in single Vagrantfile
## Intro
This manual is dedicated to create 2 web servers using vagrant virtualbox base ubuntu lts box with nginx package installed
and ubuntu64 box with mysql installed.
Tested on Mac OS X.

## Requirements
- Oracle Virtualbox recent version installed
[VirtualBox installation manual](https://www.virtualbox.org/manual/ch01.html#intro-installing)

- Hashicorp vagrant recent version installed
[Vagrant installation manual](https://learn.hashicorp.com/tutorials/vagrant/getting-started-install)

- git installed
[Git installation manual](https://git-scm.com/download/mac)

- Web browser installed. Use web browser bundled with your OS.

## Preparation 
- Clone git repository. 

```bash
git clone https://github.com/antonakv/vagrant-ob-multimachine-mysql
```

Expected command output looks like this:

```bash
Cloning into 'vagrant-ob-multimachine-mysql'...
remote: Enumerating objects: 12, done.
remote: Counting objects: 100% (12/12), done.
remote: Compressing objects: 100% (12/12), done.
remote: Total 12 (delta 1), reused 3 (delta 0), pack-reused 0
Receiving objects: 100% (12/12), done.
Resolving deltas: 100% (1/1), done.
```

- Change folder to vagrant-ob-multimachine-mysql

```bash
cd vagrant-ob-multimachine-mysql
```

## Provisioning

- In the same folder you were before run 

```bash
vagrant up
```

Sample result

```bash
$ vagrant up     
Bringing machine 'web01' up with 'virtualbox' provider...
Bringing machine 'web02' up with 'virtualbox' provider...
Bringing machine 'mysql' up with 'virtualbox' provider...
==> web01: Importing base box 'aakulov/nginx64'...
==> web01: Matching MAC address for NAT networking...
==> web01: Checking if box 'aakulov/nginx64' version '21.03.02' is up to date...
==> web01: Setting the name of the VM: vagrant-ob-multimachine-mysql_web01_1615459654752_71229
==> web01: Clearing any previously set network interfaces...
==> web01: Preparing network interfaces based on configuration...
    web01: Adapter 1: nat
    web01: Adapter 2: hostonly
==> web01: Forwarding ports...
    web01: 22 (guest) => 2222 (host) (adapter 1)
==> web01: Booting VM...
==> web01: Waiting for machine to boot. This may take a few minutes...
    web01: SSH address: 127.0.0.1:2222
    web01: SSH username: vagrant
    web01: SSH auth method: private key
    web01: 
    web01: Vagrant insecure key detected. Vagrant will automatically replace
    web01: this with a newly generated keypair for better security.
    web01: 
    web01: Inserting generated public key within guest...
    web01: Removing insecure key from the guest if it's present...

[ Some output is removed]

    mysql: 22 (guest) => 2201 (host) (adapter 1)
==> mysql: Booting VM...
==> mysql: Waiting for machine to boot. This may take a few minutes...
    mysql: SSH address: 127.0.0.1:2201
    mysql: SSH username: vagrant
    mysql: SSH auth method: private key
    mysql: 
    mysql: Vagrant insecure key detected. Vagrant will automatically replace
    mysql: this with a newly generated keypair for better security.
    mysql: 
    mysql: Inserting generated public key within guest...
    mysql: Removing insecure key from the guest if it's present...
    mysql: Key inserted! Disconnecting and reconnecting using new SSH key...
==> mysql: Machine booted and ready!
==> mysql: Checking for guest additions in VM...
==> mysql: Setting hostname...
==> mysql: Configuring and enabling network interfaces...
==> mysql: Mounting shared folders...
    mysql: /vagrant => /Users/aakulov/Documents/Development/Hashicorp/vagrant-ob-multimachine-mysql
```
