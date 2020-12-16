## Development box

### Install dependencies 
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
* [Ansible Widows Install/Upgrade](https://geekflare.com/de/ansible-installation-windows/) if already installed re-run install script and follow instructions

### Check the dependencies you need
You can comment in or out (with  # symbol) the dependencies you will need on your virtual box by commenting provisioning/playbook.yml

### Vagrant operations

#### Start the vagrant box

```
vagrant up
```
#### Shutdown the vagrant box

```
vagrant down
```

#### SSH into the vagrant box

```
vagrant ssh
```

#### Snapshot operations

```
vagrant snapshot list # Lists all snapshots
vagrant snapshot save SNAPSHOT_NAME # Saves a snapshot
vagrant snapshot restore SNAPSHOT_NAME # Restores a snapshot
vagrant snapshot delete SNAPSHOT_NAME # Deletes a snapshot
```

--- 
## Useful recommendations

* [Hyper](https://hyper.is/)  terminal windows users