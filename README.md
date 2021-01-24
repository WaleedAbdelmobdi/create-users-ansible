## Role info

> Ansible Playbook to create local users on remote servers


## Tested on the following operating systems

- CentOS 8


## Usage

- Clone the Project:

```
$ git clone https://github.com/WaleedAbdelmobdi/create-users-ansible.git
$ cd create-users-ansible
```

- Update your inventory:

```
$ vim hosts
[node1]
192.168.10.10       # Update IP for Remote user to act on
```

- Update users name to be created

```
$ vim vars.yaml
   users:
  - ledo # set username to be create
  - zezo # set username to be create
                                 
```

- Update variables in playbook file - Set remote user

```
$ vim create-users.yaml
   gather_facts: no
   become: yes               # If to escalate privilege
   become_method: sudo       # Set become method
   remote_user: root       # Update username for remote server
```

If you are using non root remote user, then set username and enable sudo

```
become: yes
become_method: sudo

```


## Running Playbook


Playbook executed as root user - with password:

```
$ ansible-playbook -i hosts create-users.yaml  --ask-pass
```

Playbook executed as sudo user - with password:

```
$ ansible-playbook -i hosts create-users.yaml --ask-pass --ask-become-pass
```

