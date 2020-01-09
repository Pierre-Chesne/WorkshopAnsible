# Workshop Ansible

**Installation d'Ansible pour Azure**<br/>
1. Pour un environnement Ubuntu 16.04 LTS :<br/>
```
sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev python-pip
```
```
sudo pip install ansible[azure]
```
2. Pour un environnement CentOS 7.4 :<br/>
```
sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel epel-release
sudo yum install -y python-pip python-wheel
```
```
sudo pip install ansible[azure]
```
**Test d'Ansible**
```
ansible --vers
```
Retour :
```
ansible 2.9.2
  config file = /etc/ansible/ansible.cfg
  configured module search path = [u'/home/pierrc/.ansible/plugins/modules', u'/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/local/lib/python2.7/dist-packages/ansible
  executable location = /usr/local/bin/ansible
  python version = 2.7.12 (default, Oct  8 2019, 14:14:10) [GCC 5.4.0 20160609]
```

