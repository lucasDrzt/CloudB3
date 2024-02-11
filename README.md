# CloudB3

## 1. deploy_database :
Script Bash pour déployer un serveur de base de données.
Nécessite un nom de serveur en argument.
Crée une instance de base de données avec des paramètres spécifiques (type PRO2-XXS, zone fr-par-1, image Debian Bookworm).
Utilise un script cloud-init situé à /home/lucas/cloud/drupalTest/install_database.
Fournit des instructions pour accéder à l'instance après son lancement.
## 2. deploy_Drupal :
Script Bash pour déployer un serveur Drupal.
Nécessite un nom de serveur en argument.
Semblable à deploy_database, il crée une instance de serveur avec des paramètres spécifiques et utilise un script cloud-init à /home/lucas/cloud/drupalTest/install_drupal.
Fournit une commande pour vérifier l'ID de l'instance après le déploiement.
## 3. go :
Un script bash utilitaire pour accéder aux instances de serveur.
Nécessite un ID d'instance en argument.
Liste les instances actuelles si aucun ID n'est fourni.
Utilise la commande scw pour récupérer l'IP publique et se connecter en SSH à l'instance.
## 4. install_database :
Un script bash pour configurer un serveur MariaDB.
Effectue une mise à jour du système, installe MariaDB et démarre/active le service MariaDB.
Crée deux bases de données et deux utilisateurs pour Drupal, en leur attribuant les privilèges appropriés.
## 5. deploy_Drupal_backend1 et deploy_Drupal_backend2 :
Les deux sont des scripts bash pour déployer des instances de backend Drupal.
Nécessitent un nom de serveur en argument.
Créent des instances de serveur avec des paramètres spécifiques et utilisent des scripts cloud-init situés à /home/lucas/cloud/drupalTest/install_drupal_backend1 et /home/lucas/cloud/drupalTest/install_drupal_backend2 respectivement.
Fournissent des instructions pour vérifier le statut de l'instance.
