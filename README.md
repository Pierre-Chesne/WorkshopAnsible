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
2. Pour un environnement CentOS 7.4 :<br/>
```
sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel epel-release
sudo yum install -y python-pip python-wheel
```
```
sudo pip install ansible[azure]
```
3. Test d'Ansible
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
**Installation Azure CLI**<br/>
1. Pour un environnement Ubuntu 18.04 LTS :<br/>

```
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
```
2. Pour un environnement CentOS 7.4
- Importez la clé de référentiel Microsoft <br/>
```
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
```
- Créez des informations de référentiel azure-cli locales.
```
sudo sh -c 'echo -e "[azure-cli]
name=Azure CLI
baseurl=https://packages.microsoft.com/yumrepos/azure-cli
enabled=1
gpgcheck=1
gpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
```
- Installez avec la commande yum install.
```
sudo yum install azure-cli
```
**Installation de Visual Studio Code**<br/>
``https://code.visualstudio.com/``
