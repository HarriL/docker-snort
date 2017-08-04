# docker-snort
A ready to run Snort and PulledPork docker image. 

Forked from: jasonish/docker-snort 2017-08-04

## Installation: to a fresh Centos7.3 (e.g. testing in a virtual machine)

Create public/private keys for authentication. See: https://wiki.centos.org/HowTos/Network/SecuringSSH
> cd ~/.ssh

> ssh-keygen -t rsa

> chmod 700 ~/.ssh

> chmod 600 ~/.ssh/id_rsa

Ensure the correct SELinux contexts are set:

> restorecon -Rv ~/.ssh 

Copy file "id_rsa.pub" to your Git / Settings / SSH and GPG keys and clone from git

> cd ~

> git clone git@github.com:HarriL/docker-snort.git

Install Docker CE (Community Edition): https://docs.docker.com/engine/installation/linux/docker-ce/centos/#install-using-the-repository

> sudo yum install -y yum-utils device-mapper-persistent-data lvm2

> sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

> sudo yum-config-manager --enable docker-ce-test

> sudo yum makecache fast

> sudo yum install docker-ce

Start Docker
> sudo systemctl start docker

Verify Docker installation
> sudo docker run hello-world

