# Data-Essential - ansible - DataStax Cassandra v3.0 - setup (3 nodes with ops center)
Simple Ansible Template to Install an apache cassandra (3.0) 3 nodes cluster on centos7 (or rhel7)

## Requirements
The prerequisits are simples:
* have 3 centos7 servers ready to go with network already configure
* have ansible properly install on your workstation (with the ssh key setup on your 3 servers)

* [DE - blogpost ](https://www.data-essential.com/category/blog/)

## Technology used

* [Centos7](https://www.centos.org/download/), [RHEL7](https://access.redhat.com/downloads)
* [Ansible](http://docs.ansible.com/ansible/)
* [VirtualBox](https://www.virtualbox.org/)
* [Vagrant](https://www.vagrantup.com/docs/getting-started/)

* [Apache cassandra](http://cassandra.apache.org/)
* [DataStax Enterprise](http://www.datastax.com/)

## Running

* Clone the repository.
* Change directory into the cloned project.
* Modify the host names in hosts file.

### Cassandra cluster
Run the following command.

```sh
$ PLAYBOOK=cassandra.yml

$ ansible-playbook -i hosts ${PLAYBOOK}.yml --list-hosts
```
If all your servers respond you are ready to go and re-do the command without the --list-hosts parameter.

Enjoy ;)

### OPS center
Complete this 3 nodes cluster with the datastax ops center

```sh
$ PLAYBOOK=opscenter.yml
$ ansible-playbook -i hosts ${PLAYBOOK}.yml --list-hosts
```

## information

More information can be found on our blog
* [DE - blogpost ](https://www.data-essential.com/category/blog/)
