# CloudB3

## 1. Install_drupal:
Script Bash pour installer Drupal.
Met à jour le système et installe les dépendances nécessaires (Apache2, MariaDB, PHP, etc.).
Configure et démarre Apache et MariaDB.
Crée une base de données et un utilisateur pour Drupal.
Configure PHP avec des paramètres spécifiques.
Télécharge et installe Drupal, puis configure les permissions des fichiers.
Redémarre Apache et indique que l'installation de Drupal est terminée.

## 2. Install_drupal_backend1:
Similaire au script install_drupal.
Télécharge et installe une instance spécifique de Drupal (drupal1).
Les autres étapes sont identiques à celles du script install_drupal.

## 3. Install_drupal_backend2:
Également similaire au script install_drupal.
Se concentre sur l'installation d'une autre instance de Drupal (drupal2).
Suit le même processus d'installation et de configuration que les autres scripts.

## 4. install_database :
Un script bash pour configurer un serveur MariaDB.
Effectue une mise à jour du système, installe MariaDB et démarre/active le service MariaDB.
Crée deux bases de données et deux utilisateurs pour Drupal, en leur attribuant les privilèges appropriés.

## 5. go :
Un script bash utilitaire pour accéder aux instances de serveur.
Nécessite un ID d'instance en argument.
Liste les instances actuelles si aucun ID n'est fourni.
Utilise la commande scw pour récupérer l'IP publique et se connecter en SSH à l'instance.

## 6. deploy_database :
Script Bash pour déployer un serveur de base de données.
Nécessite un nom de serveur en argument.
Crée une instance de base de données avec des paramètres spécifiques (type PRO2-XXS, zone fr-par-1, image Debian Bookworm).
Utilise un script cloud-init situé à /home/lucas/cloud/drupalTest/install_database.
Fournit des instructions pour accéder à l'instance après son lancement.

## 7. deploy_Drupal :
Script Bash pour déployer un serveur Drupal.
Nécessite un nom de serveur en argument.
Semblable à deploy_database, il crée une instance de serveur avec des paramètres spécifiques et utilise un script cloud-init à /home/lucas/cloud/drupalTest/install_drupal.
Fournit une commande pour vérifier l'ID de l'instance après le déploiement.

## 8. deploy_Drupal_backend1 et deploy_Drupal_backend2 :
Scripts bash pour déployer des instances de backend Drupal.
Nécessitent un nom de serveur en argument.
Créent des instances de serveur avec des paramètres spécifiques et utilisent des scripts cloud-init situés à /home/lucas/cloud/drupalTest/install_drupal_backend1 et /home/lucas/cloud/drupalTest/install_drupal_backend2 respectivement.
Fournissent des instructions pour vérifier le statut de l'instance.

## 9. deleteall:
Script Bash pour supprimer toutes les instances.
Liste et arrête toutes les instances en cours d'exécution, puis les supprime.

## 10. deletesome:
Script Bash pour supprimer des instances spécifiques.
Nécessite un mot-clé en argument pour identifier les instances à supprimer.
Liste les instances dont le nom contient le mot-clé, demande confirmation avant de procéder à la suppression.
Arrête et supprime les instances sélectionnées.

## 11. getip:
Script Bash pour obtenir l'IP publique d'une instance.
Nécessite un ID d'instance en argument.
Récupère et affiche l'IP publique de l'instance spécifiée.
