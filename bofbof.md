# ETAPE 1:
Pour commencer Téléchargez le fichier docker-compose.yml : curl https://hackropole.fr/challenges/fcsc2021-pwn-bofbof/docker-compose.public.yml -o docker-compose.yml
Prerequit Netcat : https://nmap.org/download.html
# ETAPE 2:
Lancez l'épreuve en exécutant dans le même dossier : docker compose up

# ETAPE 3:
Dans un second terminal, accédez à l'épreuve via Netcat avec :
nc localhost 4000

# ETAPE 4:
