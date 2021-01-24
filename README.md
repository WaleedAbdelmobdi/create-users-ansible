## Role info

> Ansible Playbook to create local users on remote servers


## Tested on the following operating systems

- CentOS 8

## Tasks in the role


## Usage

- Clone the Project:

```
$ git https://github.com/WaleedAbdelmobdi/create-users-ansible.git
$ cd create-users-ansible
```

- Update your inventory:

```
$ vim hosts
[nodes]
192.168.10.10       # Remote user to act on
```

- Update users name 

```
$ vim vars.yaml
---


## Running Playbook


Playbook executed as root user - with password:

```
$ ansible-playbook -i hosts create-users.yaml  --ask-pass
```

Playbook executed as sudo user - with password:

```
$ ansible-playbook -i hosts create-users.yaml --ask-pass --ask-become-pass
---

