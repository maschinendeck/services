

The purpose of this repository is to provide service definitions to:

  - quickly and safely restore a system in the case of a crash
  - save time when extending a system
  - provide documentation for old and new people



For each service there is a role.

The services can be setup via [Ansible](https://www.ansible.com/).
There is a [Vagrant](https://www.vagrantup.com/) definition to test provisioning on a local virtual machine.



https://wiki.maschinendeck.org/wiki/Projekte





## Services


[maschinentuer.fftr](https://wiki.maschinendeck.org/wiki/Schließsystem)
  - Nginx forwards to MDOS and Letsencrypt
  - [Letsencrypt](https://letsencrypt.org/) SSL certificate
  - [MDOS](https://github.com/maschinendeck/mdos) Django app
  - GPIO to Feather M0/RFM69 [door backend](https://github.com/maschinendeck/mdos/tree/master/featherm0-backend) and [door frontend](https://github.com/maschinendeck/mdos/tree/master/featherm0-frontend)
  - use [PlatformIO](http://platformio.org/) to build firmware for frontend and backend



[maschinenpi.fftr](https://wiki.maschinendeck.org/wiki/MaschinenPi)
  - MPD
  - ALSA config
  - Printer drivers


[maschinenstatus.fftr](https://github.com/maschinendeck/Maschinenstatus)
  - Nodes for [info-beamer](https://github.com/dividuum/info-beamer/)


[mate.fftr](https://wiki.maschinendeck.org/wiki/Matepad)
  - [Metepad](https://github.com/chaosdorf/mete)




## For local development


Start the virtual machine:

```
vagrant up
```


SSH into machine:

```
vagrant ssh
```


Run provision:

```
ansible-playbook --private-key=.vagrant/machines/default/virtualbox/private_key -u ubuntu -i .vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory site.yml
```
