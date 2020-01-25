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
3. **Mis à jour**<br/>
Eemple :<br/>
``
ansible -i hosts webservers -m apt -a "upgrade=yes update_cache=yes cache_valid_time=86400" --become
``
4. **Gestion des "packages"** (installation, mise à jour et désinstallation)<br/>
Exemple :<br/>
Installation du "package nginx"<br/>
``
ansible -i hosts webservers -m apt -a 'name=nginx update_cache=yes' --become
``<br/>
Mettre à jour un "package"<br/>
``
ansible -i hosts webservers -m apt -a 'name=nginx state=latest' --become
``
5. **Gestion des services**<br/>
Exemple :<br/>
Démarrage de service<br/>
``
ansible -i hosts webservers -m service -a "name=nginx state=started" --become
``<br/>
Arrêt de service<br/>
``
ansible -i hosts webservers -m service -a "name=nginx state=stopped" --become
``<br/>
Re-Démarrage de service<br/>
``
ansible -i hosts webservers -m service -a "name=nginx state=restarted" --become
``
6. **Gathering facts**<br/>
Récupérer les informations d'un host<br/>
``
ansible -i hosts webservers -m setup
``
7. **Test de connexion**<br/>
Tester la connexion entre la machine Ansible et le(s) Host(s)<br/>
``
ansible -i hosts all -m ping
``<br/>
ou<br/>
``
ansible -i hosts webservers -m ping
``








