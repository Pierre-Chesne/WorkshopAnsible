# Workshop Ansible
Pour faire ce "Workshop", il faut installer:<br/>
- Un environnement Linux (https://docs.microsoft.com/fr-fr/windows/wsl/install-win10) <br/>
- Ansible <br/>
- Installer la nouvelle collection "azcollection" (fournit une série de modules et plugins Ansible pour interagir avec Azure)<br/>

- Visual Studio Code </br>
- Extension Visual Studio Code <br/>
  - Ansible (https://marketplace.visualstudio.com/items?itemName=vscoss.vscode-ansible)<br/>
  - YAML (https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)<br/>

**Installation d'Ansible pour Azure (le "Workshop" se fera avec une distribution Ubuntu 18.04 LTS)**<br/>
1. Pour un environnement Ubuntu 18.04 LTS :<br/>
```
sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev python-pip
```
```
sudo pip install ansible[azure]
```

2. Test d'Ansible
```
ansible --vers
```
Retour :
```
ansible 2.9.9
  config file = /etc/ansible/ansible.cfg
  configured module search path = [u'/home/pierrc/.ansible/plugins/modules', u'/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/local/lib/python2.7/dist-packages/ansible
  executable location = /usr/local/bin/ansible
  python version = 2.7.12 (default, Oct  8 2019, 14:14:10) [GCC 5.4.0 20160609]
```
**Installation de la collection "azcollection"**<br/>
```
ansible-galaxy collection install azure.azcollection
```
**Installation de Visual Studio Code**<br/>
``https://code.visualstudio.com/``
