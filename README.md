# Example OpenStack modules playbooks

These playbooks show how to initialize an OpenStack tenant with Ansible. It doesn't create tenant and users, we get those from somewhere else.

THe playbooks run on localhost. You should have openrc.sh sourced before you run the playbooks, because they attempt to use the OS\_\* env variables for authentication, just like python-{nova,glance,...}client.

First you need to read and edit vars.yml

Then, run as

```
# create network, subnet and ..
$ ansible-playbook -i networking.yml

# upload images
$ ansible-playbook -i images.yml

# upload keypair
$ ansible-playbook -i keypair.yml

# launch two instances,
$ ansible-playbook -i instances.yml

```
