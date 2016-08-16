Welcome!
========

How to deploy OpenStack using Ansible playbooks 

Requirements:
===================

1. VirtualBox
For virtual machines where components will be deployd

2. Vagrant
For fast, easy and reproducible environment

How it works:
=============

Using Vagrantfile VirtualBox will spawn the VMs with
the coresponding settings.
One VM will be used as an Ansible host from where the playbooks will be run.
One VM for "controller" services like nova-conductor, nova-scheduler, rabbitmq, etc.
One VM for networking, aka neutron.
One VM as a compute host aka nova-compute.

