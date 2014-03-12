ansible-ubuntu12.04-environment
===============

Code for automated server environment setup

This will help you to quickly setup your server environment:

- Update OS
- Java JDK 7 (1.7.x)
- memcached
- Subversion 1.7
- nginx 1.4.6
- php 5.5
- mysql 5.5
- rabbitmq

# How to use
This README is meant for beginners who haven't work with ansible before

1.Install ansible
~~~
$ sudo apt-get install ansible
~~~
2.Edit the `ansible/hosts` to match your machines you want to install. Refer to this [link](http://docs.ansible.com/intro_inventory.html#host-variables) for more details

3.Edit the `ansible/group_vars/all` to match your desired configurations.

4.Edit the `ansible/install.yml` to match the `hosts`, ssh user (`remote_user`) and the modules to be installed (under `roles`)

5.Make sure all the machines have already your public key so that you can do ssh without entering password

6.Run the command below:
~~~
$ cd ansible
$ ansible-playbook install.yml -i hosts -vvvv -K
~~~
7.Run the command `ansible-playbook --help` for more usefull arguments
