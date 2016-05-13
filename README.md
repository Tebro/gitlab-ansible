# Gitlab


This is a simple project that installs Gitlab using Ansible


## Test locally

The project includes file for a easy local setup using Vagrant and VirtualBox. Just follow the steps below.

#### Start the VM

```
vagrant up
```

#### Install gitlab using ansible

```
chmod 400 key
pip install -r requirements.txt
ansible-playbook -i inventories/vagrant playbooks/provision.yml
```

After the installation completes you can browse to http://10.0.0.20
