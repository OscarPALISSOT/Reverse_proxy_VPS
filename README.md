## Reverse proxy vps

Ce repository Git contient le reverse proxy pour le serveur web de mon VPS.

### Technologies utilisées

- **Docker** : pour la conteneurisation.
- **Nginx** : pour le reverse proxy.
- **Certbot** : pour les certificats SSL.

### Génération des certificats SSL

Pour générer les certificats SSL, il faut exécuter la commande suivante :

```bash
docker exec certbot certbot certonly --webroot -w /var/www/certbot -d example.fr -d www.example.fr --non-interactive --force-renewal
```
Le répertoire `/var/www/certbot` est le répertoire webroot de Nginx.
Le renouvellement des certificats se fait automatiquement grâce à un conteneur cerbot.


 
