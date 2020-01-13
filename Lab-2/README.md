# Structure d’un playbook avec des rôles:

**Exercice**<br/>
Créer un role "delete " (Efface le fichier index de base "index.nginx-debian.html") avec la commande ansible-galaxy<br/>
Exemple, dans le rrépertoir roles:<br/>
``
ansible-galaxy init delete
``<br/>
Effacer le fichier "/var/www/html/index.nginx-debian.html" avec le module "file" (https://docs.ansible.com/ansible/latest/modules/file_module.html)



