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

