# Structure d’un playbook avec des rôles:

https://docs.ansible.com/ansible/latest/user_guide/playbooks_best_practices.html<br/>
Recommandation pour ce Lab, installer la commande "tree"<br/>
exemple:`` apt-get install tree ``<br/> 
A partir du repertoire ./WorshopAnsible/Lab-2 "executer la commande tree"<br/>


**Exercice**<br/>
Créer un role "delete " (Efface le fichier index de base "index.nginx-debian.html") avec la commande ansible-galaxy<br/>
Exemple, dans le répertoire "roles":<br/>
``
ansible-galaxy init delete
``<br/>
Effacer le fichier "/var/www/html/index.nginx-debian.html" avec le module "file" (https://docs.ansible.com/ansible/latest/modules/file_module.html)

Executer le "playbook" :<br/>
``
ansible-playbook -i hosts main.yml
``<br/>


