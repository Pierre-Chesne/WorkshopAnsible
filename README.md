# Workshop Ansible
Pour faire ce "Workshop", il faut installer:<br/>
- Un environnement Linux (https://docs.microsoft.com/fr-fr/windows/wsl/install-win10) <br/>
- Ansible <br/>
- Installer la nouvelle collection "azcollection" (fournit une série de modules et plugins Ansible pour interagir avec Azure)<br/>
- Gérer la méthode d'authentification et les droits pour Azure avec un SPN ("Service Principal Name")
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
**Gérer la méthode d'authentification et les droits pour Azure avec un SPN ("Service Principal Name")**<br/>
Il y a deux possibiltés pour créer un SPN :<br>
- En passant par la commande (Azure Could Shell ou CLI Azure):<br/>
```
az ad sp create-for-rbac --name ServicePrincipalName
```
- Ou en passant par la console:<br/>
https://docs.microsoft.com/fr-fr/azure/active-directory/develop/howto-create-service-principal-portal <br>

Créez un fichier ``~/.azure/credentials``:<br/>
```
mkdir ~/.azure
nano ~/.azure/credentials
```
Copier le code en mettant vos informations (id de votre abonnement; id de l'application et son secret et id de votre tenant )<br/>
```
[default]
subscription_id=<your-subscription_id>
client_id=<security-principal-appid>
secret=<security-principal-password>
tenant=<security-principal-tenant>
```


**Installation de Visual Studio Code**<br/>
``https://code.visualstudio.com/``
