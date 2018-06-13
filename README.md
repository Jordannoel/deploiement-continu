Les commandes à exécuter pour installer le serveur wildfly, après avoir installé lxd :

- sudo lxc exec <nom_container> -- apt -y upgrade
- sudo lxc exec <nom_container> -- apt -y install openssh-server sudo python
- sudo lxc exec <nom_container> -- adduser $USER
- sudo lxc exec <nom_container> -- usermod -a -G sudo $USER

Ensuite, si le container est bien créé, la commande ssh <adresse_container> doit fonctionner.
Ensuite, créer un fichier inventory.ini comme celui fourni.
Ensuite, créer un fichier playbook.yml comme celui fourni.
Lancer le playbook avec la commande :
- ansible-playbook -i inventaire.ini -k -K -b playbook.yml
