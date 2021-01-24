## Role info

> Ansible Playbook to create local users on remote servers


## Tested on the following operating systems

- CentOS 8

## Tasks in the role


## Usage

- Clone the Project:

```
$ git clone https://github.com/jmutai/tomcat-ansible.git
$ cd tomcat-ansible
```

- Update your inventory, e.g:

```
$ vim hosts
[nodes]
192.168.10.10       # Remote user to act on
```

- Update users name 

```
$ vim vars.yaml


## Running Playbook


Playbook executed as root user - with password:

```
$ ansible-playbook -i hosts tomcat-setup.yml --ask-pass
```

Playbook executed as sudo user - with password:

```
$ ansible-playbook -i hosts tomcat-setup.yml --ask-pass --ask-become-pass


