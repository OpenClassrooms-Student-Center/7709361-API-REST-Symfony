# 7709361-API-REST-Symfony

Ce projet sert de support au cours au cours sur API et Symfony d'Openclassrooms. 
Il est réalisé avec Symfony 6 et nécessite à minima PHP8. 

Pour vérifier votre version de php vous pouvez faire :

  - _php -v_ 


Pour utiliser ce projet, vous pouvez simplement faire un :

  - _git clone https://github.com/OpenClassrooms-Student-Center/7709361-API-REST-Symfony.git_
  
Et une fois le projet récupérez il faudra l'initialiser : 

  - _composer install_ : pour récupérer l'ensemble des packages nécessaires
  - créer vos clefs publiques et privées pour JWT dans config/jwt :
    - créez le répertoire "jwt" dans le dossier config
    - _openssl genpkey -out config/jwt/private.pem -aes256 -algorithm rsa -pkeyopt rsa_keygen_bits:4096_ : pour créer la clef privée
    - _openssl pkey -in config/jwt/private.pem -out config/jwt/public.pem-pubout_ : pour créer la clef publique
  - créer un fichier .env.local 
    - ce fichier doit contenir vos identifiants de connexion à la base de données
    - le chemin vers vos clefs privées et publiques
    - votre passphrase de création de clef
  - _php bin/console doctrine:database:create_ : pour créer la base de données
  - _php bin/console doctrine:schema:update --force_ : pour créer les tables
  - _php bin/console doctrine:fixtures:load_ : pour charger les fixtures

Si _openssl_ ne fonctionne pas, tentez de lancer cette commande depuis un "gitbash". 

Pour tester les routes, vous pouvez les interroger directement via postman. Par exemple : 
  - https://127.0.0.1:8000/api/login_check : pour se logger
  - https://127.0.0.1:8000/api/books : pour récuperer la liste des livres

Vous pouvez également utiliser la documentation via Nelmio : 
  - https://127.0.0.1:8000/api/doc
 
Vous pouvez également utiliser API Platform :
  - https://127.0.0.1:8000/apip

Chaque branche du projet correspond à un chapitre du cours. 
En cas de soucis, référez-vous au cours d'Openclassrooms.

Bonne chance !
