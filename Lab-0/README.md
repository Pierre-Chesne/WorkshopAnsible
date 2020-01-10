# The Ad-Hoc command
Les commandes "Ad-Hoc" servent à effectuer des tâches ponctuelles<br/>
``$ ansible [pattern] -m [module] -a "[module options]"``

1. Rebooter un serveur à distance<br/>
Exemple :<br/>
``
ansible -i hosts webservers -a "/sbin/reboot" -u pierrc --become
``
2. Transfert de fichiers<br/>
Exemple :<br/>
``
ansible -i hosts webservers -m copy -a 'src=/tmp/remote-wsl-loc.txt dest=/tmp'
``



