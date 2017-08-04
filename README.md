# docker-snort
A ready to run Snort and PulledPork docker image. 

Forked from: jasonish/docker-snort 2017-08-04

## Installation: to a fresh Centos7.3 (e.g. testing in a virtual machine)

Create public/private keys for authentication
> cd ~/.ssh

> ssh-keygen -t rsa

> chmod 700 ~/.ssh

> chmod 600 ~/.ssh/id_rsa

Ensure the correct SELinux contexts are set:

> restorecon -Rv ~/.ssh 

Copy file "id_rsa.pub" to your Git / Settings / SSH and GPG keys and clone from git

> cd ~

> git clone git@github.com:HarriL/docker-snort.git

