# Les-logs

## 1. Installe un serveur web (Apache ou Nginx) sur une machine virtuelle Linux  
Vérifier que le serveur Apache2 est installé :  
![Capture d'écran 2024-12-16 110607](https://github.com/user-attachments/assets/7d29bedf-01ad-4261-bfeb-948016a22b80)

Le retour de la commande indique que le serveur est installé. :white_check_mark:  

## 2. Configure le logging pour enregistrer les accès et les erreurs  

Par défaut, le fichier de configuration d'Apache se trouve dans ``/etc/apache2/sites-available/000-default.conf``.  
Il faut ensuite s'assurer que ces 2 lignes sont décommentées, elles enregistrent les erreurs d'Apache pour la première et les requêtes pour la deuxième :  
``ErrorLog ${APACHE_LOG_DIR}/error.log``  
``CustomLog ${APACHE_LOG_DIR}/access.log combined``  

Dans le cas où elles sont commentées, il faut décommenter et relancer le service (pour rappel ``systemctl restart apache2``).  
