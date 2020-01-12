# The Ad-Hoc command
Les commandes "Ad-Hoc" servent à effectuer des tâches ponctuelles<br/>
``$ ansible [pattern] -m [module] -a "[module options]"``

1. **Rebooter un serveur à distance**<br/>
Exemple :<br/>
``
ansible -i hosts webservers -a "/sbin/reboot" -u pierrc --become
``
2. **Transfert de fichiers**<br/>
Exemple :<br/>
``
ansible -i hosts webservers -m copy -a 'src=/tmp/remote-wsl-loc.txt dest=/tmp'
``
3. **Gestion des "packages"** (installation, mise à jour et désinstallation<br/>
Exemple :<br/>
Installation du "package nginx"<br/>
``
ansible -i hosts webservers -m apt -a 'name=nginx state=present' --become
``
Mettre à jour un "package"<br/>
``
ansible -i hosts webservers -m apt -a 'name=nginx state=latest' --become
``
4. **Gestion des services**<br/>
Exemple :<br/>
Démmarrage de service <br/>
``
ansible -i hosts webservers -m service -a "name=nginx state=started" --become
``
Arrêt de service <br/>
``
ansible -i hosts webservers -m service -a "name=nginx state=stopped" --become
``







