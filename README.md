# Setting up graylog on CentOS machine

These Ansible playbooks will install Graylog on a CentOS 7 machine.

## Instructions

Public SSH key should be added to /root/.ssh/authorized_keys on the target machine(s). Set the address(es) of machine(s) in the hosts file. Then execute:

ansible-playbook -i hosts main.yml

basic-setup.yml is not necessary, but this is something I need on every server.

## Server Requirements

Clean installation of CentOS takes 942 megabytes. After everything is installed, the used space is 2.0 GB.
Everything up to Elastic Search can be installed on 256 MB of RAM, although ES takes much of that RAM. However, for Graylog, at least 1.5 GB of RAM is necessary just to get it going. Much more will be needed for actual usage.
