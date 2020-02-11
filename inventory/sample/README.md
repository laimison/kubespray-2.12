# Kubespray

## Vagrant

### Build Cluster

```
python -V && pip -V
sudo pip install -r requirements.txt
```

Check `Vagrantfile`

```
vagrant up
```

If vagrant run fails and you've made some changes to fix the issue, re-run it:

```
ansible-playbook -vvv -i .vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory cluster.yml
```

Run retry:

```
ansible-playbook -vvv -i .vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory cluster.yml --limit @/Users/lvalatka/Documents/github/kubespray-2.12/cluster.retry
```
